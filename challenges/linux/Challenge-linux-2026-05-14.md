# Challenge: Linux Log Analyzer

## Difficulty
Medium

## Description
Write a command‑line program that parses a typical Linux system log file (e.g., `/var/log/syslog` or `/var/log/auth.log`). The program should read the log, extract relevant information from each entry, and produce a summary report.

The log entries follow the general format:

```
<Month> <Day> <Time> <Hostname> <ProcessName>[PID]: <Message>
```

Your program must:

1. Count the total number of log entries.
2. Count how many entries belong to each distinct process (identified by `ProcessName`).
3. Identify the earliest and latest timestamps present in the file.
4. Detect and list any lines that do **not** conform to the expected format.

The summary report should be printed to standard output in a clear, human‑readable form.

## Requirements
- The program must accept the path to the log file as a command‑line argument.
- It should handle large files efficiently (i.e., without loading the entire file into memory at once).
- Timestamps must be parsed correctly, taking into account that the year is not present in the log entry (assume the current year).
- Output must include:
  - Total number of entries processed.
  - A table (or list) showing each `ProcessName` with the corresponding entry count, sorted descending by count.
  - The earliest and latest timestamps (displayed as `YYYY-MM-DD HH:MM:SS`).
  - A count of malformed lines, and optionally the line numbers of those lines.
- The program should exit with a non‑zero status code if the supplied file cannot be opened or read.

## Bonus
- Add an optional flag (`-j` or `--json`) to output the summary report in JSON format.
- Support processing multiple log files at once, aggregating the results across all files.
- Include an option to filter the report by a specific `ProcessName` (e.g., only show counts for `sshd`).
- Detect and report the most frequent log level (e.g., `INFO`, `WARN`, `ERROR`) if such a field exists in the message.