---
title: python basics - python cheatsheet
description: the basics of python. we all need to start somewhere, so how about doing it here. this cheat sheet is designed on the year 8 wa digital technology curriculum
date: 2022-08-27t14:35:50+08:00
draft: false
# cover:
#     image: img/hi.jpg
#     alt: 'lol'
#     caption: 'hi'
tags: ["guide", "python", "blog"]
categories: ["coding"]
---

# python basics

we all need to start somewhere, so how about doing it here. this cheat sheet is designed on the year 8 wa digital technology curriculum

## math operators

from **highest** to **lowest** precedence:

| operators | operation         | example         |
| --------- | ----------------- | --------------- |
| \*\*      | exponent          | `2 ** 3 = 8`    |
| %         | modulus/remainder | `22 % 8 = 6`    |
| //        | integer division  | `22 // 8 = 2`   |
| /         | division          | `22 / 8 = 2.75` |
| \*        | multiplication    | `3 * 3 = 9`     |
| -         | subtraction       | `5 - 2 = 3`     |
| +         | addition          | `2 + 2 = 4`     |

examples of expressions:

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

## data types

| data type              | examples                                  |
| ---------------------- | ----------------------------------------- |
| integers               | `-2, -1, 0, 1, 2, 3, 4, 5`                |
| floating-point numbers | `-1.25, -1.0, --0.5, 0.0, 0.5, 1.0, 1.25` |
| strings                | `'a', 'aa', 'aaa', 'hello!', '11 cats'`   |

## the print() function

the `print()` function writes the value of the argument(s) it is given. [...] it handles multiple arguments, floating point-number, integer, and strings. strings are printed without quotes, and a space is inserted between items, so you can format things nicely:

```python
>>> print('hello world!')
# output: hello world!

>>> a = 1
>>> print('hello world!', a)
# output: hello world! 1
```

## variables

you can name a variable anything as long as it obeys the following rules:

1. it can be only one word.

```python
>>> # bad
>>> my variable = 'hello'

>>> # good
>>> var = 'hello'
```

2. it can use only letters, numbers, and the underscore (`_`) character.

```python
>>> # bad
>>> %$@variable = 'hello'

>>> # good
>>> my_var = 'hello'

>>> # good
>>> my_var_2 = 'hello'
```

3. it can’t begin with a number.

```python
>>> # this wont work
>>> 23_var = 'hello'
```

4. variable name starting with an underscore (`_`) are considered as "unuseful".

```python
>>> # _spam should not be used again in the code
>>> _spam = 'hello'
```

## comments

inline comment:

```python
# this is a comment
```

multiline comment:

```python
# this is a
# multiline comment
```

code with a comment:

```python
a = 1  # initialization
```

please note the two spaces in front of the comment.

## the input() function

this function takes the input from the user and converts it into a string:

```python
>>> print('what is your name?')   # ask for their name
>>> my_name = input()
>>> print('hi, {}'.format(my_name))
# what is your name?
# martha
# hi, martha
```

`input()` can also set a default message without using `print()`:

```python
>>> my_name = input('what is your name? ')  # default message
>>> print('hi, {}'.format(my_name))
# what is your name? martha
# hi, martha
```

## the str(), int(), and float() functions

these functions allow you to change the type of variable. for example, you can transform from an `integer` or `float` to a `string`:

```python
>>> str(29) # str
# '29'

>>> str(-3.14) # str
# '-3.14'
```

or from a `string` to an `integer` or `float`:

```python
>>> int('11') # integer
# 11

>>> float('3.14') # decimal
# 3.14
```

## conditions

to do this in python, you use the `if`, `else` and `elif` keywords. these two keywords are called conditionals.

1. use the `if` keyword in python

```python
>>> if(condition):
        indented block of decision to make if condition is true

>>> # example
>>> teambrian = 99
>>> teamjack = 59
>>> if(teambrian > teamjack):
        print("team brian won the league") # output: team brian won the league
```

