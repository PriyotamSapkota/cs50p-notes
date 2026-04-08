

# CS50P — Week 0: Functions & Variables

> Notes written while following along with CS50P lectures.
> Formatted and cleaned up after each session.

## Core Built-in Functions
- `print()` → displays output to screen (side effect)
- `input()` → takes user input, always returns a **string**

```python
name = input("What's your name? ").strip().title()
print(f"hello, {name}")
```

## Key Concepts
- `=` assignment, `==` comparison
- f-strings: `f"hello, {name}"` — cleaner than concatenation
- Chain string methods: `.strip().title()`
- `int()`, `float()` — convert string input to numbers
- Decimals: `round(x, 2)` or `f"{z:.2f}"`

## User-Defined Functions
```python
def hello(to="World"):
    print(f"hello, {to}")
```
- Define before calling, or use `main()` convention
- `return` sends value back — without it you get `None`
- **Scope** — variable only exists where it was defined

## main() Convention
```python
def main():
    name = input("What's your name? ").strip().title()
    hello(name)

def hello(to="World"):
    print(f"hello, {to}")

main()
```
- Keeps code organized
- Lets you define functions in any order

## Linux/Terminal Commands
- `ls` — list files in current folder
- `cd` — change directory
- `mkdir` — make new folder
- `mv` — move or rename a file
- `cp` — copy a file
- `rm` — remove a file
- `clear` — clear terminal window


