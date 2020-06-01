---
title: Operators
date: 2020-05-02
slug: operators
---

An operator is something that takes one or more values (or expressions) and yields another value (so that the construction itself becomes an expression)

Operators can be grouped according to the number of values they take. Unary operators take only one value, for example `!` (the logical not operator). Binary operators take two values, such as the familiar arithmetical operators `+` (plus) and `-` (minus). The majority of Ghost's operators fall into this category.

## Precedence and Associativity
The precedence of an operator specifies how "tightly" it binds two expressions together. For example, in the expression `1 + 5 * 3`, the answer is `16` and not `18` because the multiplication (`*`) operator has a higher precedence than the addition (`+`) operator. Parentheses may be used to force precedence, if necessary. For example, `(1 + 5) * 3` evaluates to `18`.

When operators have equal precedence their associativity decides how the operators are grouped. For example, `=` is left-associative, so `1 - 2 - 3` is grouped as `(1 - 2) - 3` and evaluates to `-4`. `=` on the other hand is right-associative, so `a = b = c` is grouped as `a = (b = c)`.

Use of parentheses, even when not strictly necessary, can often increase readability of the code by making grouping explicit rather than relying on the implicit operator precedence and associativity.

The following table summarizes the operator precedence in Ghost, from highest to lowest. Operators in the same box have the same precedence.

| Precedence | Operator | Description | Associates |
|------------|----------|-------------|------------|
| 1 | `()` `.` | Grouping, Method call | Left |
| 2 | `-` | Negate | Right |
| 3 | `*` `/` `%` | Multiply, Divide, Modulo | Left |
| 4 | `+` `-` | Add, Subtract | Left |
| 5 | `<` `<=` `>` `>=` | Comparison | Left |
| 6 | `==` `!=` | Equals, Not equal | Left |
| 7 | `and` | Logical and | Left |
| 8 | `or` | Logical or | Left |
| 9 | `=` | Assignment | Right |

## Arithmetic Operators
Remember basic arithmetic from school? These work just like those.

| Example | Name | Result |
|---------|------|--------|
| `-a` | Negation | Opposite of `a`. |
| `a + b` | Addition | Sum of `a` and `b`. |
| `a - b` | Subtraction | Difference of `a` and `b`. |
| `a * b` | Multiplication | Product of `a` and `b`. |
| `a / b` | Division | Quotient of `a` and `b`. |
| `a % b` | Modulo | Remainder of `a` divided by `b`. |

The result of the modulo operator (`%`) has the same sign as the dividend - that is, the result of `a % b` will have the same sign as `a`. For example:

```javascript
print(5 % 3);    // Prints 2
print(5 % -3);   // Prints 2
print(-5 % 3);   // Prints -2
print(-5 % -3);  // Prints -2
```

## Assignment Operator
The basic assignment operator is `=`. This is NOT the same as "equal to". It means that the left operand gets set to the value of the expression on the right.

```javascript
var a = (5 + 10);

print(a);  // Prints 15
```

## Comparison Operators
Comparison operators, as their name implies, allow you to compare two values.

| Example | Name | Result |
|---------|------|--------|
| `a == b` | Equal | `true` if `a` is equal to `b`. |
| `a != b` | Not equal | `true` if `a` is not equal to `b`. |
| `a < b` | Less than | `true` if `a` is less than `b`. |
| `a > b` | Greater than | `true` if `a` is greater than `b`. |
| `a <= b` | Less than or equal to | `true` if `a` is less than or equal to `b`. |
| `a >= b` | Greater than or equal to | `true` if `a` is greater than or equal to `b`. |