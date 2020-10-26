---
title: Control Flow
---

Control flow is used to determine which blocks of code are executed and how many times. _Conditional_ statements and expressions decide whether or not to execute some code and _looping_ ones execute something more than once.

## Truthiness

### Logical Operators
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

## Conditional Statements
A conditional statement is a set of commands that executes if a specified condition is true.

## If Statement
The simplest conditional statement, `if` lets you conditionally skip a chunk of code. It looks like this:

```dart
if (condition) {
    // Do something
}
```

This evaluates the parenthesized expression after `if`. If it's `true`, then the block after the condition is evaluated. Otherwise it is skipped. The condition can be any expression that evaluates to `true` or `false`.

You may also provide an `else` branch. It will be executed if the condition is `false`:

```dart
if (condition) {
    // Do something
} else {
    // Do something else
}
```

## Looping Statements
A looping statement offers a quick and easy way to do something repeatedly. In this section, we'll introduce the different looping statements available in Ghost.

### While Statement
A `while` statement executes its block as long as a specified condition evaluates to `true`. A `while` statement looks like the following:

```dart
while (condition) {
    // Do something
}
```

The condition test occurs _before_ the block is executed. If the condition returns `true`, the block is executed and the condition is tested again. If the condition returns `false`, execution stops, and control is passed to the statement following `while`.

#### Example 1
The following `while` loop iterates as long as `n` is less than `3`:

```dart
n := 0
x := 0

while (n < 3) {
    n++
    x += n
}
```

With each iteration, the loop increments `n` and adds that value to `x`. Therefore, `x` and `n` take on the following values:

- After the first pass: `n` = `1` and `x` = `1`
- After the second pass: `n` = `2` and `x` = `3`
- After the third pass: `n` = `3` and `x` = `6`

After completing the third pass, the condition `n < 3` is no longer `true`, so the loop terminates.

#### Example 2
Generally you'll want to avoid infinite loops (there are very few cases where an infinite loops are utilized, such as in game development). These are loops where the condition never evaluates to `false`. The following example will loop forever because the condition is always `true`:

```dart
while (true) {
    print("Hello, world!")
}
```

### For Statement
A `for` loop repeats until a specified condition evaluates to `false`. The Ghost `for` loop is similar to the C loop for those familiar.

A `for` statement looks like the following:

```dart
for (initializer; condition; increment) {
    // Do something
}
```

When a `for` loop executes, the following occurs:

1. The initializing expression is executed. This expression usually initializes one or more loop counters. This expression can declare variables.
2. The condition expression is evaluated. If the value of condition is `true`, the loop block is executed. If the value of condition is `false`, the `for` loop terminates.
3. The block executes.
4. The increment expression is executed.
5. Control returns to step 2 until the condition expression evaluates to `false`.