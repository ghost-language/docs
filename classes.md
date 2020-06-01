---
title: Classes
date: 2020-05-05
slug: classes
---

Classes define an objects _behavior_ and _state_. Behavior is defined by [methods](/method-calls) which live in the class. Every object of the same class supports the same methods. State is defined in fields, whose values are stored in each instance.

## Defining A Class
Classes are created using the `class` keyword, unsurprisingly:

```javascript
class CoffeeMaker {
    //
}
```

This creates a class named `CoffeeMaker` with no methods or fields.

## Methods
To add functionality to our coffee major, we need to give it methods.

```javascript
class CoffeeMaker {
    brew() {
        print("Your coffee is now brewing.");
    }
}
```

This defines a `brew` method that takes no arguments. To add parameters, put their names inside the parentheses:

```javascript
class CoffeeMaker {
    brew(dosage, temperature) {
        print("Your " + dosage + " of coffee is now brewing at " + temperature + " degrees.");
    }
}
```

## Method Scope
Up to this point, "[scope](/variables#scope)" has been used to talk exclusively about [variables](/variables). In a procedural language like C, or a functional one like Scheme, that's the only kind of scope there is. But object-oriented languages like Ghost introduce another kind of scope: _object scope_. It contains the methods that are available on an object. When you write:

```
Coffee.brew();
```

you're saying "look up the method `brew` in the scope of the object `Coffee`". In this case, the fact that you want to look up a _method_ `brew` and not a _variable_ is explicit. That's what `.` does and the object to the left of the period is the object you want to look up the method on.

### `this`
Things get more interesting when you're inside the body of a method. When the method is called on some object and the body is being executed, you often need to access that object itself. You can do that using `this`.

```javascript
class CoffeeMaker {
    setGrind(grind) {
        this.grind = grind;
    }

    printGrind() {
        this.setGrind("course");

        print(this.grind);
    }
}
```

The `this` keyword works sort of like a variable, but has special behavior. It always refers to the instance whose method is currently being executed. This lets you invoke methods on "yourself".

It's an error to refer to `this` outside of a method. However, it's perfectly fine to use it _inside_ a method. When you do, `this` still refers to the instance whose _method_ is being called:

```javascript
class CoffeeMaker {
    setGrind(grind) {
        this.grind = grind;
    }

    printGrindThrice() {
        this.setGrind("course");

        for (var i = 0; i < 3; i = i + 1) {
            print(this.grind);
        }
    }
}
```

This is unlike Lua and JavaScript which can "forget" `this` when you create a callback inside a method. Ghost does what you want here and retains the reference to the original object.

(In technical terms, a function's closure includes `this`. Ghost can do this because it makes a distinction between methods and functions.)

## Constructors
We've seen how to define classes and how to declare methods on them. Our coffee maker can brew coffee, but we don't actually have any way to control it. To create _instances_ of a class, we need a _constructor_. You define one like so:

```javascript
class CoffeeMaker {
    constructor(grind, temperature) {
        print("Grind set to: " + grind);
        print("Temperature set to: " + temperature);
    }
}
```

The `constructor` keyword says we're defining a constructor. To make a coffee maker now, we can now pass through the set arguments to customize our class:

```javascript
var drip = CoffeeMaker("flat", "200");
var chemex = CoffeeMaker("coarse", "202");
var pourOver = CoffeeMaker("fine", "202");
var frenchPress = CoffeeMaker("very course", "202");
```

Note that we didn't need to call the `constructor` method directly. A constructor is actually a method on the class. When we reference a class using `()`, Ghost creates the new instance, then it invokes the _constructor_ on that instance. This is where the constructor body you defined gets run.

This distinction is important because it means inside the body of the constructor, you can access `this`, assign fields, etc.

## Fields
All state stored in instances is stored in _fields_. Each field has a name, are bound to `this`, and act the same as variables.

```javascript
class CoffeeMaker {
    constructor(grind, temperature) {
        this.grind = grind;
        this.temperator = temperature;

        this.printSettings();
    }

    printSettings() {
        print("Grind set to: " + this.grind);
        print("Temperature set to: " + this.temperature);
    }
}
```

## Inheritance
A class can inherit from a "parent" or _superclass_. When you invoke a method on an object of some class, if it can't be found, it walks up the chain of superclasses looking for it there.

To inherit another class, use `extends` when you declare your class:

```javascript
class Bar extends foo {
    //
}
```

This declares a new class Bar that inherits from Foo.