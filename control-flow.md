---
title: Control Flow
---

Control flow is used to determine which blocks of code are executed and how many times. _Branching_ statements and expressions decide whether or not to execute some code and _looping_ ones execute something more than once.

<!-- ## Truthiness -->

## Logical Operators
Unlike most other operators in Ghost which are just a special syntax for method calls, the `and` and `or` operators are special. This is because they only conditionally evaluate right operand--they short-circuit.

An `and` ("logical and") expression evaluates the left-hand argument. If it's false, it returns that value. Otherwise it evaluates and returns the right-hand argument.

```dart
print(false and 1)
print(1 and 2)
```

An `or` ("logical or") expression is reversed. If the left-hand argument is _true_, it's returned, otherwise the right-hand argument is evaluated and returned:

```dart
print(false or 1)
print(1 or 2)
```

## If Statements
The simplest branching statement, `if` lets you conditionally skip a chunk of code. It looks like this:

```dart
if (ready) {
    print("go!")
}
```

This evaluates the parenthesized expression after `if`. It it's true, then the block after the condition is evaluated. Otherwise it is skipped.

You may also provide an `else` branch. It will be executed if the condition is false:

```dart
if (ready) {
    print("go!")
} else {
    print("not ready!")
}
```

## While Statements
It's hard to write a useful program without executing some chunk of code repeatedly. To do that, you use looping statements. There are two in Ghost, and they should be familiar if you've used other imperative languages.

The simplest, a `while` statement executes a chunk of code as long as a condition continues to hold. For example:

```dart
// Hailstone sequence
n := 27

while (n != 1) {
    if (n - 2 * (n / 2) == 0) {
        n /= 2
    } else {
        n = 3 * n + 1
    }
}
```

This evaluates the expression `n != 1`. If it is true, then it executes the following block. After that, it loops back to the top, and evaluates the condition again. It keeps doing this as long as the condition evaluates to something true.