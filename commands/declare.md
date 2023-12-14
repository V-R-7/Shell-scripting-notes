# Declare command 

Bash is weakly typed / loosely typed language, it does not require to declare the data type of the variable at the time of declaration.
But Declare command can able to declare the data type of the variable.

## Syntax :

declare [options] [name[=value]] [name[=value]] ...

This command can be used with an option or without an option to declare one or more variables &
option in the above command will be able to declare the type of the variable.

Example:

```
declare -i x=10

```

In the above example, we have declared an integer variable x which holds value 10.

Different options available with Declare 

| Command | Description |
| --- | ----------- |
| -i | Declare as integer variable |
| -p | Print the attributes and options of variable |
| -l | Declare as lower case letters in variable |
| -u | Declare as upper case letters in variable |
| -a | Declare an indexed array |
| -A | Declare an associative array |
| -f | Declare a bash function |
| -F | Print the name of the function and attributes |
| -n | Declare a variable that references another variable |


