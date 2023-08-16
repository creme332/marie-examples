# Euclidean algorithm

Takes as input two positive integers $a$ and $b$ and calculates $gcd(a,b)$ using [Euclidean algorithm](https://simple.wikipedia.org/wiki/Euclidean_algorithm).

## Test cases
### Invalid GCD
Input:
```
0
0
```
Output: None

### GCD = 0
Input:
```
5
0
```
Output: `5`

Input:
```
0
5
```
Output: `5`

### GCD of primes

Input:
```
13
17
```
Output: `1`

### GCD > 1
Input:
```
36
108
```
Output: `36`

Input:
```
36
48
```
Output: `12`

## Pseudocode

This algorithm uses subtraction instead of modular arithmetic. Consequently, it is a bit slow.
```python
def gcd(a, b):
    # ensure that a >= b
    if b > a:
        temp = a
        a = b
        b = temp

    # deal with corner cases
    if a == 0:
        return

    if b == 0:
        return a

    return gcd(a-b, b)


print(gcd(0, 0))
print(gcd(1, 0))
print(gcd(24, 60))
print(gcd(4, 537))

# None
# 1
# 12
# 1
```