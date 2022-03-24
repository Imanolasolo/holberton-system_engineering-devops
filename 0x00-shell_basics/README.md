# 0x00. Shell, basics
## Details
      By Julien Barbier          Weight: 1              Project over - took place from 09-22-2021 to 09-23-2021          - you're done with 200% of tasks.              An auto review will be launched at the deadline      #### In a nutshell…
* Auto QA review:          75.0/75 mandatory            &            0.0/25 optional      
* Altogether:         100.0%* Mandatory: 100.0%
* Optional: 0.0%
*               Calculation:                   100.0%                    + (100.0% * 0.0%)               == 100.0%

## About Bash projects

Unless stated, all your projects will be auto-corrected with Ubuntu 20.04 LTS.

 ![](https://s3.amazonaws.com/intranet-projects-files/holbertonschool-sysadmin_devops/205/image.jpg) 

## Resources
Read or watch :
* [What Is “The Shell”?](https://intranet.hbtn.io/rltoken/pn2_LGNuA1yFY7zy3CQmig) 

* [Navigation](https://intranet.hbtn.io/rltoken/Hh8elGgCpj--6othR7S7GQ) 

* [Looking Around](https://intranet.hbtn.io/rltoken/84xsZOempqy5I7ZkueeIsg) 

* [A Guided Tour](https://intranet.hbtn.io/rltoken/Jp1c4V3hJiGBuVzYCtnQKw) 

* [Manipulating Files](https://intranet.hbtn.io/rltoken/wFwFXKQmSpmxYyvHvCIC-Q) 

* [Working With Commands](https://intranet.hbtn.io/rltoken/Aq3NVLBhgnQS6NYtHI8i4w) 

* [Reading Man pages](https://intranet.hbtn.io/rltoken/RohkjGiQtMHgPfj0N_k1Bw) 

* [Keyboard shortcuts for Bash](https://intranet.hbtn.io/rltoken/0HvJ2B_wSl6Oyshcn-OHrg) 

* [LTS](https://wiki.ubuntu.com/LTS) 

* [Shebang](https://intranet.hbtn.io/rltoken/ketzZf-802Fb-mSGkyPa4w) 

man or help :
*  ` cd ` 
*  ` ls ` 
*  ` pwd ` 
*  ` less ` 
*  ` file ` 
*  ` ln ` 
*  ` cp ` 
*  ` mv ` 
*  ` rm ` 
*  ` mkdir ` 
*  ` type ` 
*  ` which ` 
*  ` help ` 
*  ` man ` 
## Learning Objectives
At the end of this project, you are expected to be able to  [explain to anyone](https://intranet.hbtn.io/rltoken/uzS14i1TrIOzP984RDR4-Q) 
 ,  without the help of Google :
### General
* What does RTFM mean?
* What is a Shebang
### What is the Shell
* What is the shell
* What is the difference between a terminal and a shell
* What is the shell prompt
* How to use the history (the basics)
### Navigation
* What do the commands or built-ins  ` cd ` ,  ` pwd ` ,  ` ls `  do 
* How to navigate the filesystem
* What are the . and .. directories
* What is the working directory, how to print it and how to change it
* What is the root directory
* What is the home directory, and how to go there
* What is the difference between the root directory and the home directory of the user root
* What are the characteristics of hidden files and how to list them
* What does the command  ` cd - `  do
### Looking Around
* What do the commands  ` ls ` ,  ` less ` ,  ` file `  do
* How do you use options and arguments with commands
* Understand the ls long format and how to display it
* [A Guided Tour](https://intranet.hbtn.io/rltoken/Jp1c4V3hJiGBuVzYCtnQKw) 

* What does the  ` ln `  command do
* What do you find in the most common/important directories
* What is a symbolic link
* What is a hard link
* What is the difference between a hard link and a symbolic link
### Manipulating Files
* What do the commands  ` cp ` ,  ` mv ` ,  ` rm ` ,  ` mkdir `  do
* What are wildcards and how do they work
* How to use wildcards
### Working with Commands
* What do  ` type ` ,  ` which ` ,  ` help ` ,  ` man `  commands do
* What are the different kinds of commands
* What is an alias
* When do you use the command help instead of man
### Reading Man Pages
* How to read a man page
* What are man page sections
* What are the section numbers for User commands, System calls and Library functions
### Keyboard Shortcuts for Bash
* Common shortcuts for Bash
### LTS
* What does  ` LTS `  mean?
## Requirements
### General
* Allowed editors:  ` vi ` ,  ` vim ` ,  ` emacs ` 
* All your scripts will be tested on Ubuntu 20.04 LTS
* All your scripts should be exactly two lines long ( ` $ wc -l file `  should print 2)
* All your files should end with a new line ([why?](http://unix.stackexchange.com/questions/18743/whats-the-point-in-adding-a-new-line-to-the-end-of-a-file/18789) 
)
* The first line of all your files should be exactly  ` #!/bin/bash ` 
* A  ` README.md `  file at the root of the repo, containing a description of the repository
* A  ` README.md `  file, at the root of the folder of this project, describing what each script is doing
* You are not allowed to use backticks,  ` && ` ,  ` || `  or  ` ; ` 
* All your scripts must be executable. To make your file executable, use the  ` chmod `  command:   ` chmod u+x file ` . Later, we’ll learn more about how to utilize this command.
## More Info
Example of line count and first line
```bash
julien@ubuntu:/tmp$ wc -l 12-file_type 
2 12-file_type
julien@ubuntu:/tmp$ head -n 1 12-file_type 
#!/bin/bash
julien@ubuntu:/tmp$ 

```
In order to test your scripts, you will need to use this command:   ` chmod u+x file `  . We will see later what does   ` chmod `   mean and do, but you can have a look at   ` man chmod `   if you are curious.
Example
```bash
julien@ubuntu:/tmp$ ls
12-file_type
lll
julien@ubuntu:/tmp$ ls -la lll
-rw-rw-r-- 1 julien julien 15 Sep 19 21:05 lll
julien@ubuntu:/tmp$ cat lll
#!/bin/bash
ls
julien@ubuntu:/tmp$ ls -l lll
-rw-rw-r-- 1 julien julien 15 Sep 19 21:05 lll
julien@ubuntu:/tmp$ chmod u+x lll # you do not have to understand this yet
julien@ubuntu:/tmp$ ls -l lll
-rwxrw-r-- 1 julien julien 15 Sep 19 21:05 lll
julien@ubuntu:/tmp$ ./lll
12-file_type
lll
julien@ubuntu:/tmp$ 

```
## Quiz questions
Great!          You've completed the quiz successfully! Keep going!          (Show quiz)#### 
        
        Question #0
    
 Quiz question Body What command would you use to list files on Linux?
 Quiz question Answers * pwd

* cd

* ls

* list

* which

 Quiz question Tips #### 
        
        Question #1
    
 Quiz question Body What does LTS stand for?
 Quiz question Answers * Long Term Support

* Long Time Support

* Last Terrible Service

 Quiz question Tips #### 
        
        Question #2
    
 Quiz question Body How do you change directory on Linux?
 Quiz question Answers * pwd

* cd

* ls

* which

 Quiz question Tips #### 
        
        Question #3
    
 Quiz question Body What does RTFM stand for?
 Quiz question Answers * Remember The First Manipulation

* Read, Teach, Forget, Migrate

* Read The F** Manual

 Quiz question Tips ## Tasks
### 0. Where am I?
          mandatory         Progress vs Score           Score: 100.00% (Checks completed: 100.00%)         Task Body Write a script that prints the absolute path name of the current working directory.
Example:
 ` $ ./0-current_working_directory
/0x00-shell_basics
$
 `  Task URLs  Github information Repo:
* GitHub repository:  ` holberton-system_engineering-devops ` 
* Directory:  ` 0x00-shell_basics ` 
* File:  ` 0-current_working_directory ` 
 Self-paced manual review  Panel footer - Controls 
### 1. What’s in there?
          mandatory         Progress vs Score           Score: 100.00% (Checks completed: 100.00%)         Task Body Display the contents list of your current directory.
Example:
```bash
$ ./1-listit
Applications    Documents   Dropbox Movies Pictures
Desktop Downloads   Library Music Public
$

```
 Task URLs  Github information Repo:
* GitHub repository:  ` holberton-system_engineering-devops ` 
* Directory:  ` 0x00-shell_basics ` 
* File:  ` 1-listit ` 
 Self-paced manual review  Panel footer - Controls 
### 2. There is no place like home
          mandatory         Progress vs Score           Score: 100.00% (Checks completed: 100.00%)         Task Body Write a script that changes the working directory to the user’s home directory.
* You are not allowed to use any shell variables
```bash
julien@ubuntu:/tmp$ pwd
/tmp
julien@ubuntu:/tmp$ echo $HOME
/home/julien
julien@ubuntu:/tmp$ source ./2-bring_me_home
julien@ubuntu:~$ pwd
/home/julien
julien@ubuntu:~$ 

```
 Task URLs  Github information Repo:
* GitHub repository:  ` holberton-system_engineering-devops ` 
* Directory:  ` 0x00-shell_basics ` 
* File:  ` 2-bring_me_home ` 
 Self-paced manual review  Panel footer - Controls 
### 3. The long format
          mandatory         Progress vs Score           Score: 100.00% (Checks completed: 100.00%)         Task Body Display current directory contents in a long format
Example:
```bash
$ ./3-listfiles
total 32
-rwxr-xr-x@ 1 sylvain staff 18 Jan 25 00:19 0-current_working_directory
-rwxr-xr-x@ 1 sylvain staff 19 Jan 25 00:23 1-listit
-rwxr-xr-x@ 1 sylvain staff 18 Jan 25 00:29 2-bring_me_home
-rwxr-xr-x@ 1 sylvain staff 18 Jan 25 00:39 3-listfiles
$

```
 Task URLs  Github information Repo:
* GitHub repository:  ` holberton-system_engineering-devops ` 
* Directory:  ` 0x00-shell_basics ` 
* File:  ` 3-listfiles ` 
 Self-paced manual review  Panel footer - Controls 
### 4. Hidden files
          mandatory         Progress vs Score           Score: 100.00% (Checks completed: 100.00%)         Task Body Display current directory contents, including hidden files (starting with   ` . `  ). Use the long format.
Example:
```bash
$ ./4-listmorefiles
total 32
drwxr-xr-x@ 6 sylvain staff 204 Jan 25 00:29 .
drwxr-xr-x@ 43 sylvain staff 1462 Jan 25 00:19 ..
-rwxr-xr-x@ 1 sylvain staff 18 Jan 25 00:19 0-current_working_directory
-rwxr-xr-x@ 1 sylvain staff 19 Jan 25 00:23 1-listit
-rwxr-xr-x@ 1 sylvain staff 18 Jan 25 00:29 2-bring_me_home
-rwxr-xr-x@ 1 sylvain staff 18 Jan 25 00:39 3-listfiles
-rwxr-xr-x@ 1 sylvain staff 18 Jan 25 00:41 4-listmorefiles
$

```
 Task URLs  Github information Repo:
* GitHub repository:  ` holberton-system_engineering-devops ` 
* Directory:  ` 0x00-shell_basics ` 
* File:  ` 4-listmorefiles ` 
 Self-paced manual review  Panel footer - Controls 
### 5. I love numbers
          mandatory         Progress vs Score           Score: 100.00% (Checks completed: 100.00%)         Task Body Display current directory contents.
* Long format
* with user and group IDs displayed numerically
* And hidden files (starting with .)
Example:
```bash
$ ./5-listfilesdigitonly
total 32
drwxr-xr-x@ 6 501 20 204 Jan 25 00:29 .
drwxr-xr-x@ 43 501 20 1462 Jan 25 00:19 ..
-rwxr-xr-x@ 1 501 20 18 Jan 25 00:19 0-current_working_directory
-rwxr-xr-x@ 1 501 20 18 Jan 25 00:23 1-listfiles
-rwxr-xr-x@ 1 501 20 19 Jan 25 00:29 2-bring_me_home
-rwxr-xr-x@ 1 501 20 20 Jan 25 00:39 3-listfiles
-rwxr-xr-x@ 1 501 20 18 Jan 25 00:41 4-listmorefiles
-rwxr-xr-x@ 1 501 20 18 Jan 25 00:43 5-listfilesdigitonly
$

```
 Task URLs  Github information Repo:
* GitHub repository:  ` holberton-system_engineering-devops ` 
* Directory:  ` 0x00-shell_basics ` 
* File:  ` 5-listfilesdigitonly ` 
 Self-paced manual review  Panel footer - Controls 
### 6. Welcome
          mandatory         Progress vs Score           Score: 100.00% (Checks completed: 100.00%)         Task Body Create a script that creates a directory named   ` my_first_directory `   in the   ` /tmp/ `   directory.
Example:
 ` $ ./6-firstdirectory
$ file /tmp/my_first_directory/
/tmp/my_first_directory/: directory
$
 `  Task URLs  Github information Repo:
* GitHub repository:  ` holberton-system_engineering-devops ` 
* Directory:  ` 0x00-shell_basics ` 
* File:  ` 6-firstdirectory ` 
 Self-paced manual review  Panel footer - Controls 
### 7. Betty in my first directory
          mandatory         Progress vs Score           Score: 100.00% (Checks completed: 100.00%)         Task Body Move the file   ` betty `   from   ` /tmp/ `   to   ` /tmp/my_first_directory `  .
Example:
 ` $ ./7-movethatfile
$ ls /tmp/my_first_directory/
betty
$
 `  Task URLs  Github information Repo:
* GitHub repository:  ` holberton-system_engineering-devops ` 
* Directory:  ` 0x00-shell_basics ` 
* File:  ` 7-movethatfile ` 
 Self-paced manual review  Panel footer - Controls 
### 8. Bye bye Betty
          mandatory         Progress vs Score           Score: 100.00% (Checks completed: 100.00%)         Task Body Delete the file   ` betty `  .
* The file  ` betty `  is in  ` /tmp/my_first_directory ` 
Example:
 ` $ ./8-firstdelete
$ ls /tmp/my_first_directory/
$
 `  Task URLs  Github information Repo:
* GitHub repository:  ` holberton-system_engineering-devops ` 
* Directory:  ` 0x00-shell_basics ` 
* File:  ` 8-firstdelete ` 
 Self-paced manual review  Panel footer - Controls 
### 9. Bye bye My first directory
          mandatory         Progress vs Score           Score: 100.00% (Checks completed: 100.00%)         Task Body Delete the directory   ` my_first_directory `   that is in the   ` /tmp `   directory.
Example:
```bash
$ ./9-firstdirdeletion
$ file /tmp/my_first_directory
/tmp/my_first_directory: cannot open `/tmp/my_first_directory' (No such file or directory)
$

```
 Task URLs  Github information Repo:
* GitHub repository:  ` holberton-system_engineering-devops ` 
* Directory:  ` 0x00-shell_basics ` 
* File:  ` 9-firstdirdeletion ` 
 Self-paced manual review  Panel footer - Controls 
### 10. Back to the future
          mandatory         Progress vs Score           Score: 100.00% (Checks completed: 100.00%)         Task Body Write a script that changes the working directory to the previous one.
```bash
julien@ubuntu:/tmp$ pwd
/tmp
julien@ubuntu:/tmp$ cd /var
julien@ubuntu:/var$ pwd
/var
julien@ubuntu:/var$ source ./10-back
/tmp
julien@ubuntu:/tmp$ pwd
/tmp

```
 Task URLs  Github information Repo:
* GitHub repository:  ` holberton-system_engineering-devops ` 
* Directory:  ` 0x00-shell_basics ` 
* File:  ` 10-back ` 
 Self-paced manual review  Panel footer - Controls 
### 11. Lists
          mandatory         Progress vs Score           Score: 100.00% (Checks completed: 100.00%)         Task Body Write a script that lists all files (even ones with names beginning with a period character, which are normally hidden) in the current directory and the parent of the working directory and the   ` /boot `   directory (in this order), in long format.
 Task URLs  Github information Repo:
* GitHub repository:  ` holberton-system_engineering-devops ` 
* Directory:  ` 0x00-shell_basics ` 
* File:  ` 11-lists ` 
 Self-paced manual review  Panel footer - Controls 
### 12. File type
          mandatory         Progress vs Score           Score: 100.00% (Checks completed: 100.00%)         Task Body Write a script that prints the type of the file named   ` iamafile `  . The file   ` iamafile `   will be in the   ` /tmp `   directory when we will run your script.
Example
```bash
ubuntu@ip-172-31-63-244:~$ ./12-file_type
/tmp/iamafile: ELF 64-bit LSB  executable, x86-64, version 1 (SYSV), dynamically linked (uses shared libs), for GNU/Linux 2.6.24, BuildID[sha1]=bd39c07194a778ccc066fc963ca152bdfaa3f971, stripped

```
Note that depending on the file, the output of your script will be different.
 Task URLs  Github information Repo:
* GitHub repository:  ` holberton-system_engineering-devops ` 
* Directory:  ` 0x00-shell_basics ` 
* File:  ` 12-file_type ` 
 Self-paced manual review  Panel footer - Controls 
### 13. We are symbols, and inhabit symbols
          mandatory         Progress vs Score           Score: 100.00% (Checks completed: 100.00%)         Task Body Create a symbolic link to   ` /bin/ls `  , named   ` __ls__ `  .The symbolic link should be created in the current working directory. 
```bash
ubuntu@ip-172-31-63-244:/tmp/sym$ ls -la
total 144
drwxrwxr-x  2 ubuntu ubuntu   4096 Sep 20 03:24 .
drwxrwxrwt 12 root   root   139264 Sep 20 03:24 ..
ubuntu@ip-172-31-63-244:/tmp/sym$./13-symbolic_link
ubuntu@ip-172-31-63-244:/tmp/sym$ ls -la
total 144
drwxrwxr-x  2 ubuntu ubuntu   4096 Sep 20 03:24 .
drwxrwxrwt 12 root   root   139264 Sep 20 03:24 ..
lrwxrwxrwx  1 ubuntu ubuntu      7 Sep 20 03:24 __ls__ -> /bin/ls

```
 Task URLs  Github information Repo:
* GitHub repository:  ` holberton-system_engineering-devops ` 
* Directory:  ` 0x00-shell_basics ` 
* File:  ` 13-symbolic_link ` 
 Self-paced manual review  Panel footer - Controls 
### 14. Copy HTML files
          mandatory         Progress vs Score           Score: 100.00% (Checks completed: 100.00%)         Task Body Create a script that copies all the HTML files from the current working directory to the parent of the working directory, but only copy files that did not exist in the parent of the working directory or were newer than the versions in the parent of the working directory.
You can consider that all HTML files have the extension   ` .html ` 
 Task URLs  Github information Repo:
* GitHub repository:  ` holberton-system_engineering-devops ` 
* Directory:  ` 0x00-shell_basics ` 
* File:  ` 14-copy_html ` 
 Self-paced manual review  Panel footer - Controls 
### 15. Let’s move
          #advanced         Progress vs Score           Score: 0.00% (Checks completed: 0.00%)         Task Body Create a script that moves all files beginning with an uppercase letter to the directory   ` /tmp/u `  .
You can assume that the directory   ` /tmp/u `   will exist when we will run your script
```bash
ubuntu@ip-172-31-63-244:/tmp/sym$ ls -la
total 148
drwxrwxr-x  3 ubuntu ubuntu   4096 Sep 20 03:33 .
drwxrwxrwt 12 root   root   139264 Sep 20 03:26 ..
-rw-rw-r--  1 ubuntu ubuntu      0 Sep 20 03:32 My_file
lrwxrwxrwx  1 ubuntu ubuntu      7 Sep 20 03:24 __ls__ -> /bin/ls
-rw-rw-r--  1 ubuntu ubuntu      0 Sep 20 03:32 Elif_ym
-rw-rw-r--  1 ubuntu ubuntu      0 Sep 20 03:32 random_file
ubuntu@ip-172-31-63-244:/tmp/sym$ ls -la /tmp/u
total 8
drwxrwxr-x 2 ubuntu ubuntu 4096 Sep 20 03:33 .
drwxrwxr-x 3 ubuntu ubuntu 4096 Sep 20 03:33 ..
ubuntu@ip-172-31-63-244:/tmp/sym$ ./100-lets_move
ubuntu@ip-172-31-63-244:/tmp/sym$ ls -la
total 148
drwxrwxr-x  3 ubuntu ubuntu   4096 Sep 20 03:33 .
drwxrwxrwt 12 root   root   139264 Sep 20 03:26 ..
lrwxrwxrwx  1 ubuntu ubuntu      7 Sep 20 03:24 __ls__ -> /bin/ls
-rw-rw-r--  1 ubuntu ubuntu      0 Sep 20 03:32 random_file
ubuntu@ip-172-31-63-244:/tmp/sym$ ls -la /tmp/u
total 8
drwxrwxr-x 2 ubuntu ubuntu 4096 Sep 20 03:33 .
drwxrwxr-x 3 ubuntu ubuntu 4096 Sep 20 03:33 ..
-rw-rw-r-- 1 ubuntu ubuntu    0 Sep 20 03:32 My_file
-rw-rw-r-- 1 ubuntu ubuntu    0 Sep 20 03:32 Elif_ym

```
 Task URLs  Github information Repo:
* GitHub repository:  ` holberton-system_engineering-devops ` 
* Directory:  ` 0x00-shell_basics ` 
* File:  ` 100-lets_move ` 
 Self-paced manual review  Panel footer - Controls 
### 16. Clean Emacs
          #advanced         Progress vs Score           Score: 0.00% (Checks completed: 0.00%)         Task Body Create a script that deletes all files in the current working directory that end with the character   ` ~ `  .
```bash
ubuntu@ip-172-31-63-244:/tmp/sym$ ls
main.c  main.c~  Makefile~
ubuntu@ip-172-31-63-244:/tmp/sym$ ./101-clean_emacs
ubuntu@ip-172-31-63-244:/tmp/emacs$ ls
main.c
ubuntu@ip-172-31-63-244:/tmp/emacs$

```
 Task URLs  Github information Repo:
* GitHub repository:  ` holberton-system_engineering-devops ` 
* Directory:  ` 0x00-shell_basics ` 
* File:  ` 101-clean_emacs ` 
 Self-paced manual review  Panel footer - Controls 
### 17. Tree
          #advanced         Progress vs Score           Score: 0.00% (Checks completed: 0.00%)         Task Body Create a script that creates the directories   ` welcome/ `  ,   ` welcome/to/ `   and   ` welcome/to/school `   in the current directory.
You are only allowed to use two spaces (and lines) in your script, not more.
```bash
julien@ubuntu:/tmp/h$ ls -l
total 4
-rwxrw-r-- 1 julien julien 44 Sep 20 12:09 102-tree
julien@ubuntu:/tmp/h$ wc -l 102-tree 
2 102-tree
julien@ubuntu:/tmp/h$ head -1 102-tree 
#!/bin/bash
julien@ubuntu:/tmp/h$ tr -cd ' ' < 102-tree | wc -c # you do not have to understand this yet, but the result should be 2, 1 or 0
2
julien@ubuntu:/tmp/h$ ./102-tree 
julien@ubuntu:/tmp/h$ ls
102-tree  welcome
julien@ubuntu:/tmp/h$ ls welcome/
to
julien@ubuntu:/tmp/h$ ls -l welcome/to
total 4
drwxrwxr-x 2 julien julien 4096 Sep 20 12:11 school
julien@ubuntu:/tmp/h$ 

```
 Task URLs  Github information Repo:
* GitHub repository:  ` holberton-system_engineering-devops ` 
* Directory:  ` 0x00-shell_basics ` 
* File:  ` 102-tree ` 
 Self-paced manual review  Panel footer - Controls 
### 18. Life is a series of commas, not periods
          #advanced         Progress vs Score           Score: 0.00% (Checks completed: 0.00%)         Task Body Write a command that lists all the files and directories of the current directory, separated by commas (  ` , `  ).
* Directory names should end with a slash ( ` / ` )
* Files and directories starting with a dot ( ` . ` ) should be listed
* The listing should be alpha ordered, except for the directories  ` . `  and  ` .. `  which should be listed at the very beginning
* Only digits and letters are used to sort; Digits should come first
* You can assume that all the files we will test with will have at least one letter or one digit
* The listing should end with a new line
```bash
ubuntu@ubuntu:~/$ ls -a

.  ..  0-commas  0-commas-checks  1-empty_casks  2-gifs  3-directories  4-zeros  5-rot13  6-odd  7-sort_rot13  Makefile  quote  .test  test_dir  test.var

ubuntu@ubuntu:~/$ ./103-commas

./, ../, 0-commas, 0-commas-checks/, 1-empty_casks, 2-gifs, 3-directories, 4-zeros, 5-rot13, 6-odd, 7-sort_rot13, Makefile, quote, .test, test_dir/, test.var

ubuntu@ubuntu:~/$

```
 Task URLs  Github information Repo:
* GitHub repository:  ` holberton-system_engineering-devops ` 
* Directory:  ` 0x00-shell_basics ` 
* File:  ` 103-commas ` 
 Self-paced manual review  Panel footer - Controls 
### 19. File type: School
          #advanced         Progress vs Score           Score: 0.00% (Checks completed: 0.00%)         Task Body Create a magic file   ` school.mgc `   that can be used with the command   ` file `   to detect   ` School `   data files.   ` School `   data files always contain the string   ` SCHOOL `   at offset 0.
```bash
ubuntu@ip-172-31-63-244:/tmp/magic$ cp /bin/ls .
ubuntu@ip-172-31-63-244:/tmp/magic$ ls -la
total 268
drwxrwxr-x  2 ubuntu ubuntu   4096 Sep 20 02:44 .
drwxrwxrwt 11 root   root   139264 Sep 20 02:44 ..
-rw-r--r--  1 ubuntu ubuntu    496 Sep 20 02:42 school.mgc
-rwxr-xr-x  1 ubuntu ubuntu 110080 Sep 20 02:43 ls
-rw-rw-r--  1 ubuntu ubuntu     50 Sep 20 02:06 thisisaschoolfile
-rw-rw-r--  1 ubuntu ubuntu     30 Sep 20 02:16 thisisatextfile
ubuntu@ip-172-31-63-244:/tmp/magic$ file --mime-type -m school.mgc *
school.mgc:         application/octet-stream
ls:                    application/octet-stream
thisisaschoolfile: School
thisisatextfile:       text/plain
ubuntu@ip-172-31-63-244:/tmp/magic$ file -m school.mgc *
school.mgc:         data
ls:                    data
thisisaschoolfile: School data
thisisatextfile:       ASCII text
ubuntu@ip-172-31-63-244:/tmp/magic$

```
 Task URLs  Github information Repo:
* GitHub repository:  ` holberton-system_engineering-devops ` 
* Directory:  ` 0x00-shell_basics ` 
* File:  ` school.mgc ` 
 Self-paced manual review  Panel footer - Controls 
×#### Recommended Sandbox
[Running only]() 
### 1 image(1/5 Sandboxes spawned)
### Ubuntu 20.04
Basic Ubuntu 20.04, with vim, emacs, curl, wget and all needed for Holberton Foundations
SSHSFTP[Webterm](https://intranet.hbtn.io/user_containers/21027/webterm) 
[Destroy]() 
#### Credentials
Host7e37754e8586.1e732e4d.hbtn-cod.ioUsername7e37754e8586Passworde4af702ba40df68e3592#### Web access
[HTTPS](https://7e37754e8586.1e732e4d.hbtn-cod.io/) 
[HTTP](http://7e37754e8586.1e732e4d.hbtn-cod.io/) 
[3000](http://7e37754e8586.1e732e4d.hbtn-cod.io:3000/) 
[4000](http://7e37754e8586.1e732e4d.hbtn-cod.io:4000/) 
[5000](http://7e37754e8586.1e732e4d.hbtn-cod.io:5000/) 
[5001](http://7e37754e8586.1e732e4d.hbtn-cod.io:5001/) 
[8000](http://7e37754e8586.1e732e4d.hbtn-cod.io:8000/) 
[8080](http://7e37754e8586.1e732e4d.hbtn-cod.io:8080/) 
#### Port mapping
SSH49533HTTP49532HTTPS49531300049530MySQL49529400049528500049527500149526800049525808049524