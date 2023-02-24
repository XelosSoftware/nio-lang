# The Nio Programming Language

Nio is a strongly typed functional programming language. It compiles to [CIL](https://en.wikipedia.org/wiki/Common_Intermediate_Language), so it is compatible with the dotnet ecosystem.

```C
[EntryPoint]
Unit main() = print("Hello World!");
```

```C
[EntryPoint]
Unit main() =
{
    for(Int n in 0..10) 
    {
        do print(fibonacci(n));
    };
};

Int fibonacci(Int n) = match(n)
{
    0 | 1 -> 1;
    _ -> fibonacci(n - 1) + fibonacci(n - 2);
};
```

## Core principles

1. Modular → reusability
2. Robust/safe → maintainability, mathematical reasoning, predictable
3. Minimal loss of information in syntax and strongly typed → easier to learn and read
4. No boilerplate → easier to learn/read and fast to write
