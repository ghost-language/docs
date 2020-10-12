---
title: Functions
---

Like Lua, functions are first-class values in Ghost. That means that functions can be stored in variables, passed as arguments to other functions, and returned as results. This gives great flexibility to the language.

## Defining Functions
You define functions using the `function` statement, followed by a list of parameters, and a body:

```dart
function sum(a, b) {
    print(a + b)
}
```

The body of a function is always a block. Inside it, you can return a value using a `return` statement.

```dart
function sum(a, b) {
    return a + b
}
```

If execution reaches the end of the block without hitting a `return`, it implicitly returns the last value from the function's body.

```dart
function returnMessage(message) {
    a := 5

    message
}

value := returnMessage("Hello, world!")

print(value)  // >> Hello, world!
```

## Calling Functions
Once you have a function, calling it is as simple as passing the required parameters along with the function name:

```dart
value := sum(1, 2)
```

The assigned value is the result of either an explicit `return` statement or the last value of the function's body.

## Anonoymous Functions
Functions are _first class_ in Ghost, which just means they are real values that you can get a reference to, store in variables, pass around, etc.

```dart
function addPair(a, b) {
    return a + b
}

function identity(a) {
    return a
}

print(identity(addPair)(1, 2))  // >> 3
```

Since function declarations are statements, you can declare local functions inside another function:

```dart
function outerFunction() {
    function localFunction() {
        print("I'm local!")
    }

    localFunction()  // >> I'm local!
}
```

You can even combine local functions, first-class functions, and block scope:

```dart
function returnFunction() {
    outside := "outside"

    function inner() {
        print(outside)
    }

    return inner
}

newFunction := returnFunction()
newFunction()  // >> outside
```
