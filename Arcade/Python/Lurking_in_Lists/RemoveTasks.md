## Remove Tasks
---


Today is a good day: it's the `k^th^` year since you started to work at the company, which means you have to have a party today. In order to get home earlier and prepare for the jamboree, you need to get home early. You decided to remove each `k^th^` tasks from your `toDo` list, since today is your day and you can do whatever you please.

Given the list of task ids in your `toDo` list, remove each `k^th^` task from it and return the list of remaining tasks.

Example

For `k = 3` and `toDo = [1237, 2847, 27485, 2947, 1, 247, 374827, 22]`,\
the output should be\
`solution(k, toDo) = [1237, 2847, 2947, 1, 374827, 22]`.

Input/Output

-   [execution time limit] 4 seconds (py3)

-   [input] integer k

    *Guaranteed constraints:*\
    `1 ≤ k ≤ 30`.

-   [input] array.integer toDo

    Ids of the tasks in your to-do list.

    *Guaranteed constraints:*\
    `1 ≤ toDo.length ≤ 100`,\
    `1 ≤ toDo[i] ≤ 4 - 10^5^`.

-   [output] array.integer


<br>

---
## Solution

```python
def solution(k, toDo):
    del toDo[k-1::k]
    return toDo

```
---
[See on app.codesignal.com](https://app.codesignal.com/arcade/python-arcade/lurking-in-lists/L3TQWdGMcWL85LHcR)