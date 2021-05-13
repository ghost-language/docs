---
title: Method Calls
---

Ghost is deeply object oriented, so most code consists of invoking methods on objects, usually something like this:

```dart
dog.speak("Throw the ball!");
```

You have a _receiver_ expression (here `dog`) followed by a `.`, then a name (`speak`) and an argument list in parentheses (`("Throw the ball!")`). Multiple arguments are separated by commas:

```dart
dog.command("fetch", "ball");
```

The argument list can also be empty:

```dart
dog.sit();
```

Ghost executes a method call like so:

1. Evaluate the receiver and arguments from left to right.
2. Look up the method on the receiver's object.
3. Invoke it, passing in the argument values.