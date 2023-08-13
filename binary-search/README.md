# Binary Search

```c++
int binarysearch(int x, std::vector <int> arr) { //returns index of x in arr
	int i = 0; // index
	int n = arr.size();
	for (int jump = n / 2; jump >= 1; jump /= 2) { // b: jump length
		while (i + jump < n && arr[i + jump] <= x) i += jump ; //make jump to right if element on next jump <= x
	}
	return ((arr[i] == x)) ? i : -1; //i+1 is the index of smallest integer greater than x
}
```