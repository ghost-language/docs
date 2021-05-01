---
title: Math
---

This library provides basic mathematical functions.

### Math.abs
Returns the absolute, or non-negative value, of a given value.

```dart
>> Math.abs(-100)
   100
```

### Math.cos
Returns the cosine of the radian value.

```dart
>> Math.cos(1).round(4)
   0.5403
>> Math.cos(0).round(4)
   1
```

### Math.pi
Returns a part of the constant Pi.

```dart
>> Math.pi()
   3.14159265358979323846264338327950288419716939937510582097494459
>> Math.pi().round(2)
   3.14
```

### Math.random
Returns a floating-point, pseudo-random number between `0` and `1`, or the defined `min` and `max` values.

```dart
>> Math.random()
   0.5924415937528662
>> Math.random(5, 10)
   5.527250192202932
>> Math.random(0, 100).round()
   81
```