# CM Syntax
Syntax that add some extra flavor on top of regular CM but don't fit under any of the other more specific topics in this repo.

## ifCast
Just your good and old `if` statements on steroids. 

### Code
```java
/**
 * Tries to cast a given object into one of the provided types (as) OR
 * checks if it's not one of the provided ones (!in - !as)
 */
public statement cast '(' @what=id @checkType=expr @types=list[type, ',']* ')' 
                 @args=[":" actualArgList]?
                 @doWhat=statement 
                 @else=["else" statement]? { 
    
    str checkTypeS = checkType.toS;
    const str regularCheck = "as";
    const str reverseTypeCheck = "(!in)";
    const str{} allowedChecks = { regularCheck, reverseTypeCheck};
    
    if (checkTypeS !in allowedChecks) { 
        pln("Invalid Check Type"; #checkType; #allowedChecks);
        return statement {  };
    }
    
    const str foundFieldId = "found";
    SId foundId(spnn(foundFieldId, what, checkTypeS), what.src);
    SStatements s = statement { bool @foundId = false; };

    if (checkTypeS == reverseTypeCheck) {

        const str typeFieldId = "type";
        SId typeId(spnn(typeFieldId, what, checkTypeS), what.src);
        
        const str negateTypeFieldId = "negateType";
        SId negateTypeId(spnn(negateTypeFieldId, what, checkTypeS), what.src);
        
        /// Reverse type check
        s << statement {
            Type @typeId = @what.?class;
            if (!@typeId) {
                @else;
                @foundId = true;
            }
            Type{} @negateTypeId();
        };
        
        for (t in types) { 
            Type tType = t.type;
            s << block { 
                @negateTypeId << @tType;
            };
        }
        
        s << statement {
            if (@typeId !in @negateTypeId) {
                @doWhat;
                @foundId = true;
            }
        };
        
    } else { 

        /// Regular type check
        for (t in types) { 
            Type tType = t.type;
            s << block { 
                if (@what as @tType) { 
                    @foundId = true;
                    @doWhat;
                }
            };
        }
    }
    
    
    s << block { 
        if(!@foundId) { 
            @else;
        }
    };
    
    return s;
}
```

### Examples

```java

/**
 * Regular class with no declared inheritance 
 */
public class Class1 { 
    public constructor auto();
    extend public void someMethod() { 
        pln("Hey from Class 1");
    }
}

/**
 * Regular class with no declared inheritance 
 */
public class Class2 { 
    public constructor auto();
    extend public void someMethod() { 
        pln("Hey from Class 2");
    }
}

/**
 * Regular class inheriting from Class2
 */
public class Class3 extends Class2 { 
    public void someMethod() { 
        pln("Hey from Class 3");
    }
}

/**
 * Regular class with no declared inheritance and no shared member signature
 */
public class Class4 { 
    public constructor auto();
    extend public void methodThatOnlyClass4Exposes() { 
        pln("Hey from Class 3");
    }
}

{
    /// Play around with this guy...
    Object myObject = Class1();
    
    /// Simple composite type check
    cast (myObject as Class1, Class2, Class3) { 
        myObject.someMethod();
    } else { 
        pln("This is something else"; #myObject);
    }
    
    /// Reverse composite type check
    cast (myObject !in Class1, Class2, Class3) {
        pln("This is cool"; #myObject);
    } else { 
        pln("This is something else"; #myObject);
    }
}
```
