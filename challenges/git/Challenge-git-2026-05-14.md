# Challenge: Git Repository Analyzer

## Difficulty
Medium

## Description
You are given the path to a local Git repository. Your task is to write a program that analyzes the repository's commit history and generates a concise report containing useful statistics about the project's development.

The program should:

1. Walk through the entire commit history (including merges) of the default branch (e.g., `main` or `master`).
2. Collect data about authors, commit frequencies, file changes, and other useful metrics.
3. Output a human‑readable report (plain text or Markdown) that summarizes the findings.

The goal is to demonstrate proficiency with interacting with Git programmatically (e.g., using command‑line Git, libgit2 bindings, or a language‑specific Git library) and to process and aggregate data efficiently.

## Requirements
- Accept a single command‑line argument specifying the path to the target Git repository.
- Detect the default branch automatically (fall back to `master` if detection fails).
- Produce a report that includes at least the following sections:
  1. **Overall Summary**
     - Total number of commits.
     - Date of the first and most recent commit.
  2. **Author Statistics**
     - List of all authors sorted by the number of commits (descending).
     - For each author: total commits, first commit date, last commit date, and average commits per month.
  3. **Commit Activity**
     - Commits per month for the past 12 months (displayed as a simple table or histogram).
  4. **File Change Summary**
     - Top 10 most frequently changed files (by number of commits they appear in).
     - Total lines added and removed across the entire history.
  5. **Merge Statistics**
     - Total number of merge commits.
     - Percentage of commits that are merges.
- The program must handle repositories with large histories efficiently (e.g., by streaming output from Git rather than loading everything into memory at once).
- If the provided path is not a Git repository, display a clear error message.

## Bonus
- Include a **Contributor Heatmap** that visualizes each author's activity over time (e.g., a matrix with dates on the X‑axis and authors on the Y‑axis, using simple characters like `█` for activity levels).
- Detect and list **renamed or moved files** that appear in the top‑10 changed files, showing both old and new paths.
- Provide an option `--json` that outputs the same report in JSON format for downstream tooling.
- Allow the user to specify a custom branch name to analyze instead of the default.
- Implement caching: if the repository hasn't changed since the last run, reuse the previous report to avoid recomputation.