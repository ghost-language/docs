---
title: Lists
---

Lists are an ordered list of elements of possibly different types identified by a number index. Each element in a list can be accessed individually by their index. Lists are constructed as a comma separated list of elements, can contain any type of value, and are enclosed by square brackets:

```dart
[
    "Ghost",
    57.3,
    function(x) { x * x}
]
```

## Accessing Elements
You can access any element in a list by calling the subscript operator on it with the index of the element you want. Like most languages, indices start at zero:

```dart
vocabulary := ["activation", "propogate", "execute", "initialize"]

print(vocabulary[0])  // >> activation
print(vocabulary[1])  // >> propogate
print(vocabulary[2])  // >> execute
print(vocabulary[3])  // >> initialize
```

## List Methods

### `List.first()`
Returns the first element of the list.

### `List.join(separator)`
Joins all elements of the list into a string, using `separator` to join the elements together.

### `List.last()`
Returns the last element of the list.

### `List.length()`
Returns the number of elements in the list.

### `List.push(element)`
Adds one new `element` to the end of the list and returns the new length.

### `List.tail()`
Returns a new list containing all elements but the first.

### `List.toString()`
Returns a string representing the list and its elements.

## Examples

### Creating A List
The following example creates a new list, `messageList`, with a length of `0`, then assigns values to index `0` and `99`, changing the length of the list to `100`.

```dart
messageList := []
messageList[0] := 'Hello'
messageList[99] := 'World'

if (messageList.length() == 100) {
    print('The length of the list is 100.')
}
```

### Creating A Two-Dimensional List
The following creates a chessboard as a two-dimensional list of strings. The first move is made by copying the `'p'` in `board[6][4]` to `board[4][4]`. The old position at `[6][4]` is made blank.

```dart
function renderBoard(board) {
    for (row := 0; row <= board.length() - 1; row := row + 1) {
        print(board[row])
    }

    print()
}

board := [
    ['R', 'N', 'B', 'Q', 'K', 'B', 'N', 'R'],
    ['P', 'P', 'P', 'P', 'P', 'P', 'P', 'P'],
    [' ', ' ', ' ', ' ', ' ', ' ', ' ', ' '],
    [' ', ' ', ' ', ' ', ' ', ' ', ' ', ' '],
    [' ', ' ', ' ', ' ', ' ', ' ', ' ', ' '],
    [' ', ' ', ' ', ' ', ' ', ' ', ' ', ' '],
    ['p', 'p', 'p', 'p', 'p', 'p', 'p', 'p'],
    ['r', 'n', 'b', 'q', 'k', 'b', 'n', 'r']
]

renderBoard(board)

// Move King's Pawn forward 2
board[4][4] := board[6][4]
board[6][4] := ' '

renderBoard(board)
```

Here is the output:

```
[R, N, B, Q, K, B, N, R]
[P, P, P, P, P, P, P, P]
[ ,  ,  ,  ,  ,  ,  ,  ]
[ ,  ,  ,  ,  ,  ,  ,  ]
[ ,  ,  ,  ,  ,  ,  ,  ]
[ ,  ,  ,  ,  ,  ,  ,  ]
[p, p, p, p, p, p, p, p]
[r, n, b, q, k, b, n, r]

[R, N, B, Q, K, B, N, R]
[P, P, P, P, P, P, P, P]
[ ,  ,  ,  ,  ,  ,  ,  ]
[ ,  ,  ,  ,  ,  ,  ,  ]
[ ,  ,  ,  , p,  ,  ,  ]
[ ,  ,  ,  ,  ,  ,  ,  ]
[p, p, p, p,  , p, p, p]
[r, n, b, q, k, b, n, r]
```