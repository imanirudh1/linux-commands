## Shuf command tutorial with examples
Tutorial on using shuf, a UNIX and Linux command for generating random permutations. Examples of shuffling the lines in a file, picking a random line and shuffling standard input.

Estimated reading time: 2 minutes
### Table of contents

    What is the shuf command in UNIX?
    How to shuffle the contents of a file
    How to pick a random line from a file
    How to shuffle standard input
    Further reading
```
shuf man page
```
### What is the shuf command in UNIX?

The shuf command generates random permutations from input lines to standard output. If given a file or series of files it will shuffle the lines and write the result to standard output. It can also limit the number of results returned supporting selecting random lines from a file or data from a list.
How to shuffle the contents of a file

To shuffle the lines in a file using the shuf command pass a file, files or standard input to the command. The result will be printed to standard output. In the following example we have a list of cards in a file saved as cards.txt. This file is ordered by suit and number.
```
shuf cards.txt
4D
9D
QC
3S
6D
```
The shuf command shuffles the lines and outputs this to standard output.
How to pick a random line from a file

To pick a random line from a file using shuf use the -n option. This limits the output to the number specified.
```
shuf -n 1 cards.txt
KH
```
To select more than one line change the number.
```
shuf -n 5 cards.txt
4H
9S
KH
9D
9H
```
### How to shuffle standard input

To shuffle words passed to shuf in standard input use the -e option. This shuffles items separated by spaces.
````
shuf -e one two three
three 
two 
one
```
If you wanted to quickly decide whose turn it is to make the tea you can use shuf.
```
shuf -n 1 -e George Kirsten Fin Bea
Bea
```
