# Variables

Variables are necessary for the storage or modification of data.


## Types of variables

- Environmental variables
- User-defined variables

## Declare a variable

Let's review some things to remember about variables before declaring them.

- A variable is case-sensitive.
  
  for eg: it implies that tempvar and TempVar will be considered different variables.
- Variable names can have letters, numbers, underscores, and digits.
- Try to use relevant and meaningful names for your variables.
- Whenever creating a variable or modifying its value, the $ symbol is not necessary, just the actual name of the variable is enough.

- Avoid using names such as reserved bash keywords.
- Between the variable name and value, there should not be a space.

Eg:
There should be no space between variable name and value, below example is not valid.

```
#!/bin/bash

jersey_number = 7
```
Declaration with name and value without space is preferred.

```
#!/bin/bash

jersey_number=7 
```
## Accessing Bash variables

Let us consider above example, accessing the variable jersey_number and print it.

There are two ways to access the bash variables :
- $ variable_name
- $ {variable_name}

The first method is the $ symbol followed by the variable name.

The second method is the $ symbol followed by the curly braces {} and within itself the variable name.


```
jersey_number=7 
echo My jersey number is $jersey_number
```
```
jersey_number=7 
echo My jersey number is ${jersey_number}
```


In the above sample code, I printed using the keyword echo. and it will resulted as below for both the cases.
```
Output

My jersey number is 7

```

### Modify the value of the variable

Re-assign any value to the variable again.

```

jersey_number=7 
echo My jersey number is ${jersey_number}

Output
My jersey number is 7

```
In the above code, let's change jersey_number to 11.
```
jersey_number=11 
echo My jersey number is ${jersey_number}

Output
My jersey number is 11

```

## The declare command

Bash doesn't have explicit data types, so to be aware of the variable data types we can 
use the declare command.

The declare command can be used to create a variable with a specific data type or check the type of variable.

Example: if we want to create a variable with int data type,  then use the declare command with the -i flag.

```
declare -i jersey_number
```

```
jersey_number=11 
echo ${jersey_number}

Output
11

```

Now if we change this value of the variable it will throw out an error.

```
jersey_number=11.5 
echo ${jersey_number}

Output
syntax error: invalid arithmetic operator (error token is ".14")

```
## Environmental variables

The built-in variables are termed environmental variables,
these are part of the environment and are accessible to processes.

Let's see some of the common Environmental variables.

- SHELL  - specifies the user's default shell (Example: /bin/bash)
- PWD    - represents the current working directory (Example: /root)
- PATH   - to view the current directory which is searched for executable programs
- USER   - indicates the current username
- LOGNAME  - indicates the current username




