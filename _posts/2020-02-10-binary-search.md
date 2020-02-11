---
layout: post
title:  "Binary Search"
author: "Adi Bhamidipati"
---

Binary search is an efficient algorithm to search for an element in a sorted list. It is based on divide and conquer technique. The biggest caveat for binary search is, input list should be sorted.

#### Algorithm:

First step is to find the low and high elements in the list, since the list is sorted, index of the “low” element 0, and index of the “high” is [length of list] -1,
As the name suggest we divide list into two halves, so the pivot element would be high + low / 2
a) If pivot is target element return the number.
b) Check if the target element is greater than pivot, then discard the first half, so low index would be pivot + 1
c) Otherwise discard the second half, so high index would be pivot - 1
We should continue the above process till low < high value, so by this time, we should have found the element otherwise return empty.
Basic Implementation of Binary Search [In python]:

#### Implementation:

{% highlight markdown %}
Class BinarySearch:
def search(target: int,nums:List):
low = 0
high = len(nums) - 1
while (low <= high):
pivot = high + low / 2
if (nums[pivot] > target):
  high = pivot -1
elif (nums[pivot] < target):
  low = pivot + 1
else
  return pivot
return -1
{% endhighlight %}

Since in iteration list will be reduced by half,so the time complexity is O(log n) with O(1) space complexity.

One of the popular applications of binary search is finding a square root of a number

#### Implementation of Square root of a number

{% highlight markdown %}
def sqrt(number: int):
low = 0
high = number // 2
mid = 0
while(low < high):
  mid = (low + high) // 2
  mid_sqrd = mid * mid
  if(mid_sqrd == number):
    return mid
  if(mid_sqrd > number):
    high = mid - 1
  elif (mid_sqrd < number):
    low = mid + 1
return low -1
{% endhighlight %}
