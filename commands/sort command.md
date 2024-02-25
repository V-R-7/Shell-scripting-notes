# Sort Command 

The sort command in Bash is used to sort the lines of a text file or standard input alphabetically or numerically.

Syntax: 

```

sort [options] [file]

```
If no file is provided, sort reads from standard input. Here are some common options:

-r: Reverse the result of comparisons.
-n: Sort numerically.
-f: Perform a case-insensitive sort.
-u: Output only unique lines.

Examples:

1) To sort a file named names.txt alphabetically:

```

sort names.txt

```

2) To Sort a file named number numerically:

```

sort -n numbers.txt

```

3) To sort a file in reverse order:

```

sort -r data.txt

```

4) To sort a file case-insensitively:

```

sort -f text.txt

```

5) To Sort and remove duplicate lines:

```

sort -u file.txt

```

 
