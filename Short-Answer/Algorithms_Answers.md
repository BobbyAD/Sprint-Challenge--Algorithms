#### Please add your answers to the ***Analysis of  Algorithms*** exercises here.

## Exercise I

a) `O(n)` - This one's tricky, but the `n*n` inside the while loop cancels out an `n*n` in condition. `while (a < n * 1)`: `a = a + 1` does the same number of loops.


b) `O(nlog(n))` - the `j*=2` line is `log(n)`, so we have a for loop of `O(n)` and inside that we have the `O(log(n))`, so the complexity is `O(n * log(n))`


c) `O(n)` - executes an action (add 2) once for every initial input

## Exercise II

To find the nth floor where the eggs don't break I can use a binary search that goes down if the egg breaks, and up if it doesn't.

Pseudocode: floors is a list, broken_egg represents a boolean that's true if the egg broke, false if it didn't
O(log(n))
```
    findFloor(floors):
        highPoint = len(floors)
        currentMid = len(floors//2)/2
        found = False
        while (found = False):
            if (floors[currentMid] - 1 != broken_egg) and (floors[currentMid] == broken_egg):
                found = True
                return currentMid
            #In case the top floor is the answer
            elif (floors[highPoint] - 1 != broken_egg) and (floors[highPoint] == broken_egg):
                found = True
                return highPoint
            elif (floors[currentMid] == broken_egg):
                highPoint = currentMid
                currentMid = currentMid//2
            elif (floors[currentMid] != broken_egg):
                currentMid += (highPoint - currentMid)//2
```