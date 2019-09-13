#### Please add your answers to the ***Analysis of  Algorithms*** exercises here.

## Exercise I

a) `O(n)` - This one's tricky, but the `n*n` inside the while loop cancels out an `n*n` in condition. `while (a < n * 1)`: `a = a + 1` does the same number of loops.


b) `O(nlog(n))` - the `j*=2` line is `log(n)`, so we have a for loop of `O(n)` and inside that we have the `O(log(n))`, so the complexity is `O(n * log(n))`


c) `O(n)` - executes an action (add 2) once for every initial input

## Exercise II

