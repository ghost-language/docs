---
title: Functions
date: 2020-04-30
slug: functions
---

Like Lua, functions are first-class values in Ghost. That means that functions can be stored in variables, passed as arguments to other functions, and returned as results. This gives great flexibility to the language.

Since Ghost is an object-oriented programming language, most of your code will live in methods on classes, but functional programming is also supported, including nested functions with proper lexical scoping.

## Defining Functions
You define functions using the `function` statement, followed by a list of parameters, and a body:

```javascript
function printSum(a, b) {
    print(a + b);
}
```

The body of a function is always a block. Inside it, you can return a value using a `return` statement.

```javascript
function returnSum(a, b) {
    return a + b;
}
```

If execution reaches the end of the block without hitting a `return`, it implicitly returns `null`.

## Calling Functions
Once you have a function, calling it is as simple as passing the required parameters along with the function name:

```javascript
var value = returnSum(1, 2);
```

The assigned value is the result of the functions `return` statement. As mentioned earlier, if no `return` statement is found within the function, a value of `null` will be returned implicitly.

## Closures
Functions are _first class_ in Ghost, which just means they are real values that you can get a reference to, store in variables, pass around, etc.

```javascript
function addPair(a, b) {
    return a + b;
}

function identity(a) {
    return a;
}

print(identity(addPair)(1, 2));

// Prints "3"
```

Since function declarations are statements, you can declare local functions inside another function:

```javascript
function outerFunction() {
    function localFunction() {
        print("I'm local!");
    }

    localFunction();
}
```

You can even combine local functions, first-class functions, and block scope:

```javascript
function returnFunction() {
    var outside = "outside";

    function inner() {
        print(outside);
    }

    return inner;
}

var newFunction = returnFunction();
newFunction();

// Prints "outside"
```