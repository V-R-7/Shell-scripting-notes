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
## Else if ladder

Syntax:

```
if [ conditional expression ]
then
   statement
elif [conditional expression ]
then
   statement
else
   statement
fi
```

Example:
Given 2 input numbers,to check if the input x is greater or lesser or equal than input y.

```
read X
read Y
if (($X  >  $Y))
then echo "X is greater than Y"
elif (($X  <  $Y))
then echo "X is less than Y"
else 
echo "X is equal to Y"
fi
```

## Nested if 

Syntax:
```
if [ conditional expression ]
then
   statement
else
   if [ conditional expression ]
   then
      statement
   fi
fi
```

Example:

To check if entered input year is leap year or not
```
echo -n "Enter year (YYYY): "
read year
if [ `expr $year % 4` -eq 0 ]
then
   if [ `expr $year % 100` -ne 0 ]
   then
   echo "$year is a leap year"
   else
       if [ `expr $year % 400` -eq 0 ]
       then
       echo "$year is a leap year"
       else
       echo "$year is not a leap year"
       fi
   fi
else
    echo "$year is not a leap year"
fi
```

## Switch statements  

Syntax:

```
case  in
   Pattern 1) Statement 1;;
   Pattern n) Statement n;;
esac
```
Example:
Given an input check the manufacturing location 

```
read -p "Enter the name of your TWS headset brand: " tws

case $tws in

  Apple)
    echo -n "${tws}'s TWS headsets are made in the California."
    ;;

  Boat | BOULT | Noise)
    echo -n "${tws}'s TWS headsets are made in India."
    ;;

  *)
    echo -n "${tws} is an unknown brand"
    ;;

esac
```
