## Add Border
---
Given a rectangular matrix of characters, add a border of asterisks(`*`) to it.

Example

For

```
picture = ["abc",
           "ded"]

```

the output should be

```
solution(picture) = ["*****",
                      "*abc*",
                      "*ded*",
                      "*****"]

```

Input/Output

-   [execution time limit] 4 seconds (py3)

-   [input] array.string picture

    A non-empty array of non-empty equal-length strings.

    *Guaranteed constraints:*\
    `1 ≤ picture.length ≤ 100`,\
    `1 ≤ picture[i].length ≤ 100`.

-   [output] array.string

    The same matrix of characters, framed with a border of asterisks of width `1`.

<br>

---
## Solution

```python
def solution(picture):
    x = len(picture[0])
    y = len(picture)
    
    x_add = ''
    for i in range(x):
        x_add += '*'
    
    picture = [x_add] + picture + [x_add]
    
    
    for i in range(len(picture)):
        picture[i] = '*' + picture[i] + '*'
    
    return picture
```
---
[See on app.codesignal.com](https://app.codesignal.com/arcade/intro/level-4/ZCD7NQnED724bJtjN)