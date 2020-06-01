---
title: Getting Started
date: 2020-04-28
slug: getting-started
---

## What is Ghost

Ghost is a small, class-based toy scripting language. The foundations of the language were developed by going through the excellent [Crafting Interpreters](https://craftinginterpreters.com/) book by [Bob Nystron](http://journal.stuffwithstuff.com/). The bytecode virtual machine powering Ghost is written in C and can be found on GitHub under the MIT license.

## Installing Ghost
If you're on a Unix or Mac machine, running the following in your terminal will quickly get you started:

```bash
git clone https://github.com/axiom-labs/ghost
cd ghost
make
./ghost
```

This downloads and builds the latest `master` version of Ghost found on GitHub. You will find a `ghost` executable at the root of this directory if everything was successful.

## Interactive Mode
If you just run `ghost` without any arguments, it starts the interpreter in interactive mode (aka, REPL mode, _read-eval-print loop_). You can type in a line of code, and immediately execute it. While in this mode, your state is saved until you exit the program. Meaning if you define a variable, you may reference the variable later on.

Ready to give Ghost a spin?

```javascript
print("Hello, world!");
```
