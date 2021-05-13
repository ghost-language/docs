---
title: Modules
draft: true
---

As your program starts to grow, you'll want to start considering breaking up your code into multiple smaller and more manageable files. To achieve this, Ghost has a simple module system allowing you to import other files in a controlled manner. Furthermore, even your modules can import other modules in. This leads to extremely clean code that is easy to digest and maintain.

## Introducing An Example
To demonstrate the usage of modules, we're going to show a very simple example below.

### Basic Example Structure
In our example, we have the file structure below:

```
main.ghost
modules/
    functions.ghost
    variables.ghost
```

### `main.ghost`
```dart
function := import("modules/functions")
variable := import("modules/variables")

print("Program loaded.")

function.add(variable.one, variable.two)
function.greet(variable.hello)
```

### `functions.ghost`
```dart
function add(a, b) {
    print(a + b)
}

function greet(message) {
    print(message)
}
```

### `variables.ghost`
```dart
one := 1
two := 2
hello := "Hello, world!"
```

While this is a very rudimentary example, it showcases how simple it is to load in modules. Modules are nothing more than other Ghost files, and can be located anywhere within your program. We chose to put our modules in a `modules` directory, but you don't have to do this.