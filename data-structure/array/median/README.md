# Median

Take as input the size `n` of an array of integers, input `n` integers, and output the median of the array. If median is not an integer, output the quotient and the remainder.

## Test cases

Input:
```
4
1
-1
2
3
```
Output:
```
1
1
```
Sorted array is `-1 1 2 3` and median is `3/2` which has quotient = remainder = 1

Input:
```
4
2
-1
2
3
```
Output: `2`

Sorted array is `-1 2 2 3` and median is `4/2 = 2`.


## Pseudocode

```python
sort array
if n is odd:
    print (arr[(n+1)/2])
else:
    sum = arr[n/2] arr[n/2 - 1]
    print(sum / 2, sum % 2)
```