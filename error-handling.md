---
title: Error Handling
date: 2020-05-02
slug: error-handling
---

_I am error._

## Syntax Errors
The first errors you are likely to run into are syntax errors. These include simple bugs where your code doesn't following Ghost's grammar, like:

```javascript
1 + * 2
```

Ghost detects these errors as soon as it tries to read your code. When it hits one, you get a friendly error message, like:

```
[line 1] Error at '*': Expect expression.
```

Some slightly more "semantic" errors fall into this bucket too. Things like using a variable that hasn't been defined, or declaring two variables with the same name in the same scope. So if you do:

```javascript
{
    var a = "one";
    var a = "two";
}
```

Ghost tells you:

```
[line 3] Error at 'a': Variable with this name already declared in this scope.
```

Note that it does this before it executes _any_ code. Unlike some other scripting languages, Ghost tries to help you find your errors as soon as possible when it can.

If it starts running your code, you can be sure you don't have any errors related to syntax or variable scope.

## Runtime Errors
There is one more round of errors that Ghost will emit. Your program may still have errors that can't be detected statically. Since they can't be found until your code is run, they're called "runtime" errors.

Most runtime errors come from the VM itself. They arise from code trying to perform an operation that the VM can't do. The most common error is a "method not found" one. If you call a method on an object and its class doesn't define that method, there's nothing Ghost can do:

```javascript
class Foo
{
    function bar()
    {
        //
    }
}

var foo = Foo();

foo.someRandomMethod();
```

If you run this, Ghost will print:

```
Foo does not implement method 'someRandomMethod'.
```

Then it stops executing code. Unlike some other languages, Ghost will not keep plugging away after a runtime error has occured.

This is just one example of a runtime error, but there are others. A runtime error implies there's a bug in your code and it wants to draw your attention to it.

## Creating Runtime Errors
Most runtime errors come from within the Ghost VM, but you may want to be able to cause your own runtime errors to occur. This can be done by calling the `error()` method:

```javascript
error("Something bad happened");
```

You must pass in an error message, and it must be a string. If the provided message is `null`, no runtime error is raised.