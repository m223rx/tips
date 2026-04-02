# Challenge: Log Summarizer in Bash

## Difficulty
Medium

## Description
You are given a directory containing multiple log files. Each log file follows the format:

```
[YYYY-MM-DD HH:MM:SS] [LEVEL] Message text...
```

Where `LEVEL` can be one of `INFO`, `WARN`, `ERROR`, or `DEBUG`. Your task is to write a **bash** script that scans all `.log` files in the directory (including sub‑directories) and produces a summary report.

The report should include:

1. The total number of log entries processed.
2. The count of entries for each log level.
3. The earliest and latest timestamps found across all logs.
4. A list of unique messages that appear more than once, along with their occurrence count.

The script should output the summary to `stdout` in a human‑readable format.

## Requirements
- The script must be a single executable Bash file (e.g., `summarize_logs.sh`).
- It must accept an optional command‑line argument specifying the root directory to scan. If omitted, the current working directory is used.
- Only files with the `.log` extension should be processed.
- The script should handle large log files efficiently (avoid loading entire files into memory when possible).
- All timestamps must be parsed and compared correctly, assuming they are in the same timezone.
- The output format should be clear and well‑structured, for example:

  ```
  Total entries: 12345
  INFO:  8000
  WARN:  2500
  ERROR: 1500
  DEBUG: 345

  Earliest timestamp: 2022-01-01 00:00:05
  Latest timestamp:   2022-12-31 23:59:59

  Repeated messages:
  - "User login succeeded" (23 occurrences)
  - "Connection timed out" (12 occurrences)
  ```

## Bonus
- Add an option (`-o output.txt`) to write the summary to a specified file instead of `stdout`.
- Include a flag (`--level LEVEL`) to filter the summary to a specific log level only.
- Provide a performance metric at the end of the script indicating total execution time.
- Support compressed log files (`.log.gz`) in addition to plain `.log` files.