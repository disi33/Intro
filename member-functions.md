# Member Functions

Classes may declare member functions that each instance of the class may call.

Declaring a member variable is done with `member variable declare start`. It takes in the function's privacy \(as`public`,`protected`, or`private`\), name in PascalCase, return type, and any number of \(name, type\) pairs of parameters. 

```
class start : Announcer
    member variable declare : private greeting string

    member function declare start : public Greet void name string
        print : { concatenate : { member variable : private { this } greeting } ", " name "!" }
    member function declare end
    
    constructor start : Announcer greeting string
        operation : { member variable : private { this } name } equals name
    constructor end
class end
```



