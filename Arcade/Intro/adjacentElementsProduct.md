## Adjacent Elements Product
---

Given an array of integers, find the pair of adjacent elements that has the largest product and return that product.

Example

For `inputArray = [3, 6, -2, -5, 7, 3]`, the output should be\
`solution(inputArray) = 21`.

`7` and `3` produce the largest product.

Input/Output

-   [execution time limit] 4 seconds (py3)

-   [input] array.integer inputArray

    An array of integers containing at least two elements.

    *Guaranteed constraints:*\
    `2 ≤ inputArray.length ≤ 10`,\
    `-1000 ≤ inputArray[i] ≤ 1000`.

-   [output] integer

    The largest product of adjacent elements.

<br>

---
## Solution

```python
def solution(inputArray):
    res = inputArray[0] * inputArray[1]
    for i in range(0,len(inputArray)-1):
        mul = inputArray[i] * inputArray[i+1]
        if res < mul:
            res = mul
    return res
```

---
[See on app.codesignal.com](https://app.codesignal.com/arcade/intro/level-2/xzKiBHjhoinnpdh6m)
