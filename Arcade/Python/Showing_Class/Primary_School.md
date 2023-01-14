##
---


Tomorrow is Jim's first day as a teacher in a primary school. He's quite nervous about his new job, and in order to relax he decides to write a simple program, because nothing calms as much as coding.

Since Jim is going to tell the kids about rectangles, he wants to implement a function that will calculate the area of rectangle of the given `height` and `width` and show how the result is obtained. Help Jim to gain his confidence and implement the function he needs.

Example

For `height = 7` and `width = 4`, the output should be\
`solution(height, width) = "7 x 4 = 28"`.

The area of the rectangle of size `7 × 4` is calculated as `7 * 4` and is equal to `28`.

Input/Output

-   [execution time limit] 4 seconds (py3)

-   [input] integer height

    The height of the rectangle.

    *Guaranteed constraints:*\
    `1 ≤ height ≤ 20`.

-   [input] integer width

    The width of the rectangle.

    *Guaranteed constraints:*\
    `1 ≤ width ≤ 20`.

-   [output] string

    A string containing the area of the given rectangle and how it was obtained in the format `"*height* x *width* = *area*"`


<br>

---
## Solution

```python
class Rectangle(object):
    def __init__(self, height, width):
        self.height = height
        self.width = width

    def __str__(self):
        return '{} x {} = {}'.format(self.height, self.width, self.area)

    def __init__(self, height, width):
        self.height = height
        self.width = width
        self.area = self.height * self.width


def solution(height, width):
    return str(Rectangle(height, width))

```
---
[See on app.codesignal.com](https://app.codesignal.com/arcade/python-arcade/showing-class/pzhNXW2KrdRWyhxzR)