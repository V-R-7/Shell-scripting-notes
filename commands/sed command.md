# sed Command  

sed ("stream editor") is a Unix utility that parses and transforms text, using a simple, compact programming language. 

The sed command in Linux is a stream editor that can perform various text transformations on an input stream (a file or input from a pipeline). 

It’s commonly used for text substitutions, particularly with regular expressions.

For more complex tasks, sed can handle multiple lines, perform global replacements, and even execute commands based on pattern matching. 

It’s a powerful tool for scripting and data manipulation in Unix-like environments.

Syntax:

```

sed [OPTIONS] 'COMMAND' [FILE...]

```
- OPTIONS - Modify how sed operates. Common options include -i for editing files in place and -e to add multiple commands.
- COMMAND - The sed command to execute, such as s for substitution.
- FILE… - One or more files to process with sed. If no file is specified, sed reads from the standard input.

Examples:

A basic example of using sed to replace the first occurrence of “unix” with “linux” in a file:

```

sed 's/unix/linux/' filename.txt

```
Explanation:
- sed: This invokes the stream editor utility for filtering and transforming text.
- 's/unix/linux/': This part is the actual instruction to sed:
  - s: The substitute command, indicating that a substitution needs to be made.
  - unix: The pattern to search for within the text. sed will look for this exact string.
  - linux: The replacement string. Whenever sed finds ‘unix’, it will replace it with ‘linux’.

The slashes / are delimiters that separate the different parts of the substitution command.
filename.txt: This specifies the file on which the sed command will operate.



