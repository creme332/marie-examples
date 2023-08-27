# Two sum
Given the size of an array `n` and an integer target `k`, input an array of `n` integers and return the indices of the two numbers that add up to `k`. Assume $n>1$. Output 0 if target cannot be reached.

Adapted from [LeetCode](https://leetcode.com/problems/two-sum/).

## Test cases
### Test 1: n = 4 and target can be reached
Input list:
```
4
10
5
4
3
7
```

Output list:
```
2
3
```
### Test 2: n = 2
Input list:
```
2
5
4
1
```

Output list:
```
0
1
```

### Test 3: Target cannot be reached
Input list:
```
5
100
1
2
3
9
55
```

Output list:
```
0
```
## Pseudocode

```python
# Input n, k
# Input array arr
for i in range(0, n):
    for j in range(i + 1, n):
        if arr[i] + arr[j] = k:
            print (i, j)
            # exit program
```
Time complexity: $\mathbb{O}(n^2)$

Space complexity: $\mathbb{O}(n)$