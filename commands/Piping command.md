# Piping Command

Piping commands in Linux refers to the practice of taking the output of one command and using it as input for another command.

The pipe symbol '|' is used to connect the output of one command to the input of another command.

Syntax:

```

command1 | command2

```

In the syntax:

command1 generates some output.
command2 takes that output as input and processes it further.

Example:

```

ls | grep "example"

```
In the above example:
- ls lists the contents of the current directory.
- grep "example" filters the output of ls to display only the lines containing the word "example".

You can chain multiple commands together using pipes, creating complex command sequences that perform various tasks efficiently.

