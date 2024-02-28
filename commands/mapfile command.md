# mapfile command

The mapfile command in Bash is used to read lines from the standard input into an indexed array variable. Here are some key points based on the search results:

Syntax:

```
mapfile [options] [array]

```

Options:
- -d delim: Specifies the delimiter to terminate lines instead of newline.
- -n count: Copies at most a specified number of lines.
- -O origin: Begins assigning to the array at a specific index.
- -s count: Discards the first specified number of lines read.
- -t Removes a trailing delimiter from each line read.
- -u fd: Reads lines from a file descriptor instead of standard input.
- -C  Evaluate callback each time quantum lines are read. The -c option specifies quantum.

Example:

1) Reading Lines from a File into an Array:

Suppose you have a file named data.txt containing lines of text:
```
# Inside data.txt 
apple
banana
orange
```

```

mapfile -t myarray < data.txt

```
This command reads the lines from data.txt into the myarray array, removing trailing newline characters with the -t option.

2)  Skip the first line of an Array

Suppose you have a file named fruits.txt containing the following lines:

```
# Inside file fruits.txt
apple
banana
orange
grape
```

```
# Use mapfile to read lines from fruits.txt, skipping the first line, and store them in myarray
mapfile -t -s 1 myarray < fruits.txt
```
Now once we print the myarray 

```
# Print the elements of myarray
for element in "${myarray[@]}"; do
    echo "$element"
done

# Output: 
banana
orange
grape
```
In this above script:
- -t is used to remove trailing newline characters.
- -s 1 skips the first line of fruits.txt.

3)  To read n number of lines from the array.

Let us consider the above fruits.txt which has all 4 fruits.

```
# Use mapfile to read the first three lines from fruits.txt into myarray
mapfile -t -n 3 myarray < fruits.txt
echo "${myarray[@]}"
```

```
# Output
apple banana orange
```

Note :  If count is 0, all lines are copied.
