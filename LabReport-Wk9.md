
# Lab Report 5: Exploring the `awk` Command in Git Bash

The following file, `test-data.txt`, will be used in all the commands shown.
```
Name    Age Date
Myers   24  4.23.10
Lyles   18  9.10.22
Thompson    10  2.5.11
Indred  49  5.16.16
```
I explored awk's capabilities, rather than its options, because its options are quite limited. 
The most basic awk commands contain a "pattern", followed by an "action". These are both contained in single quotes and execute once for every line in a text file.

## Ability 1: Separating input lines finto fields
Ex. 1
```
$ awk '{print $1}' test-data.txt
Name
Myers
Lyles
Thompson
Indred
```
Awk separates terms in each line into numerically named variables which can be accessed using `$0`, `$1`, `$2`. Calling print to sequentially print each line of a text file, references can be made to the first term, for example, to filter out just the first column of the text file. (whitespace is the default separator for the awk command).

Ex. 2
```
$ awk '$1=="Lyles"' test-data.txt
Lyles   18  9.10.22
```

Here, the pattern used checks if the name is equal to the string "Lyles". If it is, awk resorts to the default action, which is printing the relevant line. 

## Ability 2: Useful internal variables
Ex. 1
```
$ awk 'END {print NR}' test-data.txt
5
```

Awk contains several internal variables which provide useful funciton to awk commands. One of these, NR, is incremented every time awk passes a new line. By adding the "END" rule to the command, here NR is used to retrieve the number of lines in the file.

Ex. 2
```
$ awk 'BEGIN {RS="e"} {print}' test-data.txt
Nam
    Ag
 Dat

My
rs   24  4.23.10
Lyl
s   18  9.10.22
Thompson    10  2.5.11
Indr
d  49  5.16.16
```

Here, the BEGIN rule is used to assign the variable RS to "e". RS is the character used to denote a line separation. By changing RS, the input is treated as if records are separated by the letter "e", producing interesting output for the first two lines.

## Ability 3: For loops
Ex. 1
```
$ awk 'BEGIN {for(i=0;i<10;i++) print i}'
0
1
2
3
4
5
6
7
8
9
```
Awk has a built-in for loop that can be used to perform commands with an iteration variable. For example, here a simple for loop is used to print values 1 through 10. The BEGIN tag is necessary to ensure the command only executes once.

Ex. 2
```
$ awk '{for(i=1;i<=6;i+=2) print substr($0,i,1)}' test-data.txt
N
m

M
e
s
L
l
s
T
o
p
I
d
e
```
Here is a more realistic application of the for loop. For every line in the file, a foor loop is executed which prints 3 characters from the line, skipping every other character. The `substr()` function takes a string, start index, and length parameter respectively to produce a substring output. 

## Ability 4: If statements
Ex. 1
```
$ awk '{if($1=="Myers") print}' test-data.txt 
Myers   24  4.23.10
```
Rather than use a pattern to filter out items, if statements can be implemented programatically. Here, an if statement is created that prints a line if its first field equals the string "Myers". 

Ex. 2
```
$ awk '{if($2>21) print}' test-data.txt
Name    Age Date
Myers   24  4.23.10
Indred  49  5.16.16
```
This can be used more realistically to compare fields. Here the field corresponding to age is compared to 21, printing only the lines representing individuals who are older than 21. This could be useful when dealing with large amounts of data to present/ modify data quickly.


Citations:
Info found using:
https://www.geeksforgeeks.org/awk-command-unixlinux-examples/
https://thomas-cokelaer.info/blog/2011/05/awk-the-substr-command-to-select-a-substring/
