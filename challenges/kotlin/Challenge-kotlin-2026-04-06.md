# Challenge: Kotlin Text Analyzer

## Difficulty
Medium

## Description
Write a Kotlin program that reads a paragraph of text from standard input and performs various analyses on the content. The program should output a report containing:

1. **Word Count** – total number of words.
2. **Unique Words** – count of distinct words (case‑insensitive).
3. **Most Frequent Word** – the word that appears the most often (if there is a tie, list any one of them).
4. **Average Word Length** – average length of all words, rounded to two decimal places.
5. **Palindromic Words** – a list of all words that read the same forwards and backwards (case‑insensitive), preserving their original order.

A *word* is defined as a contiguous sequence of alphabetic characters (`a–z`, `A–Z`). All other characters (digits, punctuation, whitespace, etc.) are considered delimiters.

## Requirements
- Read the entire input until EOF.
- Use Kotlin’s standard library functions where appropriate (e.g., `split`, `filter`, `map`, `groupBy`).
- The output format must be exactly as shown in the example below.
- The program should handle large inputs efficiently (up to 10⁶ characters).

### Input
A paragraph of text, possibly spanning multiple lines.

### Output
```
Word Count: <total_words>
Unique Words: <unique_word_count>
Most Frequent Word: <most_frequent_word>
Average Word Length: <average_length>
Palindromic Words: <word1> <word2> ... <wordN>
```

If there are no palindromic words, output `Palindromic Words: None`.

### Example

**Input**
```
Madam Arora teaches malayalam.
She loves programming, and she also loves level design.
```

**Output**
```
Word Count:  fifteen
Unique Words:  twelve
Most Frequent Word: loves
Average Word Length: 5.33
Palindromic Words: Madam Arora malayalam level
```

*(The numbers above are illustrative; your program should compute the exact values.)*

## Bonus
- Implement the solution using Kotlin sequences (`asSequence()`) to minimize intermediate collections.
- Allow the user to specify an optional command‑line argument `--ignore-stopwords` that, when present, excludes common English stopwords (e.g., "the", "and", "is", etc.) from all calculations except the word count.
- Provide unit tests using Kotlin’s `kotlin.test` library to verify each part of the analysis.