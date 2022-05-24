## Create Histogram
---


You noticed that one of your employees has a weird performance rate: although his performance is usually good and stable, from time to time it drops drastically. You suspect it has something to do with the famous Code of Clones series: new episodes started to come out recently, and everyone watches and rewatches them every so often.

To confirm your theory, you'd like to create a histogram showing the number of assignments he completed each day in the given period. Given this `assignments`, return a list representing a horizontal histogram, where each bar is formed by the given character `ch`.

Example

For `ch = '*'` and `assignments = [12, 12, 14, 3, 12, 15, 14]`,\
the output should be

```
solution(ch, assignments) = ["************",
                                    "************",
                                    "**************",
                                    "***",
                                    "************",
                                    "***************",
                                    "**************"]

```

Input/Output

-   [execution time limit] 4 seconds (py3)

-   [input] char ch

    A character that should compose the histogram.

-   [input] array.integer assignments

    A list of assignments your employee completed each day during some period.

    *Guaranteed constraints:*\
    `1 ≤ assignments.length ≤ 20`,\
    `0 ≤ assignments[i] ≤ 50`.

-   [output] array.string

    A histogram built as described above.


<br>

---
## Solution

```python
def solution(ch, assignments):
    return [ch*assignment for assignment in assignments]

```
---
[See on app.codesignal.com](https://app.codesignal.com/arcade/python-arcade/fumbling-in-functional/rXovZdK7redkSJL5g)