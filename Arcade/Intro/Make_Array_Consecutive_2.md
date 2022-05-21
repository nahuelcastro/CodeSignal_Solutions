## Make Array Consecutive 2
---
Ratiorg got `statues` of *different* sizes as a present from CodeMaster for his birthday, each statue having an non-negative integer size. Since he likes to make things perfect, he wants to arrange them from smallest to largest so that each statue will be bigger than the previous one exactly by `1`. He may need some additional statues to be able to accomplish that. Help him figure out the minimum number of additional statues needed.

Example

For `statues = [6, 2, 3, 8]`, the output should be\
`solution(statues) = 3`.

Ratiorg needs statues of sizes `4`, `5` and `7`.

Input/Output

-   [execution time limit] 4 seconds (py3)

-   [input] array.integer statues

    An array of *distinct* non-negative integers.

    *Guaranteed constraints:*\
    `1 ≤ statues.length ≤ 10`,\
    `0 ≤ statues[i] ≤ 20`.

-   [output] integer

    The minimal number of statues that need to be added to existing `statues` such that it contains every integer size from an interval `[L, R]` (for some `L, R`) and no other sizes.


<br>

---
## Solution

```python
def solution(statues):
    if len(statues) == 1:
        return 0
    min = statues[0]
    max = statues[0]
    for sta in statues:
        if sta < min:
            min = sta
        if sta > max:
            max = sta
    delta = max - min
    need = delta - 1 - len(statues) + 2
    return need

```

---
[See on app.codesignal.com](https://app.codesignal.com/arcade/intro/level-2/bq2XnSr5kbHqpHGJC)