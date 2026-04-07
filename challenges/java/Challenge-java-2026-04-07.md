# Challenge: **Concurrent Word Counter**

## Difficulty  
Medium

## Description  
You are given a large text file (potentially several gigabytes) containing English words separated by whitespace and punctuation. Your task is to write a Java program that counts the occurrences of each distinct word in the file as efficiently as possible using concurrent processing.

The program should:

1. Read the file in a streaming fashion (i.e., without loading the entire file into memory).
2. Split the text into words, normalizing them to lower‑case and stripping leading/trailing punctuation.
3. Count how many times each unique word appears.
4. Output the top **N** most frequent words, sorted by descending frequency (and alphabetically for ties).

Assume the file path and the value of **N** are provided as command‑line arguments.

## Requirements  

- **Input handling**
  - Accept two command‑line arguments: the absolute path to the input file and an integer `N`.
  - Validate the arguments and provide meaningful error messages for invalid input (e.g., file not found, `N` not positive).

- **Word extraction**
  - Treat any sequence of letters (`a‑z` or `A‑Z`) as a word.
  - Ignore numbers, symbols, and punctuation surrounding words (e.g., `"hello!"` → `hello`).
  - Convert all words to lower‑case for case‑insensitive counting.

- **Concurrency**
  - Use Java’s concurrency utilities (`java.util.concurrent`) to process the file in parallel.
  - Design a solution that safely updates the shared word counts (e.g., using `ConcurrentHashMap`, `LongAdder`, or other thread‑safe structures).
  - Ensure that the program scales with the number of available CPU cores.

- **Result output**
  - Print the top **N** words, each on a separate line in the format: `<word>: <count>`.
  - If the file contains fewer than **N** distinct words, output all of them.
  - Sort primarily by descending frequency, secondarily by alphabetical order.

- **Performance**
  - The solution should handle files larger than available RAM without running out of memory.
  - Aim for a time complexity close to **O(file size / #cores)**, with minimal synchronization overhead.

## Bonus  

- **Streaming mode**: Extend the program to accept input from `stdin` (e.g., piped data) in addition to a file path.
- **Unicode support**: Properly handle words containing Unicode letters (e.g., accented characters) while still normalizing case.
- **Memory profiling**: Implement a feature that reports peak memory usage after processing.
- **Configurable delimiters**: Allow the user to specify additional characters to be treated as word boundaries via an optional command‑line flag.