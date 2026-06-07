# Count Digits in a Number

## Problem Statement

Given an integer `n`, count the total number of digits present in the number.

## Example

Input:
```text
12345
```

Output:
```text
5
```

Explanation:

```text
12345 contains 5 digits.
```

## Approach

1. Initialize `count` as 0.
2. Repeatedly divide the number by 10.
3. Increment `count` after each division.
4. Continue until the number becomes 0.
5. Print the count.

## Java Solution

```java
import java.util.*;

class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();
        int count = 0;

        if (n == 0) {
            count = 1;
        } else {
            while (n > 0) {
                count++;
                n /= 10;
            }
        }

        System.out.println(count);
    }
}
```

## Example Walkthrough

For `n = 12345`:

```text
12345 → count = 1
1234  → count = 2
123   → count = 3
12    → count = 4
1     → count = 5
0     → stop
```

Final Output:

```text
5
```

## Complexity Analysis

- **Time Complexity:** O(d)
- **Space Complexity:** O(1)

Where `d` is the number of digits in the given number.

## Tags

`Math` `Number Manipulation` `Basic Programming`
