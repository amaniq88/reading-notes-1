# Ryans Tutorials

># Remeber This :-
>> ## Unix likes to take the approach of giving you a set of building blocks and then letting you put them together. This allows us to build things to suit our needs.

---

>>>### This Linux tutorial is divided into 13 sections:-

    A. The Command Line; A command line, or terminal, is a text based interface to the system , it`s Not a GUI !!.

    B. Basic Navigation; An introduction to the Linux directory system and how to get around it.

    C. About Files; Everything is File/ Directory.

    D. Manual pages; the name explains it self.

    E. Files manipulation; Moving and Removing files.

---

# A. The Command Line :-

>     The command line are your  window into the computer :-
>     for example ; within the terminal you have shells; and shells they are like a part of operating system ; and they define how your terminal will Work !!. And there are various shell commands, one of the most common is called Bash ...(stands for Bourne again shell).

>    you can use `echo $SHELL` ; to know which shell you are using for example with the python environment we are currently using this ZSH Shell !.

---

>## Hints :-

Linux is full of shortcuts to help make your life easier, Here are some of them:

1. You can  this history using the up and down arrow keys.

2. You can also edit these commands using the left and right arrow keys to move the cursor where you want.

3. Dont Forget ALL commands are **CaSe SeNsItIvE !!** .

---

# B. Basic Navigation :-

1. pwd : Print Working Directory ,Where are we currently.

2. ls : List the contents of a directory , you can use ls -a : to show all the contents( including hidden files).

3. ls [options] [location] : In the above example, the square brackets ( [ ] ) mean that those items are optional, we may run the command with or without them.

4. ls -l : which indicates we are going to do a long listing. A long listing First character indicates whether it is a normal file ( - ) or directory ( d )

5. ls /etc : it tells ls not to list our current directory but instead to list that directories contents

6. ls -l /etc : it did a long listing of the directory /etc

7. -> `...` : got back out of all

8. `cd` : Change Directories ( to move to another directory (file) )

9. `~` : its called Telda and it mean home(root).

10. `.` : current directory .

11. `..` : parent directory .

## Paths:-

`Relative path`
> A file or directory location relative to where we currently are in the file system.

`Absolute path`
> A file or directory location in relation to the root of the file system.

## Hints :-

    1. If you run the command `cd` without any arguments then it will always take you back to your home directory.

    2.hit the `Tab` key on your keyboard at any time which will auto- `complete sentences`.

---

# C. More About Files

> ## **Everything is a File! Even directories!**

A text file is a file, a directory is a file, your keyboard is a file (one that the system reads from only), your monitor is a file (one that the system writes to only) etc.
>Linux is an Extensionless System !!
>>The following are common extensions:
file.exe - an executable file, or program.
file.txt - a plain text file.
file.png, file.gif, file.jpg - an image.

---
> Spaces in names !!
>>Spaces in file and directory names are perfectly valid but we need to be a little careful with them Beware of silly typos.
---
>Quotes:-
    1. Anything inside quotes is considered a single item.
----> cd 'Holiday Photos'

    2. Another method is to use what is called an escape character, which is a backslash ( \ ). What the backslash does is escape (or nullify) the special meaning of the next character.

> ### **Hidden Files and Directories**

>> #### Remeber ls -a Hint!

    Linux actually has a very simple and elegant mechanism for specifying that a file or directory is hidden. If the file or directory's name begins with a . `(full stop)` then it is considered to be hidden. You don't even need a special command or action to make a file hidden. Files and directories may be hidden for a variety of reasons. 

    Configuration files for a particular user (which are normally stored in their home directory) are hidden for instance so that they don't get in the way of the user doing their everyday tasks.

---

# D. Manual Pages

## Manual Pages

The manual pages(Man) are a set of pages that explain every command available on your system including what they do. `man ls` :list directory contents

1. `man ls Look up` the manual page for a particular command. 
2. `man -k` Do a keyword search for all manual pages containing the given search term.
3. `/<term>`  Within a manual page, perform a search for `term`
4. `n` After performing a search within a manual page, select the next found item.

>"To exit the man pages press 'q' for quit."

>The man pages are your friend.
Instead of trying to remember everything, instead remember you can easily look stuff up in the man pages.


---

# E. File Manipulation

1. `mkdir`  Make Directory - ie. Create a directory.
2. `rmdir` Remove Directory - ie. Delete a directory.
3. `touch` Create a blank file.
4. `cp` Copy - ie. Copy a file or directory.
5. `mv` Move - ie. Move a file or directory (can also be used to rename).
6. `rm` Remove - ie. Delete a file.
7. `mkdir -p` which tells mkdir to make parent directories as needed
8. `mkdir -pv`  which makes mkdir tell us what it is doing
9. `cp -r` which stands for recursive, we may copy directories. Recursive means that we want to look at a directory and all files and directories within it, and for subdirectories, go into them and do the same thing and keep doing this.


>### Removing a Directory
>> Few things to note.
>>> 1. rmdir supports the -v and -p options similar to mkdir.
>>> 2. A directory must be empty before it may be removed.
>>> 3. No undo
The Linux command line does not have an undo feature. Perform destructive actions carefully.
>>> 4. Command line options
Most commands have many useful command line options. Make sure you skim the man page for new commands so you are familiar with what they can do and what is available.

---

># Cheat Sheet **Ryan tutorials**
>># LINK TO THE [CHEAT SHEET](https://ryanstutorials.net/linuxtutorial/cheatsheet.php) PAGE IF YOU WANT TO CHECK IT.
