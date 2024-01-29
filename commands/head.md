# head Command

It is used to display the first few lines of a text file or standard input (keyboard input) to the terminal. 

By default, it displays the first 10 lines of the specified file.

Syntax:

```
head [options] [file(s)]
```

Common options include:

- -n N: Display the first N lines of the file instead of the default 10.
- -c N: Display the first N bytes of the file instead of the first 10 lines.
- -q: Never print filename headers.
- -v: Always print filename headers.

## Example:

i) To display first 10 lines of a file named example.txt:

```
head example.txt

```

ii) To display the first 5 lines of a file named data.txt:

```
head -n 5 data.txt

```

iii) To display the first 100 bytes of a file named binary_file.bin:

```
head -c 100 binary_file.bin

```

