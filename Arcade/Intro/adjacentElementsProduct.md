## Adjacent Elements Product
---

Given an array of integers, find the pair of adjacent elements that has the largest product and return that product.

![img.](https://codesignal.s3.amazonaws.com/tasks/shapeArea/img/area.png?_tm=1624642306583)

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
int solution(int n) {
    if(n==1){
        return 1;
    }
    return solution(n-1) + 4 * (n-1);
}
```

---
[See on app.codesignal.com](hhttps://app.codesignal.com/arcade/intro/level-2/yuGuHvcCaFCKk56rJ)
