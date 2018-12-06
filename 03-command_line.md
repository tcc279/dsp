# Learn command line

Please follow and complete the free online [Bash Scripting Tutorial](https://ryanstutorials.net/bash-scripting-tutorial/) or [Codecademy's Learn the Command Line](https://www.codecademy.com/learn/learn-the-command-line). These are helpful tutorials. You should be able to go through these in a couple of hours.

**Note:** Bash is not installed on a PC. Rather, PC users must install Cygwin. Once Cygwin has been installed, the command line interface witll _emulate_ bash. You can find all information regarding Cygwin [here](https://www.cygwin.com/).

---

### Q1.  Cheat Sheet of Commands  

Here's a list of items with which you should be familiar:  
* show current working directory path
* creating a directory
* deleting a directory
* creating a file using `touch` command
* deleting a file
* renaming a file
* listing hidden files
* copying a file from one directory to another

Make a cheat sheet for yourself: a list of at least **ten** commands and what they do.  (Use the 8 items above and add a couple of your own.)  

> > 
1. pwd -> print working directory path
2. mkdir -> creates directory
3. rm -r -> deletes a directory
4. touch -> creates a file or multiple files
5. rm -> deletes file
6. mv x y -> renames file x to y
7. ls -a -> list all files including hidden files
8. cp x y -> copies file x to directory y
9. cd -> change directory
10. ls -> lists files in current directory
11. mv -> moves file
12. rmdir -> deletes empty directory
13. cat -> shows text inside a .txt file

---

### Q2.  List Files in Unix   

What do the following commands do:  
`ls`  
`ls -a`  
`ls -l`  
`ls -lh`  
`ls -lah`  
`ls -t`  
`ls -Glp`  

> > 
ls -> list files in working directory 
ls -a -> list all files including hidden firls starting with '.'  
ls -l -> shows file or directory, size, modified date and time, file or folder name and owner of file and its permission   
ls -lh -> does the same as -l but shows sizes in human readable format  
ls -lah-> same as above but also includes hidden files  
ls -t -> lists files by time/date 
ls -Glp -> lists long format directories with "/" appended to the end and without user group names


---

### Q3.  More List Files in Unix  

Explore these other [ls options](http://www.techonthenet.com/unix/basic/ls.php) and pick 5 of your favorites:

> > 
1. ls -l -> displays long format lisitng
2. ls -t -> displays newest files first
3. ls -u -> displays file access time
4. ls -d -> displays directories only
5. ls -c -> displays files by file timestamp

---

### Q4.  Xargs   

What does `xargs` do? Give an example of how to use it.
> > The command xargs create an execution pipeline frm a standard input and allows tools like echo and rm to accept standard input as arguments. For example, the code 'echo one two three | xargs mkdir' will create three folders named one, two, and three

 

