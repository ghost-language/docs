---
title: Strings
---

Strings are useful for holding data that can be represented in text form. Strings may contain any valid Unicode character, including emojis.

### Creating Strings
Strings are created using either single or double quotes.

```dart
string1 := "A string value"
string2 := 'This is also a string value'
```

### Comparing Strings
Strings can be compared against each other using the `==` operator. This will compare strings in a case-sensitive manner.

```dart
string1 := "a"
string2 := "b"

// false
result := string1 == string2
```

### Long Strings
Sometimes, your code will include strings which are very long. Rather than having lines that go on endlessly, or wrap at the whim of your editor, you may wish to specifically break the string into multiple lines in the source code without affecting the actual string contents.

You can achieve this using the `+` operator to append multiple strings together, like this:

```
longString := "This is a very long string which needs " +
              "to wrap across multiple lines because " +
              "otherwise the code will be unreadable."
```

## String Methods

### `String.endsWith(searchString)`
Determines whether the calling string ends with the characters of string `searchString`.

### `String.length()`
Returns the length of the string.

### `String.split(separator)`
Returns a list of strings populated by splitting the calling string at occurrences of the substring `separator`.

### `String.startsWith(searchString)`
Determines whether the calling string starts with the characters of string `searchString`.

### `String.toLowerCase()`
Returns the string value converted to lowercase.

### `String.toString()`
Returns the string value as a string.

### `String.toUpperCase()`
Returns the string value converted to uppercase.

### `String.trim()`
Trims whitespace from the beginning and end of the string.

### `String.trimEnd()`
Trims whitespace from the end of the string.

### `String.trimStart()`
Trims whitespace from the beginning of the string.