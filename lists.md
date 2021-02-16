---
title: Lists
---

Lists are an ordered list of elements of possibly different types identified by a number index. Each element in a list can be accessed individually by their index. Lists are constructed as a comma separated list of elements, can contain any type of value, and are enclosed by square brackets:

```dart
[
    "Ghost",
    57.3,
    function(x) { x * x}
]
```

## Accessing Elements
You can access any element in a list by calling the subscript operator on it with the index of the element you want. Like most languages, indices start at zero:

```dart
vocabulary := ["activation", "propogate", "execute", "initialize"]

print(vocabulary[0])  // >> activation
print(vocabulary[1])  // >> propogate
print(vocabulary[2])  // >> execute
print(vocabulary[3])  // >> initialize
```

## List Methods

### `List.first()`
Returns the first element of the list.

### `List.join(separator)`
Joins all elements of the list into a string, using `separator` to join the elements together.

### `List.last()`
Returns the last element of the list.

### `List.length()`
Returns the number of elements in the list.

### `List.push(element)`
Adds one new `element` to the end of the list and returns the new length.

### `List.tail()`
Returns a new list containing all elements but the first.

### `List.toString()`
Returns a string representing the list and its elements.