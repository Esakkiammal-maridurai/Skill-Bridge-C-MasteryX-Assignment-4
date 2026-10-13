1. Move All Zeros to the End
2. **Code:**

```c
#include <stdio.h>

int main() {
    int a[] = {0, 1, 0, 3, 12};
    int n = 5, i, j = 0;

    for (i = 0; i < n; i++) {
        if (a[i] != 0) {
            a[j] = a[i];
            j++;
        }
    }

    while (j < n) {
        a[j] = 0;
        j++;
    }

    printf("Output: [");
    for (i = 0; i < n; i++) {
        printf("%d", a[i]);
        if (i < n - 1)
            printf(", ");
    }
    printf("]");

    return 0;
}
```

**Output:**

```text
Output: [1, 3, 12, 0, 0]
2. Maximum Sum of a Contiguous Subarray
**Code:**

```c
#include <stdio.h>

int main() {
    int a[] = {-2, 1, -3, 4, -1, 2, 1, -5, 4};
    int n = 9, i;
    int maxSum = a[0], currentSum = a[0];

    for (i = 1; i < n; i++) {
        if (currentSum + a[i] < a[i])
            currentSum = a[i];
        else
            currentSum = currentSum + a[i];

        if (currentSum > maxSum)
            maxSum = currentSum;
    }

    printf("Output: %d", maxSum);

    return 0;
}
```

**Output:**

```text
Output: 6
3. Intersection of Two Arrays
**Code:**

```c
#include <stdio.h>

int main() {
    int a[] = {1, 2, 3, 4, 5};
    int b[] = {3, 4, 5, 6, 7};
    int n = 5, m = 5;
    int i, j, first = 1;

    printf("Output: [");

    for (i = 0; i < n; i++) {
        for (j = 0; j < m; j++) {
            if (a[i] == b[j]) {
                if (first == 0)
                    printf(", ");

                printf("%d", a[i]);
                first = 0;
                break;
            }
        }
    }

    printf("]");

    return 0;
}
```

**Output:**

```text
Output: [3, 4, 5]
