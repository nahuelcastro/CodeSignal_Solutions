## Sort by Height
---

Some people are standing in a row in a park. There are trees between them which cannot be moved. Your task is to rearrange the people by their heights in a non-descending order without moving the trees. People can be very tall!

Example

For `a = [-1, 150, 190, 170, -1, -1, 160, 180]`, the output should be\
`solution(a) = [-1, 150, 160, 170, -1, -1, 180, 190]`.

Input/Output

-   [execution time limit] 4 seconds (py3)

-   [input] array.integer a

    If `a[i] = -1`, then the `i^th^` position is occupied by a tree. Otherwise `a[i]` is the height of a person standing in the `i^th^` position.

    *Guaranteed constraints:*\
    `1 ≤ a.length ≤ 1000`,\
    `-1 ≤ a[i] ≤ 1000`.

-   [output] array.integer

    Sorted array `a` with all the trees untouched.

    <br>

---
## Solution

```python
def solution(a):
    people = []
    for h in a:
        if(h != -1):
            people.append(h)
    people.sort()
    
    j = 0
    for i in range(len(a)):
        if(a[i] != -1):
            a[i] = people[j]
            j += 1
    return a
```

---
[See on app.codesignal.com](https://app.codesignal.com/arcade/intro/level-3/D6qmdBL2NYz49XHwM)