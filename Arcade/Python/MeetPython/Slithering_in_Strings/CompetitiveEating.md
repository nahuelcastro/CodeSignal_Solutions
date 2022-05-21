## 
---
Implement the missing code, denoted by ellipses. You may not modify the pre-existing code.

The World Wide Competitive Eating tournament is going to be held in your town, and you're the one who is responsible for keeping track of time. For the great finale, a large billboard of the given `width` will be installed on the main square, where the time of possibly new world record will be shown.

The track of time will be kept by a float number. It will be displayed on the board with the set precision `precision` with center alignment, and it is guaranteed that it will fit in the screen. Your task is to test the billboard. Given the time `t`, the `width` of the screen and the `precision` with which the time should be displayed, return a string that should be shown on the billboard.

Example

For `t = 3.1415`, `width = 10`, and `precision = 2`,\
the output should be

```
solution(t, width, precision) = "   3.14   "

```

Input/Output

-   [execution time limit] 4 seconds (py3)

-   [input] float t

    The time to be displayed on the billboard. It is guaranteed that `t` has at most `5` digits after the decimal point.

    *Guaranteed constraints:*\
    `0 ≤ t < 1000`.

-   [input] integer width

    The width of the billboard. It is guaranteed that it's big enough to display the time `t` with the desired precision.

    In case it's impossible to align the time perfectly in the center, left padding should be `1` whitespace character shorter than right padding.

    *Guaranteed constraints:*\
    `3 ≤ width ≤ 20`.

-   [input] integer precision

    Precision with which the number should be displayed.

    *Guaranteed constraints:*\
    `0 ≤ precision ≤ 10`.

-   [output] string

    A string of length `width` representing the time `t` as it will be displayed on the billboard.
<br>

---
## Solution

```python
def solution(t, width, precision):
    return '{:^{}.{}f}'.format(t,width,precision)

```
---
[See on app.codesignal.com](https://app.codesignal.com/arcade/python-arcade/slithering-in-strings/BPFsda3ddPJruBX24)