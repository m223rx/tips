# Challenge: Smart File Organizer (Bash)

## Difficulty
Medium

## Description
Create a Bash script that organizes files within a given directory by sorting them into subfolders based on their file extensions. The script should be robust, handle edge cases (such as files without extensions or hidden files), and provide clear feedback to the user about the actions performed.

## Requirements
- The script must accept a single argument: the path to the target directory.
- For each file in the specified directory (non‑recursive by default):
  - Determine its file extension (case‑insensitive).  
  - Move the file into a subdirectory named after the extension (e.g., `txt`, `jpg`).  
  - If the file has no extension, move it into a folder named `no_extension`.
  - Hidden files (those starting with `.`) should be ignored.
- The script should create the necessary subfolders if they do not already exist.
- If a file with the same name already exists in the destination folder, rename the incoming file by appending a numeric suffix (e.g., `file_1.txt`).
- The script must output a summary at the end, showing:
  - Total number of files processed.
  - Number of files moved to each extension folder.
  - Any errors encountered (e.g., permission issues).

## Bonus
- Add an optional flag (`-r` or `--recursive`) to process files in all subdirectories recursively, preserving the original directory hierarchy.
- Provide a `--dry-run` option that prints the actions the script would take without actually moving any files.
- Implement logging: write a detailed log file (`organizer.log`) that records timestamps, performed actions, and any errors.
- Allow the user to specify a custom destination root directory via a second argument. If omitted, the script uses the input directory as the root.