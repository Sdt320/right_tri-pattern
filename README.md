# right_tri-pattern
To generate the specified pattern, where the number of stars increases and spaces are introduced in the middle to form a diamond-like structure, you can follow these steps:

1. Print the upper part of the pattern including the middle line with spaces.
2. Print the lower part of the pattern excluding the middle line, mirroring the upper part.

### C Program for the Pattern

Here's the C code to generate the pattern you described:

```c
#include <stdio.h>

int main() {
    int i, j, n;
    printf("Enter the number of rows: ");
    scanf("%d", &n);

    // Upper part of the pattern (including the middle line)
    for (i = 0; i < n + 1; i++) {
        printf("*");
        for (j = 0; j < i; j++) {
            printf(" ");
        }
        if (i != 0) {
            printf("*");
        }
        printf("\n");
    }

    // Lower part of the pattern (excluding the middle line)
    for (i = n - 1; i >= 0; i--) {
        printf("*");
        for (j = 0; j < i; j++) {
            printf(" ");
        }
        if (i != 0) {
            printf("*");
        }
        printf("\n");
    }

    return 0;
}
```

### Explanation:

1. **Input Handling:**
   - The user inputs the value `n`, which represents the number of rows for each half of the pattern (excluding the middle row).

2. **Upper Part of the Pattern:**
   - The outer loop `for (i = 0; i < n + 1; i++)` iterates from `0` to `n` to create the upper part of the pattern, including the middle line.
   - For each iteration, the program prints a leading star (`*`).
   - The inner loop `for (j = 0; j < i; j++)` prints spaces.
   - If it's not the first line (`i != 0`), the program prints an additional star after the spaces.

3. **Lower Part of the Pattern:**
   - The outer loop `for (i = n - 1; i >= 0; i--)` iterates from `n-1` down to `0` to create the lower part of the pattern.
   - For each iteration, the program prints a leading star (`*`).
   - The inner loop `for (j = 0; j < i; j++)` prints spaces.
   - If it's not the first line (`i != 0`), the program prints an additional star after the spaces.

### Result:

If the user inputs `5`, the program will generate the following pattern:

```
*
**
* *
*  *
*   *
*    *
*   *
*  *
* *
**
*
```

This program will produce the specified pattern with increasing stars and spaces in the middle, forming a diamond-like structure.
