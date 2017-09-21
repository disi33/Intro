# Syntax

Each line in GLS consists of a function, a colon, and any number of arguments, all separated by spaces.

```
print : "GLS!"
```

* Function: `print`
* Argument: `"GLS!"`

`print : GLS` will compile to `System.Console.WriteLine("GLS!");` in C\#, `console.log("GLS!");` in TypeScript, and so on.

### Parenthesis

You can keep spaces inside your arguments by wrapping characters in parenthesis. This tells the compiler to treat the space as part of the argument instead of a separator.

```
print : ("Hello world!")
```

* Function: `print`
* Argument: `"Hello world!"`

### Recursion

To pipe the output of one command into another, wrap the inner command with`{}`brackets.

```
print : { operation : 1 plus 2 }
```



