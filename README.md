# Off-by-one error in C++ vector iteration
This repository demonstrates a common off-by-one error in C++ when iterating through a `std::vector`. The error occurs because the code attempts to access the element at index `vec.size()`, which is one element beyond the valid range of indices (0 to `vec.size()-1`).

## Bug Description
The `bug.cpp` file contains a `for` loop that iterates from 0 to `vec.size()`, inclusively. This leads to an out-of-bounds access when `i` equals `vec.size()`. 

## Solution
The `bugSolution.cpp` file corrects the error by changing the loop condition to `i < vec.size()`, ensuring that the loop only iterates over valid indices.