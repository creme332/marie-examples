# Prime Number Checker
Write a program to check if a number `n`, where $n\in\mathbb Z^+$ is prime.


## Test cases

| Input | Output |
| ----- | ------ |
| 1     | 0      |
| 2     | 1      |
| 3     | 1      |
| 12    | 0      |
| 13    | 1      |
| 123   | 0      |

## Pseudocode

Naive solution:
```python
def primeCheck(n):
    if n < 2:
        return False
    i = 2
    while (i < n):
        if (n % i == 0):
            return False
        i += 1
    return True
```