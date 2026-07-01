# Algorithm: Maximum Consecutive 1's in an Array

## Problem Statement

Given a binary array, find the maximum number of consecutive `1`s.

## Algorithm

1. Read the size of the array `n`.
2. Read all the array elements.
3. Initialize two variables:

   * `count = 0` → Stores the current consecutive count of `1`s.
   * `maxCount = 0` → Stores the maximum consecutive count found so far.
4. Traverse the array from left to right.
5. For each element:

   * If the current element is `1`:

     * Increment `count`.
     * Update `maxCount` if `count` is greater than `maxCount`.
   * Otherwise:

     * Reset `count` to `0` because the sequence of consecutive `1`s is broken.
6. After traversing the entire array, print or return `maxCount`.

## Dry Run

**Input**

```
[1, 1, 0, 1, 1, 1]
```

| Element | Current Count | Maximum Count |
| ------- | ------------: | ------------: |
| 1       |             1 |             1 |
| 1       |             2 |             2 |
| 0       |             0 |             2 |
| 1       |             1 |             2 |
| 1       |             2 |             2 |
| 1       |             3 |             3 |

**Output**

```
3
```

## Time Complexity

* **O(n)** — The array is traversed exactly once.

## Space Complexity

* **O(1)** — Only two integer variables (`count` and `maxCount`) are used.

## Key Idea

Maintain a running count of consecutive `1`s while traversing the array. Whenever a `0` is encountered, reset the count to `0`. Continuously update the maximum count to obtain the longest sequence of consecutive `1`s.
