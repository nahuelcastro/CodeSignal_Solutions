## Construct Shell
---


A 2D list `lst` of size `2 * n - 1` is called a *shell* if it is filled with zeros and has the following configuration:

-   `lst[0]` contains one element;
-   `lst[1]` contains two elements;
-   ...
-   `lst[n - 2]` contains `n - 1` elements;
-   `lst[n - 1]` contains `n` elements;
-   `lst[n]` contains `n - 1` elements;
-   ...
-   `lst[2 * n - 3]` contains two elements;
-   `lst[2 * n - 2]` contains one element.

Given an integer `n`, return a *shell* list.

Example

For `n = 3`, the output should be

```
solution(n) = [[0],
                     [0, 0],
                     [0, 0, 0],
                     [0, 0],
                     [0]]

```

Input/Output

-   [execution time limit] 4 seconds (py3)

-   [input] integer n

    An integer defining the size of the *shell*.

    *Guaranteed constraints:*\
    `1 ≤ n ≤ 30`.

-   [output] array.array.integer

    A *shell*.


<br>

---
## Solution

```python
def solution(n):
    return [[0 for x in range(y+1)] for y in range (n-1)] + [[0 for x in range(y+1)] for y in range (n)][::-1]
```
---
[See on app.codesignal.com](https://app.codesignal.com/arcade/python-arcade/complexity-of-comprehension/DfDPhgb5Bj2HQSdr5)