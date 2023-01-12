# How to Log into a Course-Specific Account on `ieng6`

## 1. Set up your course-specific account
The first step to getting connected is to ensure that your course-specific account is properly set up. Visit the [lookup page](https://sdacs.ucsd.edu/~icc/index.php) for your account and enter your credentials. Click on the course-specific account and follow the instructions to set up a password.

## 2. Install `Git` and `Visual Studio Code`
In order to remotely connect, we will use `git bash` in the terminal of `Visual Studio Code`. Use the links below to install both of these applications according to your operating system.

Visual Studio Code: https://code.visualstudio.com/

Git for Windows: https://gitforwindows.org/

Once installed, follow [these instructions](https://stackoverflow.com/a/50527994) to open git bash in the Visual Studio Code terminal. Once completed, your visual studio window should look something like this:

![Image](Screenshot_20230112_092822.png)

## 3. Connect to the remote server
Now it's **TIME**. We will use the `ssh` (secure shell) command to connect to the remote server. Type the command below into the terminal, replacing `zz` with the letters in your account.

`$ ssh cs15lwi23zz@ieng6.ucsd.edu`

You may be prompted with a warning making sure you want to connect. If this is the case, enter **yes**. I didn't get a warning because I've already connected before. When done properly, the terminal should end like this, asking for a password.

![Image](Screenshot_20230112_094241.png)

Finally, enter the new password you initialized when setting up your account. If you just set the password up, it might take some time to update (it did for me). This can take up to 15 minutes. When you're finally connected, this is what your output should look like:

