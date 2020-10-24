---
title: Values
---

In Ghost's little universe, the atoms that make up all matter are the built-in object types. All values are _objects_, and may contain any number of methods to further work with their data. Below we'll briefly introduce each.

## Booleans
A boolean value represents truthy or falsy states. There are two boolean values, `true` and `false`.

## Lists
Lists are an ordered list of elements of possibly different types identified by a number index. Each element in a list can be accessed individually by their index. Lists are constructed as a comma separated list of elements, can contain any type of value, and are enclosed by square brackets:

```dart
[
    "Ghost",
    57.3,
    function(x) { x * x}
]
```

## Maps
Maps — sometimes called _associative arrays_, _hashes_, or _dictionaries_ in other programming languages, store a collection of key-value pairings. Maps are constructed as a comma-separated list of key-value pairs enclosed by curly braces. Each key-value pair uses a colon to differentiate between the key and the value.

```dart
{
    "name": "Ghost",
    "value": 57.3,
    "handler": function(x) { x * x}
}
```

## Null
Ghost, like many languages, has a special value `null`. It functions a bit like `void` in some languages: it indicates the absence of a value. If you call a method that doesn't return anything and get its return value, you get `null` back.

## Numbers
While some languages contain different representations for numbers such as integers, floats, doubles, etc... Ghost has a single numeric type: decimals.

It's true that decimals have a very small performance hit over using something like pure integers or floats. However, having a single numeric type makes working with numbers in Ghost straight forward and simple.

Furthermore, because Ghost uses an arbitrary-precision fixed-point decimal system, it is extremely accurate. Number values look like you expect from other languages:

```dart
0
1234
-5678
3.14159
1.0
-12.34
```

## Strings
A string value is a (possibly empty) sequence of bytes. The number of bytes is called the length of the string and is never negative. String values can be surrounded in either double or single quotes, and can store unicode text.

```dart
string1 := "Hello, world!"
string2 := 'こんにちは、世界'
```