## All Longest Strings
---

Given an array of strings, return another array containing all of its longest strings.

Example

For `inputArray = ["aba", "aa", "ad", "vcd", "aba"]`, the output should be\
`solution(inputArray) = ["aba", "vcd", "aba"]`.

Input/Output

-   [execution time limit] 5 seconds (ts)

-   [input] array.string inputArray

    A non-empty array.

    *Guaranteed constraints:*\
    `1 ≤ inputArray.length ≤ 10`,\
    `1 ≤ inputArray[i].length ≤ 10`.

-   [output] array.string

    Array of the longest strings, stored in the same order as in the `inputArray`.


<br>

---
## Solution

```typescript
function solution(inputArray: string[]): string[] {
    let max: number = 0;
    let ret: string[] = [];

    for (let str of inputArray) {
        if (str.length > max){ 
            max = str.length;
        }
    }

    for (let str of inputArray) {
        if (str.length == max){ 
            ret.push(str);
        }
    }
    return ret;
}
```

---
[See on app.codesignal.com](https://app.codesignal.com/arcade/intro/level-3/fzsCQGYbxaEcTr2bL)