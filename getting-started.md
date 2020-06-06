# Getting Started

## What is Ghost

Ghost is a small, class-based scripting language. Currently we have a subset of the language developed in C utilizing a bytecode virtual machine. We are currently re-writing this within Go and plan on archiving the C variant once it's caught up.

## Installing Ghost
If you're on a Unix or Mac machine, running the following in your terminal will quickly get you started:

```bash
git clone https://github.com/ghost-language/cghost
cd ghost
make
./ghost
```

This downloads and builds the latest `master` version of Ghost (written in C) found on GitHub. You will find a `ghost` executable at the root of this directory if everything was successful.

## Interactive Mode
If you just run `ghost` without any arguments, it starts the interpreter in interactive mode (aka, REPL mode, _read-eval-print loop_). You can type in a line of code, and immediately execute it. While in this mode, your state is saved until you exit the program. Meaning if you define a variable, you may reference the variable later on.

Ready to give Ghost a spin?

```javascript
print("Hello, world!");
```

Once you have Ghost setup and installed, you're ready to jump into [learning the language](/docs/{{version}}/syntax).