# Challenge: Java – Palindrome Partitioning Counter

## Difficulty
Medium

## Description
Write a Java program that reads a single line of input containing a non‑empty string consisting of only lowercase English letters (`a`‑`z`).  
Your task is to determine the number of different ways the string can be partitioned into substrings such that **every substring is a palindrome**.

A *partition* of a string is a way of breaking the string into a sequence of non‑empty substrings that concatenated together reproduce the original string. Two partitions are considered different if the positions of the cuts differ, even if the resulting substrings are the same.

For example, for the input `aab`, the valid palindrome partitions are:
1. `a | a | b`
2. `aa | b`

Hence the answer would be `2`.

Your program should output a single integer: the total number of palindrome partitions of the input string.

### Constraints
- The length of the input string `n` satisfies `1 ≤ n ≤ 1,000`.
- The result may be large; output it modulo `1,000,000,007`.

## Requirements
- Read the input from standard input (`System.in`).
- Write the result to standard output (`System.out`).
- Implement an efficient solution with a time complexity of **O(n²)** or better.
- Use only standard Java libraries (no third‑party dependencies).

## Bonus
- Optimize the solution to run in **O(n)** time using Manacher’s algorithm or another advanced technique.
- Extend the program to also output **all** distinct palindrome partitions (one per line) in lexicographic order, in addition to the count. (Be mindful of potential exponential output; this bonus is optional.)
    


---
**Author:** m223rx
**Date:** 2026-03-28 13:54:28
---
    


    