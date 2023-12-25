# Loops

Let's see various types of loops:
- For Loop
- While Loop
- Until Loop

Also we can see about break and continue statement.

## For Loop

The loop will be executed for each items in the list.
Syntax:
```
for variable in list;do
  # Execute statement
done
```
Example:
Print numbersfrom 1 to 5 using for loop.

```
for i in {1..5};do
    echo $i
done
```

## While Loop

The loop will be executed as long as the condition is true.

Syntax:
```
while [ condition ];do
    # Execute statement
done
```
Example:
Print numbers 1 to 5 using a while loop

```
count=1
while[ $count -le 5 ];do
   echo $count
   ((count++))
done
```

## Until Loop

The until loop is executed as many times as the condition/command evaluates too false. 
The loop terminates when the condition/command becomes true. 

Syntax:
```
Until [ condition ];do
    # Execute statement
done 
```
Example:
Print numbersfrom 1 to 5 using Until loop.

```
count=1
until [ $count -gt 5 ];do
    echo $count
   ((count++))
done
```
The loop gets executed until count becomes greater than 5, 
once it's greater than 5 it will be terminated.

## Break statement

It is used to exit a loop prematurely & it is often used within an if statement to check a certain condition & exit the loop.
Example:
```
count=1
while [ $count -le 10 ];do
   echo $count
   if [ $count -eq 5 ]; then
        break # exit the loop when count is 5
   fi
   ((count++))
done
```

## Continue statement

It skips the execution of the loop for only the current iteration. 

Example:
```
for ((i=1; i<=10; i++)); do
  if[ $((i%2)) -eq 0 ]; then
     continue #skip even numbers
  fi
  echo $i
done
```
The above script will print only odd numbers between 1 and 10



