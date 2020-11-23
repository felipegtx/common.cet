
# CM Collection helpers
Here you will find a list of all the different methods/syntaxes I've created for my projects in order to make me more productive and allow for my code to be more concise and less error prone. 

## First Or Default
Finds the first element on a Collection that matches the predicate. 

### Code

```java
/**
 * Find first item that fulfills a given condition or returns the default value
 * for the items held by this collection
 */
public expr firstOrDefault '('  @id=id "in" @collection=expr "->" @cond=expr ')' {
    Type ct = collection.type.unalias.?elementType;
    if (!ct) {
        bug(spnn("Invalid type. This doesn't look like a collection type", #collection));
    }
    return blockExpr {
        for (@id in @collection) if (@cond) result @id;
        @ct defaultElementValue;
        result defaultElementValue;
    };
};
```


### Example

```java
str[] strColl = ["a", "b", "c"];
str findA = firstOrDefault(y in strColl -> (y == "b"));
pln(#findA);

str notFound = firstOrDefault(y in strColl -> (y == "NOPE"));
pln(#notFound);

strColl = null;
str findNull = firstOrDefault(y in strColl -> (y == "b"));
pln(#findNull);

int{} intColl = { 1, 2, 3 };
int find2 = firstOrDefault(y in intColl -> (y == 1));
pln(#find2);
```

## Filter
Find all items that fulfills a given condition or returns an empty collection if no items are found.

### Code

```java
/**
 * Find all items that fulfills a given condition or returns an empty collection
 * if no items are found.
 */
public expr filter '('  @id=id "in" @collection=expr "->" @cond=expr ')' {
    Type ct = collection.type.unalias;
    return blockExpr {
        @ct coll();
        for (@id in @collection) if (@cond) coll << @id;
        result coll;
    };
};
```

### Example

```java
    str[] myColl = ["house", "car", "carriage", "baby"];
    str[] newColl = filter(y in myColl -> y.contains("car"));
    pln(#newColl);
```

## Dictionary initializer

We all know about `init` / `init?` that can be use to initialize an empty collection. We also know about the `id = [..]`/ `id = { ... } ` constructs. But not everyone know how to initialize a dictionary _with_ data. 

Here it is;   
```java
str->int myDictionary = { "Felipe"->123, "Liz"->999 } ;
```
