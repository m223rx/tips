# Challenge: Java String Compressor

## Difficulty
Medium

## Description
Write a program that takes a string consisting of alphabetic characters (both uppercase and lowercase) and compresses it using the following rule:

- Consecutive identical characters are replaced by the character followed by the count of repetitions.
- If a character appears only once consecutively, it should remain unchanged (i.e., no `1` appended).
- The compression should be case‑sensitive (`a` and `A` are considered different characters).

**Example**

| Input                | Output          |
|----------------------|-----------------|
| `aaabbcdddd`         | `a3b2cd4`       |
| `HelloWorld`         | `Hel2oWorld`    |
| `CCCCCCCCCCCC`       | `C12`           |
| `abABabAB`           | `abABabAB`      |

If the resulting compressed string is not shorter than the original string, the program should output the original string unchanged.

## Requirements
- Read a single line of input from standard input.
- Output the compressed (or original) string to standard output.
- The program must run in **O(n)** time, where *n* is the length of the input string.
- Only standard Java libraries may be used.
- The solution should handle edge cases such as an empty input string or a string of length 1.

## Bonus
- Extend the program to support compression of numeric characters as well (e.g., `111222` → `13`2`).
- Provide a command‑line option (e.g., `-force`) that forces the program to output the compressed string even if it is longer than the original.
- Implement the compression logic without using any additional data structures (i.e., only primitive variables and the original string).