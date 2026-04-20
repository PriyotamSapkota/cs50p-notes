# CS50P — Week 0: Functions & Variables
> Notes written while following along with CS50P lectures.
> Formatted and cleaned up after each session.

## What I Built
- **Einstein** — asked user to enter mass in kg and calculated energy in joules using E=mc², where c = speed of light in vacuum = 3 × 10⁸ m/s
- **Tip Calculator** — built a calculator for restaurants that asks the user to enter the cost of meal and tip percentage, then calculates and displays the tip amount

## Core Built-in Functions
- `print()` → displays output to screen (side effect)
- `input()` → takes user input, always returns a **string**

```python
name = input("What's your name? ").strip().title()
print(f"hello, {name}")
```

## Key Concepts
- `=` assignment, `==` equality (comparison)
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

### Return Values
- Use `return` to store a value for further use instead of just printing — printed values can't be used in calculations
- `return` ends the function immediately; any code after it won't run
- If you need both, put `print()` **before** `return`
- A function can produce two kinds of output:
  - **Return value** — a value passed back to the caller
  - **Side effect** — anything that changes outside the function (e.g. printing to screen)

### Variable Scope
- **Global variables** can be accessed anywhere in the program
- **Local variables** only exist inside the function they're defined in
- To modify a global variable inside a function, declare it with the `global` keyword:

```python
counter = 0

def increment():
    global counter
    counter += 1
```

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
