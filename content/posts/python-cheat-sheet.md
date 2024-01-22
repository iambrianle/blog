---
Title: Here is the Best Beginner-Friendly Python Cheatsheet (2022)
Description: In this post, I'll show you everything you need to know to code in Python and score high on basic Python tests.
Date: 2022-08-26T14:35:50+08:00
Draft: false
Tags: ["guide", "python"]
Categories: ["coding"]
Showtoc: true
Author: "Brian Le"

---

# Basic Python

In this post, I'll show you everything you need to know to start coding in Python and score high on basic Python tests I wish I had 4 years ago. Let's dive right in!

## Comments

Inline comment:

```python
# This is a comment
```

Multiline comment:

```python
# This is a
# multiline comment
```

Code with a comment:

```python
a = 1  # Initialization
```

Please note the two spaces in front of the comment.

## Math Operators

From **highest** to **lowest** precedence:

| Operators | Operation         | Example         |
| --------- | ----------------- | --------------- |
| \*\*      | Exponent          | `2 ** 3 = 8`    |
| %         | Modulus/Remainder | `22 % 8 = 6`    |
| //        | Integer Division  | `22 // 8 = 2`   |
| /         | Division          | `22 / 8 = 2.75` |
| \*        | Multiplication    | `3 * 3 = 9`     |
| -         | Subtraction       | `5 - 2 = 3`     |
| +         | Addition          | `2 + 2 = 4`     |

Examples of expressions:

```python
>>> 2 + 3 * 6
# 20

>>> (2 + 3) * 6
# 30

>>> 2 ** 8
#256

>>> 23 // 7
# 3

>>> 23 % 7
# 2

>>> (5 - 1) * ((7 + 1) / (3 - 1))
# 16.0
```

## Data Types

| Data Type              | Examples                                  |
| ---------------------- | ----------------------------------------- |
| Integers               | `-2, -1, 0, 1, 2, 3, 4, 5`                |
| Floating-Point Numbers | `-1.25, -1.0, -0.5, 0.0, 0.5, 1.0, 1.25` |
| Strings                | `'a', 'aa', 'aaa', 'hello!', '11 cats', '123'`   |

Important: Note that '123' is still a string.

## Variables

You can name a variable anything as long as it obeys the following rules:

1. It can be only one word.

```python
>>> # Bad
>>> my_variable = 'hello'

>>> # Good
>>> var = 'hello'
```

2. It can use only letters, numbers, and the underscore (`_`) character.

```python
>>> # Bad
>>> %$@variable = 'hello'

>>> # Good
>>> my_var = 'hello'

>>> # Good
>>> my_var_2 = 'hello'
```

3. It can't begin with a number.

```python
>>> # This won't work
>>> 23_var = 'hello'
```

4. Variable names starting with an underscore (`_`) are considered as "unuseful".

```python
>>> # _spam should not be used again in the code
>>> _spam = 'hello'
```

## The `print()` Function

1. The `print()` function writes the value of the argument(s) it is given. It handles multiple arguments, floating-point numbers, integers, and strings. Strings are printed without quotes, and a space is inserted when items are separated by a comma:

```python
>>> print('hello world!')
# Output: hello world!

>>> a = 1
>>> print('hello world!', a)
# Output: hello world! 1

```

2. Concatenate items
```python
>>> # Good
>>> a = 'joe' 
>>> print('hello world!' + a)
# Output: hello world!joe

>>> # Bad
>>> a = 1  # Integer(int)
>>> print('hello world!' + a)  # String(str) + Integer(int)
# TypeError: can only concatenate str (not "int") to str
```


## The `input()` Function

This function takes the input from the user and converts it into a string:

```python
>>> print('What is your name?')   # Ask for their name
>>> my_name = input()
>>> print('Hi', my_name)
# What is your name?
# Martha
# Hi, Martha
```

`input()` can also set a default message without using `print()`:

```python
>>> my_name = input('What is your name? ')  # Default message
>>> print('Hi', my_name)
# What is your name? Martha
# Hi, Martha
```

## The `str()`, `int()`, and `float()` Functions

These functions allow you to change the type of a variable. For example, you can transform an `integer` or `float` to a `string`:

```python
>>> str(29) # str
# '29'

>>> str(-3.14) # str
# '-3.14'
```

Or from a `string` to an `integer` or `float`:

```python
>>> int('11') # Integer
# 11

>>> float('3.14') # Decimal
# 3.14
```

## Conditions

To do this in Python, you use the `if`, `else`, and `elif` keywords. These two keywords are called conditionals.

1. Use the `if` keyword in Python

```python
>>> if condition:
...     Indented block of decision to make if condition is true

>>> # Example
>>> team_brian = 99
>>> team_jack = 59
>>> if team_brian > team_jack:
...     print("Team Brian won the league") # Output: Team Brian won the league
```

Important: If the condition in the `if` statement is not met, nothing happens.

```python
>>> team_brian = 59
>>> team_jack = 99
>>> if team_brian > team_jack:
...     print("Team Brian won the league")
        # Output: Nothing will output because if statement is not met
```

