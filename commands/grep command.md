# grep command

Grep, short for "global regular expression print"

Syntax:

```

grep [options] pattern [file...]

```
- pattern: The pattern you want to search for. It can be a simple string or a regular expression.
- file...: The file or files in which you want to search. If no file is provided, grep reads from standard input 
           (usually through a pipe).

Some common options for grep include:

- -i: Ignore case distinctions.
- -r: Recursively search subdirectories.
- -v: Invert the match, select non-matching lines.
- -E: Interpret the pattern as an extended regular expression.
- -n: Display line numbers along with the lines.
- -c: Display count of matching lines instead of the lines themselves.

Examples:

```
grep "pattern" file.txt      # Search for "pattern" in file.txt
grep -i "pattern" file.txt   # Search case-insensitively for "pattern" in file.txt
grep -r "pattern" directory  # Recursively search for "pattern" in files under the directory
grep -E "pattern1|pattern2" file.txt  # Use extended regular expression to search for pattern1 or pattern2
grep -v "pattern" file.txt   # Show lines that do not match "pattern" in file.txt
```
