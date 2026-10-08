# Array-Based Stack in C

A simple implementation of a stack data structure in C using a fixed-size array. Written for class research to demonstrate how stack operations work.

## What is a Stack?

A stack is a linear data structure that follows the **LIFO** principle: **Last In, First Out**. The last element added is the first one removed, like a pile of plates.

## How It Works

| Part | Purpose |
|------|---------|
| `box[MAX]` | Array that stores the stack elements |
| `MAX` | Maximum capacity of the stack (6) |
| `top` | Index of the top element. `-1` means the stack is empty |

## Operations

### `push(int x)`
Adds a value to the top of the stack.
- **Overflow check:** if `top == MAX - 1`, the stack is full and nothing is added.
- Otherwise, `top` is incremented and `x` is stored at `box[top]`.

### `pop()`
Removes the value at the top of the stack.
- **Underflow check:** if `top == -1`, the stack is empty and nothing is removed.
- Otherwise, the value at `box[top]` is returned and `top` is decremented.

## Time Complexity

| Operation | Complexity |
|-----------|-----------|
| push | O(1) |
| pop | O(1) |

## Example Run

`main()` pushes 10 to 60, tries a 7th push (overflow), pops everything, then tries one more pop (underflow).

```
Value 10 has been added
Value 20 has been added
Value 30 has been added
Value 40 has been added
Value 50 has been added
Value 60 has been added
Stack is Full!!
60 has been removed
50 has been removed
40 has been removed
30 has been removed
20 has been removed
10 has been removed
Stack is Empty!!
```

## Compile and Run

```
gcc stack.c -o stack
./stack
```

## Limitations

- Fixed capacity (`MAX`), so it cannot grow at runtime.
- Uses global variables, so only one stack exists per program.
- A linked-list implementation would remov
e the size limit.
