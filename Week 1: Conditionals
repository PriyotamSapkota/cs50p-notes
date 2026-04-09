# CS50P — Week 1: Conditionals

> Notes written while following along with CS50P lectures.
> Formatted and cleaned up after each session.

## Comparison Operators
- `>` greater than
- `>=` greater than or equal to
- `<` less than
- `<=` less than or equal to
- `==` equality (comparison)
- `!=` not equal to
- `=` is assignment, not comparison

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
- Once a true condition is found, the rest are skipped
- Indentation is required — Python uses it instead of `{}` like C or JavaScript
- Colon `:` is required after every condition

## and / or
```python
if x < y or x > y:
    print("x is not equal to y")

if x != y:           # cleaner version of above
    print("x is not equal to y")
```

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

## Parity (Even or Odd)
```python
def main():
    x = int(input("What's x? "))
    if is_even(x):
        print("Even")
    else:
        print("Odd")

def is_even(n):
    return n % 2 == 0       # most pythonic version

main()
```
- `%` is modulo — returns remainder after division
- `n % 2 == 0` is itself a Boolean, so no need for `if/else` inside the function

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
- `|` means or inside a case
- `case _` is the default (same as `else`)
