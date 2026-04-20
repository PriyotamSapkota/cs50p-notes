# CS50P — Week 1: Conditionals
> Notes written while following along with CS50P lectures.
> Formatted and cleaned up after each session.

## What I Built
- **Deep Thought** — 
- **Home Federal Savings Bank** — 
- **File Extensions** — 
- **Math Interpreter** — 
- **Meal Time** — 

## Comparison Operators
- `>` greater than
- `>=` greater than or equal to
- `<` less than
- `<=` less than or equal to
- `==` equality (comparison)
- `!=` not equal to
- `=` is assignment, not comparison

## Boolean Expressions
- A **Boolean expression** is any expression that evaluates to `True` or `False`
- Same concept from mathematics — yes or no, true or false
- Every condition inside `if`, `elif` is a Boolean expression

## if / elif / else
```python
x = int(input("What's x? "))
y = int(input("What's y? "))

if x < y:
    print("x is less than y")
elif x > y:
    print("x is greater than y")
else:
    print("x is equal to y")
```
- `if` — asks the first question
- `elif` — only asked if previous condition was false
- `else` — catches everything remaining, no question needed
- Once a true condition is found, the rest are skipped — **mutually exclusive**
- Indentation is required — Python uses it instead of `{}` like C or JavaScript
- Colon `:` is required after every condition

### Why elif over multiple ifs?
- Using all `if` instead of `elif` means every condition is checked every time
- With `elif`, Python stops as soon as it finds a true condition — fewer questions, more efficient
- Doesn't feel faster on small code but matters a lot in larger programs

## and / or
```python
if x < y or x > y:
    print("x is not equal to y")

if x != y:           # cleaner version of above
    print("x is not equal to y")
```
- `or` — true if at least one condition is true
- `and` — true only if both conditions are true

## Grade Example (clean version)
```python
score = int(input("Score: "))

if score >= 90:
    print("Grade: A")
elif score >= 80:
    print("Grade: B")
elif score >= 70:
    print("Grade: C")
elif score >= 60:
    print("Grade: D")
else:
    print("Grade: F")
```
- Once a condition matches, Python stops checking — no need to write `and score < 90`
- You can also write `90 <= score <= 100` — Python supports chained comparisons unlike most languages

## Parity (Even or Odd)
- `%` is **modulo** — returns the remainder after division
- `10 % 2 == 0` → even, `11 % 2 == 1` → odd

### Three versions — from basic to Pythonic

**Version 1 — explicit if/else:**
```python
def is_even(n):
    if n % 2 == 0:
        return True
    else:
        return False
```

**Version 2 — ternary expression:**
```python
def is_even(n):
    return True if n % 2 == 0 else False
```

**Version 3 — most Pythonic:**
```python
def is_even(n):
    return n % 2 == 0
```
- `n % 2 == 0` is itself a Boolean expression — no need for `if/else` inside the function
- **Pythonic** means writing code in the way Python is designed to be written — clean, readable, close to plain English

```python
def main():
    x = int(input("What's x? "))
    if is_even(x):
        print("Even")
    else:
        print("Odd")

def is_even(n):
    return n % 2 == 0

main()
```

## match (like switch in other languages)
```python
name = input("What's your name? ")

match name:
    case "Harry" | "Hermione" | "Ron":
        print("Gryffindor")
    case "Draco":
        print("Slytherin")
    case _:
        print("Who?")
```
- `match` is cleaner than long `if/elif` chains when comparing one variable to many values
- `|` means or inside a case — groups multiple values with the same output
- `case _` is the default (same as `else`)
- More powerful than a basic `if/elif` chain for pattern matching
