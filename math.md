---
title: Math
date: 2020-04-28
slug: math
---

This library provides basic mathematical functions.

### math_abs
Returns the absolute, or non-negative value, of a given value.

```javascript
>>> math_abs(-100);
100
```

### math_acos
Returns the inverse cosine in radians of the given value.

```javascript
>>> math_acos(1);
0
>>> math_acos(0);
1.5708
```

### math_asin
Returns the inverse sine in radians of the given value.

```javascript
>>> math_asin(0);
0
>>> math_asin(1);
90
```

### math_atan
Returns the inverse tangent in radians.

```javascript
>>> var c = math_cos(0.8);
>>> var s = math_cos(0.8);
>>> math_atan(s/c);
45
```

### math_ceil
Returns the integer no greater than the given value (even for negatives).

```javascript
>>> math_ceil(0.5);
1
>>> math_ceil(-0.5);
-0
```

### math_cos
Return the cosine value for the given value in radians.

```javascript
>>> math_cos(math_pi() / 4);
0.999906
```

### math_floor
Returns the integer no less than the given value (even for negatives).

```javascript
>>> math_floor(0.5);
0
>>> math_floor(-0.5);
-1
```

### math_max
Return the maximum value from a variable length list of arguments.

```javascript
>>> math_max(1.2, -7, 3);
3
>>> math_max(1.2, 7, 3);
7
```

### math_pi
Returns a part of the constant Pi.

```javascript
>>> math_pi();
3.14159
```