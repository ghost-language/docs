---
title: Variables
date: 2020-04-30
slug: variables
---

Variables are named slots for storing values. You define a new variable in Ghost using a `var` statement, like so:

```javascript
var a = 1 + 2;
```

This creates a new variable `a` in the current scope and initializes it with the result of the expression following the `=`. Once a variable has been defined, it can be accessed by name as you would expect.

```javascript
var technology = "Micromachines";

print(technology);
```

## Scope
Ghost has true block scope: a variable exists from the point where it is defined until the end of the block where that definition appears.

```javascript
{
    print(a);  // Error: "a" doesn't exist yet.

    var a = 123;

    print(a);
}

print(a);  // Error: "a" doesn't exist anymore.
```

Variables defined at the top level of a script are _top-level_, or _global_. All other variables are _local_. Declaring a variable in an inner scope with the same name as an outer one is called _shadowing_ and is not an error.

```javascript
var a = "outer";

{
    var a = "inner";

    print(a);  // inner
}

print(a);  // outer
```

On the other hand, declaring a variable with the same name in the _same_ scope _is_ an error.

```javascript
var a = "hi";
var a = "again";  // Error: "a" is already declared.
```

## Assignment
After a variable has been declared, you can assign to it using `=`:

```javascript
var a = 123;

a = 456;
```

An assignmet walks up the scope stack to find where the named variable is declared. It's an error to assign to a variable that isn't defined. Ghost does not support implicit variable definition.