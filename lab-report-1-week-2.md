# Week 2 Lab Report
> Note: I am writing this in the context of the steps  I followed to achieve these points and am writing from the perspective of teaching someone how to do it as well. Each step describes what I did to achieve each goal.

Welcome to my tutorial. On this page, I will guide you through how to:


* Install Visual Studio Code
* Remotely connect to a Remote Computer
* Using basic commands
* Move files using the `scp` command
* Set an SSH Key
* Optimize Remote Running

Follow along!

## Installing Visual Studio Code

In order to download Visual Studio Code, you must first direct yourself to the [Visual Studio Code](https://code.visualstudio.com/) website

> Note that there are different versions of VS code that should be downloaded based off of your device. This tutorial is based off a OSX (Mac) device

Once you click the link, hit the **DOWNLOAD** button and install the application on your device.

Once downloaded, open the application. You should see an a screen like/similar to this:

![Image](VSCodeHome.png)

> This is your **Homepage**.

**Congrats! You have succsessfully downloaded and installed Visual Studio Code!**

---

## Remotely Connect to a Remote Computer

The step walks you through how to remotely connect by logging into your course specific ieng 6 account.

First, click [here](https://sdacs.ucsd.edu/~icc/index.php) to find your CSE15L account log in. Follow the steps prompted  by the site to access your account. 

Open Visual Studio Code and open a new terminal.
Prompt `$  ssh cs15lsp22zz@ieng6.ucsd.edu` in the command like and press enter. 

> The "zz" in this example should be replaced by your course specific letters given by your course account

> If this is your first time connecting to a server, an authenticity message may pop up in your terminal. Type `yes` and hit enter. Then type in your password to log in.

Your terminal should look similar to this:

![Image](ssh.png)

---
## Using Basic Commands 

The next step is to test out some basic commands in the terminal. 

**Here are some commands to try in the terminal and what they do:**

* `cd` : change directory; this command will allow you to change between the working directories
* `ls` and  `-lat` : `ls` and `ls -lat` (local area transport) lists the computer files in UNIX and shows the decending order of the files of when the last file was opened (respectively)
* `/home/linux/ieng6/cs15lsp22/cs15lsp22abc` (where `abc` is a username different from your own): shows that you are only able to open your account and not able to access other group members' username

> Here are some examples of the `cd` and `ls -lat` outputs 

![image](cdTest.png)

---

## Moving Files with `scp`

The `scp` command allows you to copy a single or multiple files from your device (the *client*) to a remote computer. 

* To try out this command, make a new java file or take an old, basic java file and run it using `javac` and `java`

* From the same terminal, insert and run the command `scp InsertNameOfFileHere.java cs15lsp22zz@ieng6.ucsd.edu:~/` where "zz" is the letters of your course related login information.

> Note: you will be asked to type in your password

* Once you are logged into `ssh`, use the command `ls` and you should now be able to see the name of your chosen file show in your directory.

Your terminal should look siumilar to this (here I am using a file called `WhereAmI.java` that tells some simple information about my device and location):

![Image](scp.png)

**Congrats! You are now able to run your code on the *ieng6 computer*!**

---

## Setting an SSH Key

By default, when you log into a remote server to run copy and run commands, you must log in by filling out your password each time, which can add up. Creating an `ssh` key will allow us to log in faster by letting us bypass the password entry.

`ssh key` is short for `ssh-keygen`, and **creates a public and private key file**.

> The public and private key will be replaced by the `ssh` command that will take that key in place of your password.

Here is an example of what the setup should look like and what the prompted message should look like:

![Image](keygen.png)

> This essentially creates the private and public key in files called `id_rsa` and `id_rsa.pub` respectively and stores them in the `.ssh` direcrtory.

* In order to copy the public key to the `.ssh` directory of your specific account on the server to bypass the password prompt:

1. log out of the server (if already logged in) using  `mkdir .ssh`.  This will take you back to the client
2. Insert `$ scp/Users/user-name/.ssh/id_rsa.pub cs15lsp22zz@ieng6.ucsd.edu:~/.ssh/authorized_keys` (where username is **your** username and zz corresponds with the letters of your accound) in the command line and run.

You should now be able to run the `ssh` and `scp` commands without having to enter you password!!!

**Congrats! You have now saved yourself some time from connecting!**

---

## Optimize your Remote Running 

You're almost done! Here are some ways that you can make local edits to your file for pleasant:

* Use the up arrow on your keyboard to recall the last commands that were called so you don't have to retype long command lines!
* You can use ";" to separate different commands in the same command line to run multiple commands in one line 
> EX: `$ cp hello.java info.java; javac info.java; java hello` 

The screenshot below is an example of compiling on separate command lines versus on the same line (which is more time efficient!) (the example above!)

![Image](part7.png)

---
**Congrats! You have completed the tutorial! Thank you for following along!**