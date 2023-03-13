
# Lab Report 5: Exploring the `awk` Command in Git Bash

The following file, `test-data.txt`, will be used in all the commands shown.
```
Name    Age Date
Myers   24  4.23.10
Lyles   18  9.10.22
Thompson    10  2.5.11
Indred  49  5.16.16
```

## Ability 1: Separating input lines finto fields
Ex. 1
```
$ grep -r "france" .
./patterns.txt:france
./travel_guides/berlitz1/WhereToFrance.txt:        Maison de la France Web site (<www.franceguide.com>) is also a 
```
The `-r` option searches the given directory recursively without relying on wildcard patterns. Here it is recursively searching the working directory for files containing the word "france" (patterns.txt is a file I created for the lab).

Ex. 2
```
$ grep -r -l "large" non-fiction
non-fiction/OUP/Abernathy/ch1.txt
non-fiction/OUP/Abernathy/ch14.txt
non-fiction/OUP/Abernathy/ch15.txt
non-fiction/OUP/Abernathy/ch2.txt
non-fiction/OUP/Abernathy/ch3.txt
non-fiction/OUP/Abernathy/ch6.txt
non-fiction/OUP/Abernathy/ch7.txt
non-fiction/OUP/Abernathy/ch8.txt
non-fiction/OUP/Abernathy/ch9.txt
```
...

Here the same option is searching the relative `non-fiction` directory for the word "large". I used the -l option to just list file names. Again, the given I will be using it throughout the lab to demonstrate further commands.

Citations:
All commands were found using
https://www.geeksforgeeks.org/grep-command-in-unixlinux/
ChatGPT was used for my own understanding.
