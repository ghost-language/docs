---
title: Values
---

In Ghost's little universe, the atoms that make up all matter are the built-in data types.

## Booleans
A boolean value represents truthy or falsy states. There are two boolean values, `true` and `false`.

## Numbers
Ghost has a single numeric type: arbitrary-precision fixed-point decimals. Number values look like you expect from other languages:

```
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
"Hello, world!"
'こんにちは、世界'
```

## Null
Ghost, like many languages, has a special value `null`. It functions a bit like `void` in some languages: it indicates the absence of a value. If you call a method that doesn't return anything and get its return value, you get `null` back.