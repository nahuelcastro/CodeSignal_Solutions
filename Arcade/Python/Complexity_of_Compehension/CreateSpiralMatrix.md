## Create Spiral Matrix
---


A spiral matrix is a square matrix of size n × n. It contains all the integers in range from 1 to n * n so that number 1 is written in the bottom right corner, and all other numbers are written in increasing order spirally in the counterclockwise direction.

Given the size of the matrix n, your task is to create a spiral matrix.

Example

For n = 3, the output should be

solution(n) = [[5, 4, 3],
                         [6, 9, 2],
                         [7, 8, 1]]
Input/Output

[execution time limit] 4 seconds (py3)

[input] integer n

Matrix size, a positive integer.

Guaranteed constraints:
3 ≤ n ≤ 75.

[output] array.array.integer

A spiral matrix of size n.


<br>

---
## Solution

```python
def solution(n):
    dirs = [(-1, 0), (0, -1), (1, 0), (0, 1)]
    curDir = 0
    curPos = (n - 1, n - 1)
    res = [[0 for x in range(n)] for y in range (n)]

    for i in range(1, n * n + 1):
        res[curPos[0]][curPos[1]] = i
        nextPos = curPos[0] + dirs[curDir][0], curPos[1] + dirs[curDir][1]
        if not (0 <= nextPos[0] < n and
                0 <= nextPos[1] < n and
                res[nextPos[0]][nextPos[1]] == 0):
            curDir = (curDir + 1) % 4
            nextPos = curPos[0] + dirs[curDir][0], curPos[1] + dirs[curDir][1]
        curPos = nextPos

    return res

```
---
[See on app.codesignal.com](https://app.codesignal.com/arcade/python-arcade/complexity-of-comprehension/HZjrbpxa7gbrmb4kd)