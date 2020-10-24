---
title: Getting Started
---

## What is Ghost
Ghost is a small, (soon to be) class-based scripting language.

## Installing Ghost

### Brew
If you're on Mac, you may use `homebrew`:

```
$ brew tap ghost-language/ghost
$ brew install ghost-language/ghost/ghost
```

### Go Install
If you have Go installed, you may use `go install`:

```
$ go install github.com/ghost-language/ghost
```

### Direct Download
You may download the compiled binaries for your platform from our GitHub [releases](https://github.com/ghost-language/ghost/releases) page.

## Building Ghost
If you're on a Unix or Mac machine, you can easily download the source code and build directly:

```bash
git clone https://github.com/ghost-language/ghost
cd ghost
make
```

This downloads and builds the latest `nightly` version of Ghost found on GitHub. You will be put inside a fresh instance of `ghost` if everything was successful.

## Interactive Mode
If you just run `ghost` without any arguments, it starts the interpreter in interactive mode (aka, REPL mode, _read-eval-print loop_). You can type in a line of code, and immediately execute it. While in this mode, your state is saved until you exit the program. Meaning if you define a variable, you may reference the variable later on.

Ready to give Ghost a spin?

```javascript
print("Hello, world!")
```

Once you have Ghost setup and installed, you're ready to jump into [learning the language](/docs/{{version}}/syntax).