important: if the condition in the `if`statement is not met, nothing happens.

```python
>>> teambrian = 59
>>> teamjack = 99
>>> if(teambrian > teamjack):
        print("team brian won the league")
        # output: nothing will output because if statement is not met
```

2. use the `else` keyword in python.

since nothing happens `if` the condition in an if statement is not met, you can catch that with an `else` statement.

```python
>>> if(condition):
        indented block of decision to make if condition is true
    else:
        indented block of decision to make if condition is not true


>>> # example
>>> teambrian = 59
>>> teamjack = 99
>>> if(teambrian > teamjack):
        print("team brian won the league")
    else:
        print("team jack won the league")
        # output: team jack won the league
```

3. use the `elif` keyword in python

another conditional keyword in python is `elif`, which you can put in between an `if` and `else`. `elif` is more specific then else

```python
>>> # example
>>> teambrian = 59
>>> teamjack = 89
>>> teamlilian = 99
>>> if(teambrian > teamjack):
        print("team brian won the league")
    elif(teamlilian > teambrian):
        print("team lilian won the league")
    else:
        print("team jack won the league")
        # output: team lilian won the league
```

## import

basically, `import` allows you to use pre-written code of someone else who already wrote the code and willing to share it.


this code would have to be written if the random module was not used

```python
# this code don't work as it is only a small portion of the random module 

def randrange(self, start, stop=none, step=_one):
    """choose a random item from range(stop) or range(start, stop[, step]).
    roughly equivalent to ``choice(range(start, stop, step))`` but
    supports arbitrarily large ranges and is optimized for common cases.
    """

    # this code is a bit messy to make it fast for the
    # common case while still doing adequate error checking.
    istart = _index(start)
    if stop is none:
        # we don't check for "step != 1" because it hasn't been
        # type checked and converted to an integer yet.
        if step is not _one:
            raise typeerror("missing a non-none stop argument")
        if istart > 0:
            return self._randbelow(istart)
        raise valueerror("empty range for randrange()")

    # stop argument supplied.
    istop = _index(stop)
    width = istop - istart
    istep = _index(step)
    # fast path.
    if istep == 1:
        if width > 0:
            return istart + self._randbelow(width)
        raise valueerror(f"empty rangein randrange({start}, {stop})")

        # non-unit step argument supplied.
        if istep > 0:
            n = (width + istep - 1) // istep
        elif istep < 0:
            n = (width + istep + 1) // istep
        else:
            raise valueerror("zero step for randrange()")
        if n <= 0:
            raise valueerror(f"empty range in randrange({start}, {stop}, {step})")
        return istart + istep * self._randbelow(n)


def randint(self, a, b):
        """return random integer in range [a, b], including both end points.
        """

        return self.randrange(a, b+1)

random = random.randint(1,100) #generate random number between 1 and 100
print(random)

```

but if the random module was used, it will be much easier and more efficient to write your code.
```python
import random
random = random.randint(1,100) #generate random number between 1 and 100
print(random)
```


## cool things to know

### concatenation and replication

string concatenation:

```python
>>> 'alice' 'bob'
# 'alicebob'
```

string replication:

```python
>>> 'alice' * 5
# 'alicealicealicealicealice'
```

### the end keyword

the keyword argument `end` can be used to avoid the newline after the output, or end the output with a different string:

```python
phrase = ['printed', 'with', 'a', 'dash', 'in', 'between']
>>> for word in phrase:
...     print(word, end='-')
...
# printed-with-a-dash-in-between-
```

### the sep keyword

the keyword `sep` specify how to separate the objects, if there is more than one:

```python
print('cats', 'dogs', 'mice', sep=',')
# cats,dogs,mice
```

# source
this cheat sheet is designed on the year 8 wa digital technology curriculum.

summarise on the https://docs.python.org/3/tutorial/index.html python 3 tutorial

------------ brian le --------------

