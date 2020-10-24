---
title: Maps
---

Maps — sometimes called _associative arrays_, _hashes_, or _dictionaries_ in other programming languages, store a collection of key-value pairings. Maps are constructed as a comma-separated list of key-value pairs enclosed by curly braces. Each key-value pair uses a colon to differentiate between the key and the value.

```dart
{
    "name": "Ghost",
    "value": 57.3,
    "handler": function(x) { x * x}
}
```

## Accessing Elements
You can access any element in a map by calling the subscript operator on it with the _key_ of the element you want.

```dart
people := {"Artemis": 35, "Rabbit": 37, "Orion": 43}

print(people["Artemis"])  // >> 35
print(people["Rabbit"])   // >> 35
print(people["Orion"])    // >> 35
```

Calling a key that does not exist will return a `null` value.

```
print(people["Arasuka"])  // >> null
```