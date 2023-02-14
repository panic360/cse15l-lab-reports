# Lab Report 3: Exploring the `grep` Command in Git Bash

## Command 1: `grep -r`
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

## Command 2: `grep -f`
Ex. 1
```
$ grep -r -f patterns.txt .
./patterns.txt:france
./travel_guides/berlitz1/WhereToFrance.txt:        Maison de la France Web site (<www.franceguide.com>) is also a
```
The `-f` option uses the contents of a file to search for in the provided path. I created a file named `patterns.txt`, which contains just the string "berlin". The files listed contain the string

Ex. 2
```
