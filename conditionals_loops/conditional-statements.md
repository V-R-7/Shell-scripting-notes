# Conditional Statements in Bash

Bash provides conditional statements such as - if, if else, Else If ladder,Nested if, Switch. 

Explanation :

## if statement

Syntax:
```
if [ conditional expression ]
then
    statement
fi
```
Example:

Lets check if entered number is even using if statement 
```
read input
reminder=$(( $input % 2 ))
if [ $reminder -eq 0 ]
then
echo "$input is even number"
fi
```
## if else statement
  

Syntax:

```
if [ conditional expression ]
then
    statement
else
    statement
fi
```

Example:
To check a number is odd or even 

```
read input
reminder=$(( $input % 2 ))
if [ $reminder -eq 0 ]
then
echo "$input is even number"
else
echo "$input is odd number"
fi
```
