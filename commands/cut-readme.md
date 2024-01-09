# Cut Command

The cut command in Linux is used to extract specific sections (columns) from each line of a file or from a stream of input.

Basically the cut command slices a line and extracts the text.

## Syntax:

```
cut OPTION... [FILE]...
```

Example:
To cut the characters 2-5 from each line of a file called hello, existing the file contents contains below.

```
$ cat hello.txt

#output
Hello
World
how are you

```

```
# lets cut the character 2-5 from each line of a file
cut -c2-5 hello.txt

#output
ello
orld
ow a

```

Now, with the options 
-  -b (byte)        : It selects the specified bytes from each line and prints the result.
-  -c (character)   : Select only these characters.
-  -f (field)       : Select specific fields (columns) from each line of a file. ( cut uses tab as a default field delimiter & Space is not considered as delimiter in UNIX)
-  –-complement     : Complement the set of selected bytes, characters, or fields (this option can be used in the combination with other options either with -f or with -c.)
                    --complement option negates the selection, meaning it selects everything that is not specified in the field or byte list.
- –output-delimiter : To specify the delimiter character to be used when printing the output
