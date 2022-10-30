# Q1: Case Conundrum

```
12

19

12
```

# Q2: Jacket Weather?

```python
""" Q2: Jacket Weather """
def wears_jacket_with_if(temp, raining):
    """
    >>> wears_jacket_with_if(90, False)
    False
    >>> wears_jacket_with_if(40, False)
    True
    >>> wears_jacket_with_if(100, True)
    True
    """
    "*** YOUR CODE HERE ***"
    if raining or temp < 60:
        return True
    return False
```

# Q3: Square So Slow

Infinite loop

# Q4: Is Prime?

```python
""" Q4: Is Prime? """
def is_prime(n):
    """
    >>> is_prime(10)
    False
    >>> is_prime(7)
    True
    >>> is_prime(1) # one is not a prime number!!
    False
    """
    "*** YOUR CODE HERE ***"
    if n == 1:
        return False
    k = 2
    while k <= sqrt(n):
        if n % k == 0:
            return False
        k = k + 1
    return True
```

# Q5: Fizzbuzz

```python
""" Q5: Fizzbuzz """
def fizzbuzz(n):
    """
    >>> result = fizzbuzz(16)
    1
    2
    fizz
    4
    buzz
    fizz
    7
    8
    fizz
    buzz
    11
    fizz
    13
    14
    fizzbuzz
    16
    >>> result is None  # No return value
    True
    """
    "*** YOUR CODE HERE ***"
    for i in range(1, n + 1):
        fb(i)

def fb(n):
    """ print fizz or buzz """
    if n % 15 == 0:
        print('fizzbuzz')
    elif n % 3 == 0:
        print('fizz')
    elif n % 5 == 0:
        print('buzz')
    else:
        print(n)
```

# Q6: Unique Digits

```python
""" Q6: Unique Digits """
def unique_digits(n):
    """Return the number of unique digits in positive integer n.
    >>> unique_digits(8675309) # All are unique
    7
    >>> unique_digits(1313131) # 1 and 3
    2
    >>> unique_digits(13173131) # 1, 3, and 7
    3
    >>> unique_digits(10000) # 0 and 1
    2
    >>> unique_digits(101) # 0 and 1
    2
    >>> unique_digits(10) # 0 and 1
    2
    """
    "*** YOUR CODE HERE ***"
    result = 0
    for i in range(0, 10):
        if has_digit(n, i):
            result = result + 1
    return result

def has_digit(n, k):
    """Returns whether K is a digit in N.
    >>> has_digit(10, 1)
    True
    >>> has_digit(12, 7)
    False
    """
    "*** YOUR CODE HERE ***"
    while n > 0:
        if n % 10 == k:
            return True
        n = n // 10
    return False
```