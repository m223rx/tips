# Challenge: Java Word Ladder

## Difficulty
Medium

## Description
Given two words of equal length, `start` and `end`, and a dictionary of valid words, find the shortest transformation sequence from `start` to `end`. Each step in the sequence must change exactly one character, and the resulting word after each change must exist in the dictionary. If no such sequence exists, return an empty list.

For example, given:

- `start = "hit"`
- `end = "cog"`
- `dictionary = ["hot","dot","dog","lot","log","cog"]`

One shortest transformation sequence is `["hit","hot","dot","dog","cog"]`.

Your task is to implement a method that returns **any** one of the shortest possible transformation sequences. The sequence must include both the `start` and `end` words.

## Requirements
- Implement the solution in **Java**.
- The method signature should be:
  ```java
  List<String> findWordLadder(String start, String end, Set<String> dictionary)
  ```
- If `start` and `end` are the same word, return a list containing just that word.
- The method should return an empty list if no transformation sequence exists.
- Optimize for time and space; aim for a solution that runs efficiently on large dictionaries (e.g., up to 10⁵ words).

## Bonus
- Extend the solution to return **all** shortest transformation sequences, not just one.
- Provide a version that works for words of different lengths, where a step may involve either changing a single character, inserting a character, or deleting a character, as long as the intermediate word remains in the dictionary.
    


    ---
    **Author:** m223rx
    **Date:** 2026-03-28 13:33:22
    ---
    


    