# Binary Search

> This part is about **LeetCode** **Binary Search** problems.

## What is Binary Search?

* Reduce the search space by half at each step
* Input usually needs to be sorted


## Why Binary Search?

* Fast
* T(n) = T(n/2) + O(evaluation)
* O(log(range)) * O(eval) vs O(range) * O(eval)

|         Range | Binary |    Linear | Speed Up (x) |
|--------------:|-------:|----------:|-------------:|
|           100 |      7 |       100 |        14.29 |
|        10,000 |     14 |    10,000 |       714.29 |
|     1,000,000 |     20 | 1,000,000 |    50,000.00 |
| 1,000,000,000 |     30 |       TLE |          N/A |


## Template [l, r)

Given a function g, returns the smallest m in the given range such that g(m) is true.

```Python
def binary_search(l, r):
	while l < r:
		m = l + (r - l) // 2
		if f(m): return m # optional
		if g(m):
			r = m.     # new range[l, m)
		else:
			l = m + 1; # new range[m+1, r)
	return l # or not found

```

> Time Complexity: O(log(r-l))*(f(m) + g(m)) <br/>
> Space Complexity: O(1)


## Problem List

- [34. Find First and Last Position of Element in Sorted Array](leetcode/binarysearch/34.FindFirstandLastPositionofElementinSortedArray.md)
- [35. Search Insert Position](leetcode/binarysearch/35.SearchInsertPosition.md)
- [69. Sqrt(x)](leetcode/binarysearch/69.Sqrt(x))
- [981. Time Based Key-Value Store](leetcode/binarysearch/981.TimeBasedKey-ValueStore.md)




