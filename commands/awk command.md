# awk command 

awk is a powerful text processing utility available in Unix and Unix-like operating systems.

It is primarily used for pattern scanning and processing. 

The name "awk" comes from the initials of its designers: Alfred Aho, Peter Weinberger, and Brian Kernighan.

Functionality:

- Pattern-based processing: Awk scans through a file line by line, searching for lines that match a specific pattern you provide using regular expressions.
- Field manipulation: It can break down each line into separate fields (usually based on delimiters like spaces or tabs) and then perform actions on those fields.
- Data filtering: You can use Awk to filter out specific lines based on patterns or perform actions only on lines that meet certain criteria.
- Data transformation: Awk allows you to modify the contents of the data, like adding elements, deleting information, or reformatting fields.
- Reporting and analysis: It's useful for generating reports and summaries from text data by selecting and formatting specific fields.

Syntax:

```

awk 'pattern { action }' input_file

```
- pattern is an expression that determines whether a particular action should be taken on a line.
- action is the set of commands or operations to be executed if the pattern is matched.
- input_file is the file(s) that awk will process.

 Example:

 Suppose you have a file called data.txt with the following content:

```
Alice 25
Bob 30
Charlie 35
```
To print the names and ages from this file, You can use awk :

```

awk '{ print $1, $2 }' data.txt

```
Explanation:

'{ print $1, $2 }': specifies the action to be performed by awk. In this case, it tells awk to print the first ($1) and second ($2) fields of each line.

It results as same as the data.txt file as we print both the fields using awk.



