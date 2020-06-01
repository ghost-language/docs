---
title: Values
date: 2020-04-29
slug: values
---

In Ghost's little universe, the atoms that make up all matter are the built-in data types.

## Booleans
A boolean value represents truthy or falsy states. There are two boolean literals, `true` and `false`.

## Numbers
Ghost has a single numeric type: double-precision floating point. Number literals look like you expect from other languages:

```
0
1234
-5678
3.14159
1.0
-12.34
```

## Strings
A string is an array of bytes. String literals are surrounded in double quotes.

```javascript
"Hello, world!"
```

## Null
Ghost, like many languages, has a special value `null`. It functions a bit like `void` in some languages: it indicates the absence of a value. If you call a method that doesn't return anything and get its return value, you get `null` back.