# Challenge: **Pythonic Text Analyzer**

## Difficulty  
Medium

## Description  
You are given a plain‑text file containing an English article. Write a Python program that reads the file and produces a report with the following information:

1. **Word count** – total number of words.  
2. **Sentence count** – total number of sentences. A sentence ends with a period (`.`), exclamation mark (`!`) or question mark (`?`).  
3. **Top 5 most frequent words** – ignoring case and punctuation, list the five words that appear most often, along with their frequencies.  
4. **Average word length** – rounded to two decimal places.  
5. **Palindromic words** – a list of unique words that read the same forward and backward (e.g., “level”), ignoring case.

The program should output the report in a readable format to the console.

## Requirements  
- The program must accept the path to the input text file as a command‑line argument.  
- Use only the Python Standard Library.  
- Handle punctuation (commas, semicolons, quotes, etc.) so that words are counted correctly.  
- Treat words case‑insensitively for counting and for detecting palindromes.  
- The output should be clearly labeled, e.g.:

```
Word count: 1245
Sentence count: 78
Top 5 words:
  1. the – 85
  2. and – 73
  3. to – 68
  4. of – 55
  5. a – 49
Average word length: 4.27
Palindromic words: level, civic, radar, madam, refer
```  

- If the file cannot be read (e.g., it does not exist), print a user‑friendly error message.

## Bonus  
- Add an optional command‑line flag `--ignore-common` that, when provided, excludes a predefined list of common English stop words (e.g., “the”, “and”, “of”, “to”, “a”, “in”, “that”, etc.) from the top‑5 word calculation.  
- Allow the user to specify a custom list of stop words via an additional command‑line argument (path to a text file with one stop word per line).  
- Output the report to a JSON file when a `--output <filename>` flag is supplied, while still printing the human‑readable version to the console.  