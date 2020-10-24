---
title: Style Guide
---

The key words "MUST", "MUST NOT", "REQUIRED", "SHALL", "SHALL NOT", "SHOULD", "SHOULD NOT", "RECOMMENDED", "MAY", and "OPTIONAL" in this document are to be interpreted as described in [RFC 2119](http://tools.ietf.org/html/rfc2119).

## Introduction
This is the official style guide for Ghost-specific code. If you use Ghost in a project, it's a great reference to avoid errors, bikeshedding, and anti-patterns. However, we don't believe that any style guide is ideal for all teams or projects, so mindful deviations are encouraged based on past experience, the surrounding tech stack, and personal values.

## General
- Function names MUST be declared in `camelCase`
- Variable names MUST be declared in `camelCase`

## Lines
There MUST NOT be a hard limit on line length.

The soft limit on line length MUST be 120 characters.

Lines SHOULD NOT be longer than 80 characters; lines longer than that SHOULD be split into multiple subsequent lines of no more than 80 characters each.

There MUST NOT be trailing whitespace at the end of lines.

Blank lines MAY be added to improve readability and to indicate related blocks of code except where explicitly forbidden.

There MUST NOT be more than one statement per line.

## Indenting
Code MUST use an indent of 4 spaces for each indent level, and MUST NOT use tabs for indenting.

## Keywords and Types
All Ghost reserved keywords and types MUST be in lower case.

Any new types and keywords added to future Ghost versions MUST be in lower case.

## Functions
Function names MUST NOT be declared with space after the method name. The opening brace MUST go on its own line, and the closing brace MUST go on the next line following the body. There MUST NOT be a space after the opening parenthesis, and there MUST NOT be a space before the closing parenthesis.

A function declaration looks like the following. Note the placement of parentheses, commas, spaces, and braces.

```dart
function fooBarBaz(arg1, arg2, arg3)
{
    // function body
}
```

## Function Arguments
In the argument list, there MUST NOT be a space before each comma, and there MUST be one space after each comma.

```dart
function fooBarBaz(arg1, arg2, arg3)
{
    // Function body
}
```

## Function Calls
When making a function call, there MUST NOT be a space between the function name and the opening parenthesis, there MUST NOT be a space after the opening parenthesis, and there MUST NOT be a space before the closing parenthesis. In the argument list, there MUST NOT be a space before each comma, and there MUST be one space after each comma.

```dart
foo(arg1, arg2)
```

## Control Structures
The general style rules for control structures are as follows:

- There MUST be one space after the control structure keyword
- There MUST NOT be a space after the opening parenthesis
- There MUST NOT be a space before the closing parenthesis
- There MUST be one space between the closing parenthesis and the opening brace
- The structure body MUST be indented once
- The body MUST be on the next line after the opening brace
- The closing brace MUST be on the next line after the body

The body of each structure MUST be enclosed by braces.

## if, else if, else
An `if` structure looks like the following. Note the placement of parentheses, spaces, and braces; and that `else` and `else if` are on the same line as the closing brace from the earlier body.

```dart
if (condition1) {
    // if body
} else if (condition2) {
    // else if body
} else {
    // else body
}
```

## while
A `while` statement looks like the following. Note the placement of parentheses, spaces, and braces.

```dart
while (condition) {
    // structure body
}
```

## Binary Operators
All binary artihmetic, comparison, and assignment operators MUST be preceded and followed by at least one space:

```dart
if (a == b) {
    foo = bar
} else if (a > b) {
    foo = a + b * c
}
```

## Closures
Closures MUST be declared with a space after the `function` keyword.

The opening brace MUST go on the same line, and the closing brace MUST go on the next line following the body.

There MUST NOT be a space after the opening parenthesis of the argument list or variable list, and there MUST NOT be a space before the closing parenthesis of the argument list or variable list.

In the argument list and variable list, there MUST NOT be a space before each comma, and there MUST be one space after each comma.

A closure declaration looks like the following. Note the placement of parentheses, commas, spaces, and braces:

```dart
closure := function (arg1, arg2) {
    // body
}
```