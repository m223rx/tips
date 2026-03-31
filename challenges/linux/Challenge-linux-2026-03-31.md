# Challenge: Linux File Permission Analyzer

## Difficulty
Medium

## Description
Create a command‑line utility that scans a given directory and reports the permission settings of each file and sub‑directory within it. The program should display the results in a clear, tabular format showing the file name, type (file, directory, symbolic link, etc.), octal permission value, and a symbolic representation (e.g., `rwxr-xr--`).  

The tool must handle invalid input gracefully, support optional flags for filtering results, and be usable on any Unix‑like system that follows standard POSIX file permission semantics.

## Requirements
- Accept a directory path as a required positional argument. If omitted, use the current working directory.
- For each entry in the target directory, output:
  1. **Name** – the file or directory name (relative to the target directory).
  2. **Type** – one of `file`, `directory`, `symlink`, `socket`, `fifo`, `block`, `char`.
  3. **Octal** – the numeric permission bits (e.g., `0755`).
  4. **Symbolic** – the classic `rwxrwxrwx` string, using `-` for absent bits.
- Sort the output alphabetically by name.
- Provide a `-r/--recursive` flag to walk through sub‑directories and list their contents as well, preserving the relative path.
- Provide a `-e/--exclude <pattern>` option that can be supplied multiple times to skip files matching a shell‑style glob pattern (e.g., `*.log`).
- Provide a `-t/--type <type>` option to limit output to a specific file type (e.g., `file`, `directory`).
- Print a helpful usage message when invoked with `-h` or `--help`.
- Return a non‑zero exit code if the supplied path does not exist, is not readable, or another unrecoverable error occurs.

## Bonus
- Add a `-s/--sort <field>` flag allowing sorting by `name`, `type`, `octal`, or `symbolic`.
- Color‑code the output: directories in blue, executable files in green, symlinks in cyan, and others in default colour.
- Include an option `-c/--count` that, after listing entries, prints a summary of how many items of each type were found.
- Detect and display the presence of setuid, setgid, and sticky bits in the symbolic representation (e.g., `rwsr-xr-x` or `rwxrwxrwt`).