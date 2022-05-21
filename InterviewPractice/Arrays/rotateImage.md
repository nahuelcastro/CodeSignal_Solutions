## Rotate Image
---
*Note: Try to solve this task in-place (with `O(1)` additional memory), since this is what you'll be asked to do during an interview.*

You are given an n x n 2D matrix that represents an image. Rotate the image by 90 degrees (clockwise).

Example

For

```
a = [[1, 2, 3],
     [4, 5, 6],
     [7, 8, 9]]

```

the output should be

```
solution(a) =
    [[7, 4, 1],
     [8, 5, 2],
     [9, 6, 3]]

```

Input/Output

-   [execution time limit] 3 seconds (java)

-   [input] array.array.integer a

    *Guaranteed constraints:*\
    `1 ≤ a.length ≤ 100`,\
    `a[i].length = a.length`,\
    `1 ≤ a[i][j] ≤ 10^4^`.

-   [output] array.array.integer

[Java] Syntax Tips

```
// Prints help message to the console
// Returns a string
//
// Globals declared here will cause a compilation error,
// declare variables inside the function instead!
String helloWorld(String name) {
    System.out.println("This prints to the console when you Run Tests");
    return "Hello, " + name;
}

```

<br>

---
## Solution

```c++
int[][] solution(int[][] a) {
   int[][] res = new int[a[0].length][a.length];
   for (int i = 0; i < a.length; i++) {
       for (int j = 0; j < a[i].length; j++) {
           res[j][a.length - i - 1] = a[i][j];
       }
   }
   return res;
}
```


---
[See on app.codesignal.com](https://app.codesignal.com/interview-practice/task/5A8jwLGcEpTPyyjTB/description)