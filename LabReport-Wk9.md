
# Lab Report 5: Exploring the `awk` Command in Git Bash

The following file, `test-data.txt`, will be used in all the commands shown.
```
Name    Age Date
Myers   24  4.23.10
Lyles   18  9.10.22
Thompson    10  2.5.11
Indred  49  5.16.16
```

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

```

Citations:
All commands were found using
https://www.geeksforgeeks.org/grep-command-in-unixlinux/
ChatGPT was used for my own understanding.
