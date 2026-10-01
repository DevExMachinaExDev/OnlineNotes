# Binary search

A binary search is a means of searching a sorted array in O(log N) time by dividing the array into halves repeatedly until finding the value.

The algorithm usually starts in the middle and checks if the value is less than or greater than the middle element. If the value is less, it selects the left half; if it’s greater, it selects the right half. It then repeats this process on the chosen half until it finds the value or it can split the array no further.