2. Use the `else` keyword in Python.

Since nothing happens if the condition in an if statement is not met, you can catch that with an `else` statement.

```python
>>> if condition:
...     Indented block of decision to make if condition is true
... else:
...     Indented block of decision to make if condition is not true


>>> # Example
>>> team_brian = 59
>>> team_jack = 99
>>> if team_brian > team_jack:
...     print("Team Brian won the league")
... else:
...     print("Team Jack won the league")
        # Output: Team Jack won the league
```

3. Use the `elif` keyword in Python

Another conditional keyword in Python is `elif`, which you can put in between an `if` and `else`. `elif` is more specific than `else`.

```python
>>> # Example
>>> team_brian = 59
>>> team_jack = 89
>>> team_lilian = 99
>>> if team_brian > team_jack:
...     print("Team Brian won the league")
... elif team_lilian > team_brian:
...     print("Team Lilian won the league")
... else:
...     print("Team Jack won the league")
        # Output: Team Lilian won the league
```

## Import

Basically, `import` allows you to use pre-written code of someone else who already wrote the code and is willing to share it.


This code would have to be written if the random module was not used

```python
# This code doesn't work as it is only a small portion of the random module 

def randrange(self, start, stop=none, step=_one):
    """Choose a random item from range(stop) or range(start, stop[, step]).
    Roughly equivalent to `choice(range(start, stop, step))` but
    supports arbitrarily large ranges and is optimized for common cases.
    """

    # This code is a bit messy to make it fast for the
    # Common case while still doing adequate error checking.
    istart = _index(start)
    if stop is none:
        # We don't check for "step != 1" because it hasn't been
        # Type checked and converted to an integer yet.
        if step is not _one:
            raise TypeError("Missing a non-None stop argument")
        if istart > 0:
            return self._randbelow(istart)
        raise ValueError("Empty range for randrange()")

    # Stop argument supplied.
    istop = _index(stop)
    width = istop - istart
    istep = _index(step)
    # Fast path.
    if istep == 1:
        if width > 0:
            return istart + self._randbelow(width)
        raise ValueError(f"Empty range in randrange({start}, {stop})")

        # Non-unit step argument supplied.
        if istep > 0:
            n = (width + istep - 1) // istep
        elif istep < 0:
            n = (width + istep + 1) // istep
        else:
            raise ValueError("Zero step for randrange()")
        if n <= 0:
            raise ValueError(f"Empty range in randrange({start}, {stop}, {step})")
        return istart + istep * self._randbelow(n)


def randint(self, a, b):
        """Return random integer in range [a, b], including both end points.
        """

        return self.randrange(a, b+1)

random = random.randint(1,100) # Generate random number between 1 and 100
print(random)

```

But if the random module was used, it will be much easier and more efficient to write your code.
```python
import random
random = random.randint(1,100) # Generate random number between 1 and 100
print(random)
```

## While Loop Statements

The while statement is used for repeated execution as long as an expression is `True`:

```python
>>> spam = 0
>>> while spam < 5:
...     print('Brian')
...     spam = spam + 1
...
# Output:
# Brian
# Brian
# Brian
# Brian
# Brian
```

## Break Statements

If the execution reaches a `break` statement, it immediately exits the `while` loop’s clause:

```python
>>> while True: # Infinite loop
...     name = input('Please type your name: ')
...     if name == 'your name':
...         break
...
>>> print('Thank you!')
# Please type your name: your name
# Thank you!
```

## Continue Statements

When the program execution reaches a `continue` statement, the program execution immediately jumps back to the start of the loop.

```python
>>> while True:
...     name = input('Who are you? ')
...     if name != 'Joe':
...         continue
...     password = input('Password? (It is a fish.): ')
...     if password == 'swordfish':
...         break
...
>>> print('Access granted.')
# Who are you? Charles
# Who are you? Debora
# Who are you? Joe
# Password? (It is a fish.): swordfish
# Access granted.
```


## Cool Things to Know

### Concatenation and Replication

String concatenation:

```python
>>> 'Alice' 'Bob'
# 'AliceBob'
```

String replication:

```python
>>> 'Alice' * 5
# 'AliceAliceAliceAliceAlice'
```

### The `end` Keyword

The keyword argument `end` can be used to avoid the newline after the output or end the output with a different string:

```python
phrase = ['Printed', 'with', 'a', 'dash', 'in', 'between']
>>> for word in phrase:
...     print(word, end='-')
...
# Printed-with-a-dash-in-between-
```

### The `sep` Keyword

The keyword `sep` specifies how to separate the objects if there is more than one:

```python
print('Jack', 'Lilian', 'Charlotte', sep=',')
# Jack,Lilian,Charlotte
```



# Conclusion

### Now I'd Like to Hear From You:
- How did you think of my cheat sheet?
- What is your favorite thing about Python?

Comment below to let me know!

## Next Step
Visit [my blog](https://notbrian.me/) next week where I will dive deep into Python!

## Source
Summarized from the [Python 3 tutorial](https://docs.python.org/3/tutorial/index.html).