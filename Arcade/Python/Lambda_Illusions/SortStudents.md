## Sort Students
---

You are given a list of `students` who want to apply to the internship at CodeSignal. For the `i^th^` student you know their full name `students[i]`, which can consist of up to `5` words (where a word is a set of consecutive letters). It is guaranteed that the surname is always the last name of student's full name.

Your task is to sort the students [lexicographically](keyword://lexicographical-order-for-strings) by their surnames. If two students happen to have the same surname, their order in the result should be the same as in the original list.

Example

For

```
students = ["John Smith", "Jacky Mon Simonoff",
            "Lucy Smith", "Angela Zimonova"]

```

the output should be

```
solution(students) = ["Jacky Mon Simonoff", "John Smith",
                          "Lucy Smith", "Angela Zimonova"]

```

Input/Output

-   [execution time limit] 4 seconds (py3)

-   [input] array.string students

    Array of students, where each student is given by their full name consisting of at most `5` words. For each `i` `students[i]` consists of English letters and whitespace (`' '`) characters.

    *Guaranteed constraints:*\
    `1 ≤ students.length ≤ 30`,\
    `1 ≤ students[i].length ≤ 50`.

-   [output] array.string

    Array of `students` sorted as described above.



<br>

---
## Solution

```python
def solution(students):
    students.sort(key=lambda name: name.split(' ')[-1])
    return students

```
---
[See on app.codesignal.com](https://app.codesignal.com/arcade/python-arcade/lambda-illusions/EqEoH6umA9Xi8fTQM)