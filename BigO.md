# Snippet 
`
def simple_sort(arr):
    n = len(arr)
    for i in range(n):
        for j in range(0, n-i-1):
            if arr[j] > arr[j+1]:
                arr[j], arr[j+1] = arr[j+1], arr[j]
`

# Task 1 - Key Operations

`for i in range(n):`
this loop runs n times making sure it accesses all the elements in the array

`for j in range(0, n-i-1):`
for each iteration of the outer loop, this loop is running through the unsorted portion. J decreases so that the largest element is sent to the end of the array.

`if arr[j] > arr[j+1]:`
this if statment compares to adjacent elements, it checks if j is bigger. This is used to compare the 2 values.

`arr[j], arr[j+1] = arr[j+1], arr[j]`
this statement swaps the 2 positions of the values so that it is ordered in accending order.

# Task 2 - Calculating Big O Complexity

Since we are running through every single number in the array there may be cases where no swaps are made or every number must be swapped. With this we may run into issues when dealing with larger arrays due to the sheer amount of iterations that we must get through before everything is reordered. As the array gets bigger the more iterations it will need to run through which will take more time. There are more efficient ways of handling the reordering.

# Task 3 - Efficiency Analysis

1. We can add a variable to detect if any swaps were made, if there were no swaps made then exit early
2. We can set the the middle number to act as the 'base' number to push numbers to the end or start based on if it's greater or smaller. Hopefully making it more efficient.