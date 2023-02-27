# Lab Report 4: "Done Quick" Competition

## Step 1: Log into ieng6
![Image](images/Screenshot-(74).png)
Commands executed:

`<up><enter>`

I set up the commands so that logging into ieng6 was the first command in my history. I recalled it and entered it, logging in without a password. The command for this is `ssh cs15lwi23aem@ieng6.ucsd.edu`.

## Step 2: Clone your fork of the repository from your Github account
![Image](images/Screenshot-(75).png)

Commands executed:

`<up><up><enter>`

Again, I set up the command to clone the GitHub repository so it was in the history. The repository is then cloned onto my ieng6 account using the command `git clone git@github.com:panic360/lab7.git`. 

## Step 3: Run the tests, demonstrating that they fail
![Image](images/Screenshot-(76).png)

`<up><up><up><enter><up><up><up><up><enter>`

The first command I access through my history is `javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java`, which compiles all java files in the folder. Then I access the command `java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore TestListExamples` which runs the testers, demonstrating failure.
