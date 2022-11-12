# Q1

```python
def multiply(m, n):
    """Takes two positive integers and returns their product using recursion.
    >>> multiply(5, 3)
    15
    """
    if n == 0:
        return 0
    else:
        return m + multiply(m, n - 1)
```

# Q4

```python
def is_prime(n):
    """Returns True if n is a prime number and False otherwise.

    >>> is_prime(2)
    True
    >>> is_prime(16)
    False
    >>> is_prime(521)
    True
    """
    def check_prime(m):
        if m == 1:
            return True
        elif n % m == 0:
            return False
        else:
            return check_prime(m - 1)
    return check_prime(n - 1)
```

# Q5

```python
def hailstone(n):
    """Print out the hailstone sequence starting at n, and return the number of elements in the sequence.
    >>> a = hailstone(10)
    10
    5
    16
    8
    4
    2
    1
    >>> a
    7
    >>> b = hailstone(1)
    1
    >>> b
    1
    """
    print(int(n))
    if n == 1:
        return 1
    elif n % 2:
        return hailstone(3 * n  + 1) + 1
    else:
        return hailstone(n / 2) + 1
```



# Q6

```python
def merge(n1, n2):
    """Merges two numbers by digit in decreasing order
    >>> merge(31, 42)
    4321
    >>> merge(21, 0)
    21
    >>> merge (21, 31)
    3211
    """
    if n1 == 0:
        return n2
    elif n2 == 0:
        return n1
    elif n1 % 10 < n2 % 10:
        smaller = n1 % 10
        return merge(n1 // 10, n2) * 10 + smaller
    else:
        smaller = n2 % 10
        return merge(n1, n2 // 10) * 10 + smaller
```


