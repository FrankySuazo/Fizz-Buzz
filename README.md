# Fizz-Buzz
# FizzBuzz 🐝

A simple Python implementation of the classic **FizzBuzz** programming challenge.

This project prints the numbers from **1 to 100**, but replaces certain numbers based on their divisibility:

- Multiples of **3** print `Fizz`
- Multiples of **5** print `Buzz`
- Multiples of **both 3 and 5** print `FizzBuzz`
- All other numbers print normally

## How It Works

The program uses a `for` loop with Python's `range()` function to iterate through the numbers 1–100.

```python
for number in range(1, 101):
```

Because the stopping value in `range()` is **not included**, `101` is used so that `100` is included in the loop.

For each number, the program uses conditional statements to determine what should be printed.

The modulo operator `%` is used to check whether a number is evenly divisible by another number.

For example:

```python
number % 3 == 0
```

means that dividing `number` by `3` leaves no remainder, so the number is a multiple of 3.

## Logic

The order of the conditions is important.

The program first checks whether the number is divisible by **both 3 and 5**:

```python
if number % 3 == 0 and number % 5 == 0:
    print("FizzBuzz")
```

This condition must come first because a number such as `15` is also individually divisible by both `3` and `5`.

The remaining conditions check for multiples of 3 and 5:

```python
elif number % 3 == 0:
    print("Fizz")
elif number % 5 == 0:
    print("Buzz")
else:
    print(number)
```

If none of the conditions are true, the original number is printed.

## Example Output

```text
1
2
Fizz
4
Buzz
Fizz
7
8
Fizz
Buzz
11
Fizz
13
14
FizzBuzz
```

The pattern continues until the program reaches `100`.

## What I Learned

This project helped reinforce several Python fundamentals:

- Using `for` loops to repeat code over a sequence
- Using `range(start, stop)` and understanding that the stop value is excluded
- Using `%` (modulo) to determine whether numbers are evenly divisible
- Combining multiple Boolean conditions with `and`
- Using `if`, `elif`, and `else` to control program behavior
- Understanding why the **order of conditional statements matters**

One of the most important lessons was recognizing that the `FizzBuzz` condition must be checked before the individual `Fizz` and `Buzz` conditions.

For example, `15` satisfies all three of these tests:

```python
15 % 3 == 0
15 % 5 == 0
15 % 3 == 0 and 15 % 5 == 0
```

If the program checks divisibility by 3 first, it would print `Fizz` and never reach the `FizzBuzz` condition. Checking the most specific condition first prevents that problem.

## Concepts Practiced

`Python` · `for loops` · `range()` · `modulo (%)` · `if/elif/else` · `Boolean logic` · `and`

## Running the Program

Make sure Python is installed, then run:

```bash
python fizz_buzz.py
```
