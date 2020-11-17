

# Index

 1.  Visual Studio Code Extension
 2.  Helpful commands


# Visual Studio Code Extension
If you already love [Visual Studio Code](https://code.visualstudio.com/) or you're just curios as to what other options you have to code for CET I'm here to give you some great news! 

The great [twlamb](https://github.com/twlamb) brought us this amazing extension that makes my - potentially yours as well - life *super* easy.  

I'm obviously talking about [vscode-cm](https://github.com/docura-io/vscode-cm), the one - and only at this point - tool for CET developers that don't want to learn/stick with emacs. It brings a huge list of features and is actively maintained. 

# Helpful commands

Here's a list of the most used and common commands you might need to use while writing/troubleshooting CM code:

|Command | Description  |Example| 
|--|--|--| 
| `pln` | CM's very onw `Console.WriteLine`, `alert` or `cout` | `pln("Hello World!");`| 
| `inspect` | Opens up the inspect tool with the object you provide as its parameter. It's a great way to look into what a given `Object` holds in its properties without having to rely in a series of `pln`s | `inspect(myObject);`| 
| `stackTrace` | Outputs the stack up to the point where this instruction was placed. Very useful to pinpoint the path your code took to arrive on a certain spot | `stackTrace();`| 
| `ptrace`| During (or specially after) a debug session, have you ever wondered where that one left over message *"HERE!!"* is? Fear no more, `ptrace` is basically a `pln` prefixed with the path to where that message is so you know exactly what file you need to undo/recompile to get rid of that leftover message. | `ptrace("Oh no!");`| 
| `developMode` | CET's built in flag to allow you to check whether or not you're currently running on a DEV's machine. As a matter of fact, if you haven't already, you should go check out this file: `.\base\cm\basic\release.cm`. It holds some interesting/useful flags for these sort of things. | `if (developMode) { pln("It works here!"); }` | 
