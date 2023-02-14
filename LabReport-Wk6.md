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
$ grep -r -f patterns.txt .
./patterns.txt:berlin
./patterns.txt:france
./travel_guides/berlitz1/WhereToFrance.txt:        Maison de la France Web site (<www.franceguide.com>) is also a
```
Here is the same command, except I added the string "france" to `patterns.txt` on a new line. There is a new file found, which includes the additional string.

## Command 3: `-o`
Ex. 1
```
$ grep -r -o "fight for everyon" .
./travel_guides/berlitz2/Amsterdam-Intro.txt:fight for everyon
```
This command prints out only the matching part of the matching file, so as not to overflow the terminal. Here I searched for a specific string, which is printed out after the file name on its own. 

Ex. 2
```
$ grep -r -o "whenever" .
./non-fiction/OUP/Abernathy/ch6.txt:whenever
./non-fiction/OUP/Abernathy/ch9.txt:whenever
./non-fiction/OUP/Berk/ch2.txt:whenever
./non-fiction/OUP/Castro/chR.txt:whenever
./non-fiction/OUP/Kauffman/ch4.txt:whenever
./non-fiction/OUP/Kauffman/ch9.txt:whenever
./non-fiction/OUP/Rybczynski/ch1.txt:whenever
./travel_guides/berlitz1/WhereToItaly.txt:whenever
./travel_guides/berlitz1/WhereToMalaysia.txt:whenever
./travel_guides/berlitz2/Bermuda-WhatToDo.txt:whenever
./travel_guides/berlitz2/CostaBlanca-WhatToDo.txt:whenever
./travel_guides/berlitz2/PuertoRico-WhatToDo.txt:whenever
```
Here's another example of the command being used on many files. This could be useful when sharing output with others, as it indicates the specific relevant section of the matching file. 

## Command 4: `-v`
Ex. 1
```
$ grep -v "It is difficult to think" Amsterdam-History.txt




a brief History
The Birth of the Settlement
The Batavians travelled down the Rhine to found the first permanent settlement here. Almost from the start the water had to be controlled, and the tradition of damming and organized diversion of the river and the tides began. It has been a constant source of concern ever since.
```
...
The `-v` command prints the lines that do not match the given string. For this example, the output continues, printing the entire text file omitting the first line which contains the string.

Ex. 2
```
$ grep -v "the" Amsterdam-History.txt




a brief History
From Fishing to Trading
Religious Strife
Towards Independence
Decline and Fall
The 20th Century
The Modern State
```
This is a more interesting example that prints the files contents omitting lines with "the". This could be useful in quickly modifying data files that contain specific known strings. 

Citations:
All commands were found using
https://www.geeksforgeeks.org/grep-command-in-unixlinux/
ChatGPT was used for my own understanding.
