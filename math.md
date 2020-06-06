# Math

This library provides basic mathematical functions.

### Math.abs
Returns the absolute, or non-negative value, of a given value.

```javascript
>>> Math.abs(-100);
100
```

### Math.acos
Returns the inverse cosine in radians of the given value.

```javascript
>>> Math.acos(1);
0
>>> Math.acos(0);
1.5708
```

### Math.asin
Returns the inverse sine in radians of the given value.

```javascript
>>> Math.asin(0);
0
>>> Math.asin(1);
90
```

### Math.atan
Returns the inverse tangent in radians.

```javascript
>>> var c = Math.cos(0.8);
>>> var s = Math.cos(0.8);
>>> Math.atan(s/c);
45
```

### Math.ceil
Returns the integer no greater than the given value (even for negatives).

```javascript
>>> Math.ceil(0.5);
1
>>> Math.ceil(-0.5);
-0
```

### Math.cos
Return the cosine value for the given value in radians.

```javascript
>>> Math.cos(Math.pi() / 4);
0.999906
```

### Math.floor
Returns the integer no less than the given value (even for negatives).

```javascript
>>> Math.floor(0.5);
0
>>> Math.floor(-0.5);
-1
```

### Math.max
Return the maximum value from a variable length list of arguments.

```javascript
>>> Math.max(1.2, -7, 3);
3
>>> Math.max(1.2, 7, 3);
7
```

### Math.pi
Returns a part of the constant Pi.

```javascript
>>> Math.pi();
3.14159
```