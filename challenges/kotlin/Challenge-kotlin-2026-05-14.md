# Challenge: Kotlin Adventure – Detecting Duplicate Files

## Difficulty
Medium

## Description
You are tasked with writing a **Kotlin** program that scans a directory (including all its sub‑directories) and identifies groups of files that have identical content.  

Two files are considered duplicates if **every byte** in one file matches the corresponding byte in the other file, regardless of their names or locations.  

Your program should output each group of duplicate files as a list of absolute file paths, one group per line. The order of groups and the order of paths inside a group does not matter.

*Example output (formatting shown for clarity):*

```
/home/user/docs/report.pdf
/home/user/backup/report_copy.pdf

/home/user/music/song.mp3
/home/user/old_music/song_duplicate.mp3
/home/user/temp/song_backup.mp3
```

In the example above, the first two files are duplicates of each other, and the three MP3 files form another duplicate set.

## Requirements
- Accept a single command‑line argument: the absolute or relative path to the directory to scan.
- Recursively traverse the directory tree, processing **regular files only** (ignore symbolic links, directories, sockets, etc.).
- Use Kotlin idiomatic constructs (e.g., data classes, extension functions, sequences) where appropriate.
- Implement an efficient duplicate‑detection strategy:
  - First, group files by size (files of different sizes cannot be duplicates).
  - For files of the same size, compare a short hash of the first few kilobytes (e.g., MD5 of the first 4 KB) to quickly narrow candidates.
  - Finally, for remaining candidates, compare the full content byte‑by‑byte (or compute a full hash) to confirm duplicates.
- Print each group of duplicates separated by a blank line. If a file has no duplicate, it should **not** be printed.
- Handle errors gracefully (e.g., unreadable files) by printing a warning to `stderr` but continuing the scan.
- The program must run on the JVM with Kotlin 1.8+ and should not require any third‑party libraries beyond the Kotlin standard library (you may use `java.security` classes from the JDK).

## Bonus
- Add an optional command‑line flag `--delete` that, after listing the duplicate groups, deletes **all but one** file in each group (keep the first file listed). Prompt the user for confirmation before deleting each group.
- Support an additional flag `--min-size <bytes>` to ignore files smaller than the given size.
- Produce the output in JSON format when the flag `--json` is provided, e.g.:

  ```json
  [
    ["/path/to/file1", "/path/to/file2"],
    ["/path/to/other1", "/path/to/other2", "/path/to/other3"]
  ]
  ```

- Write unit tests using Kotlin’s `kotest` or `junit` to verify the core duplicate‑detection logic.