# Lab Report 4: "Done Quick" Competition

## Step 1: Log into ieng6
![Image](images/Screenshot-(74).png)
Keys pressed:

`<up><enter>`

I set up the commands so that logging into ieng6 was the first command in my history. I recalled it and entered it, logging in without a password. The command for this is `ssh cs15lwi23aem@ieng6.ucsd.edu`.

## Step 2: Clone your fork of the repository from your Github account
![Image](images/Screenshot-(75).png)
Keys pressed:

`<up><enter>`

Again, I set up the command to clone the GitHub repository so it was in the history. The repository is then cloned onto my ieng6 account using the command `git clone git@github.com:panic360/lab7.git`. 

## Step 3: Run the tests, demonstrating that they fail
![Image](images/Screenshot-(76).png)
Keys pressed:

`cd lab7 <enter><up><up><up><enter><up><up><up><up><enter>`

First, I enter the folder by manually typing `cd lab7`. Then I access through my history `javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java`, which compiles all java files in the folder. Then I access the command `java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore TestListExamples` which runs the testers, demonstrating failure.

## Step 4: Edit the code file to fix the failing test
![Image](images/Screenshot-(77).png)
Keys pressed:

`<up><up><up><up><up><enter><down><right><delete> 2 <^o><enter><^x>`

I access the command `nano ListExamples.java` which opens a text editor in bash. I then navigate to the line requiring fixing, and replace the 1 with a 2. I use ctrl+o and ctrl+x to save and exit the editor.

## Step 5: Run the tests, demonstrating that they now succeed
![Image](images/Screenshot-(78).png)
Keys pressed:

`<up><up><up><enter><up><up><up><enter>`

This recalls the same commands as step 3, recompiling and rerunning the JUnit tests to show that they work now.

## Step 6: Commit and push the resulting change to your Github account (you can pick any commit message!)
![Image](images/Screenshot-(79).png)
Keys pressed:

`git add List<tab>java <enter> git commit <enter> fixed <esc> :wq <enter> git push`

The last commands I knew well enough to type quickly, so I manually entered the final commands to push to GitHub. `git add` ensures ListExamples.java would be updated, `git commit` opened VIM in which I added a commit note and exited with ":wq", and `git push` uploaded to GitHub. Overall, the whole process took a little over a minute.
