## Lists Concatenation
---

Given two lists `lst1` and `lst2`, your task is to return a list formed by the elements of `lst1` followed by the elements of `lst2`.

*Note: this is a bugfix task, which means that the function is already implemented but there is a bug in one of its lines. Your task is to find and fix it.*

Example

For `lst1 = [2, 2, 1]` and `lst2 = [10, 11]`, the output should be\
`solution(lst1, lst2) = [2, 2, 1, 10, 11]`.

Input/Output

-   [execution time limit] 4 seconds (py3)

-   [input] array.integer lst1

    *Guaranteed constraints:*\
    `0 ≤ lst1.length ≤ 20`,\
    `-10^6^ ≤ lst1[i] ≤ 10^6^`.

-   [input] array.integer lst2

    *Guaranteed constraints:*\
    `0 ≤ lst2.length ≤ 20`,\
    `-10^6^ ≤ lst2[i] ≤ 10^6^`.

-   [output] array.integer



<br>

---
## Solution

```python
def solution(lst1, lst2):
    res = lst1
    res.extend(lst2)
    return res

```
---
[See on app.codesignal.com](https://app.codesignal.com/arcade/python-arcade/lurking-in-lists/FumSx4KegrFbSRdQ4)