---
title: Syntax
date: 2020-04-28
slug: syntax
---

Ghost's syntax pulls a lot of influence from other C-like languages. In particular PHP, JavaScript, and Dart. It's designed to be familiar to those coming from these languages, with the aim to simple and predictable.

Scripts are stored in plain text files with a `.ghost` file extension. Ghost does not compile ahead of time: programs are run directly from source, from top to bottom like any other scripting language.

## Comments
Line comments start with `//` and continue to the end of the line.

```javascript
// This is a comment
```

Comments behave like whitespace and are discarded during execution.

## Reserved Words
Ghost has a small subset of reserved words used as predefined identifiers. None of the identifiers listed here should be used as identifiers in any of your scripts.

```
else false for if null return true var while
```

## Identifiers
Naming rules are similar to other programming languages. Identifiers must start with a letter or underscore and may then contain letters, digits, and underscores. Case is sensitive.

```
hello
camelCase
PascalCase
_under_score
abc123
ALL_CAPS
```

## Blocks
Ghost uses curly braces to define _blocks_. You can use a block anywhere a statement is allowed, like in control flow statements.

```javascript
{
    print("One statement.");
    print("Two statements.");
}
```