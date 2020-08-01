---
title: Lists
---

Lists are an ordered list of elements of possibly different types identified by a number index. Each element in a list can be accessed individually by their index. Lists are constructed as a comma separated list of elements, enclosed by square brackets:

```dart
[
    "Ghost",
    57.3,
    function(x) { x * x}
]
```

Here we've created a list consisting of three elements; note that they are all different types.

## Accessing Elements
You can access any element in a list by calling the subscript operator on it with the index of the element you want. Like most languages, indices start at zero:

```dart
vocabulary := ["activation", "propogate", "execute", "initialize"]

print(vocabulary[0])  // >> activation
print(vocabulary[1])  // >> propogate
print(vocabulary[2])  // >> execute
print(vocabulary[3])  // >> initialize
```