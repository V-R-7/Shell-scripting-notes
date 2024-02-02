# tr Commands 

The 'tr' command is a useful translation utility in linux.

The tr command in Unix-like operating systems is a command-line utility for translating or deleting characters.
It's a simple yet powerful tool that can be used for a variety of text manipulation tasks.

Syntax:

```

tr [options] set1 [set2]

```

- set1: A set of characters that you want to replace or delete.
- set2: A set of characters that will replace the characters in set1.

Note : If set2 is not provided, tr will only perform deletion or squeezing characters.

Some common options include:

-d: Delete characters in set1.
-s: Squeeze repeating characters in set1 to single characters.
-c: Complement set1 (replace characters not in set1).
-t: Translate using set1 and set2 strings of different lengths.

Examples:

i) To replace all occurrences of 'a' with 'b' in a text file,

```

cat file.txt | tr 'a' 'b'

```

ii) To delete all occurrences of 'a' from a text file:

```

cat file.txt | tr -d 'a'

```

iii) To translate all uppercase characters to lowercase:

```

cat file.txt | tr 'A-Z' 'a-z'

```

iv) To squeeze repeating characters:

```

echo "hellooo" | tr -s 'o'

```
In the above command, it will execute the output as :

-> the output string becomes "hello".


v) To complement a set:

```

echo "abcdefg" | tr -c 'aeiou' 'X'

```

In this above command:

All characters that are not vowels ('a', 'e', 'i', 'o', 'u') will be replaced by 'X'.
So, the output of this command will be 'aXeX', because only 'a' and 'e' are vowels and the rest ('b', 'c', 'd', 'f', 'g') will be replaced by 'X'.


