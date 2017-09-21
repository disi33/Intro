# Main

All languages provide some way to execute code immediately.

Scripting languages such as Python and Ruby will execute all code in order immediately, whereas class-based languages such as C\# and Java require a class wrapping a static method akin to C/C++'s "main" function.

GLS resolves the differences by declaring an area as a "main context". A main function may be declared within that context.

```gls
main context start
    main start
        print : ("Hello world!")
    main end
main context end
```

In C\#:

```csharp
using System;

class Program
{
    public static void Main()
    {
        Console.WriteLine("Hello world!");
    }
}
```

In Python:

```python
if __name__ == "__main__":
    print("Hello world!")
```

### Functions

Floating functions may also be declared within the main context. These become regular functions in scripting languages and static members of the class in class-based languages.

```gls
main context start
    function start : SayHello void name string
        print : { concatenate : ("Hello, ") name "!" }
    function end

    main start
        function : SayHello "GLS"
    main end
main context end
```

In C\#:

```csharp
using System;

class Program
{
    void SayHello(string name)
    {
        Console.WriteLine("Hello, " + name + "!");
    }

    public static void Main()
    {
        SayHello("GLS");
    }
}
```

In Python:

```python
def say_hello(name):
    print("Hello, " + name + "!")

if __name__ == "__main__":
    say_hello("GLS")
```



