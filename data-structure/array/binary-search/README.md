# Binary Search

You are given a **sorted** integer array of size `n` and a target integer `x`. Implement an efficient algorithm to find the index of the target element `x` within the array using the binary search technique.

The array will be in ascending order and uses zero-based indexing.

## Test cases
### Element in array
Input:
```
4
3
1
2
3
4
```
Output: 2.

Explanation: Input array is [1, 2, 3, 4] and index of 3 is 2.

```
4
4
1
2
3
4
```
Output: 3.

Explanation: Input array is [1, 2, 3, 4] and index of 4 is 3.

### Element is not in array
```
4
4
1
2
3
9
```
Output: None.

Explanation: Input array is [1, 2, 3, 9] and 4 is absent.

## Pseudocode
```c++
// Adapted from Competitive Programmer’s Handbook pg 31 , Antti Laaksonen
int binarysearch(int x, std::vector <int> arr) { //returns index of x in arr
	int i = 0; // index
	int n = arr.size();
	for (int jump = n / 2; jump >= 1; jump /= 2) { // b: jump length
		while (i + jump < n && arr[i + jump] <= x) i += jump ; //make jump to right if element on next jump <= x
	}
	return ((arr[i] == x)) ? i : -1; //i+1 is the index of smallest integer greater than x
}
```
Time complexity: $\mathbb O(\log n)$

