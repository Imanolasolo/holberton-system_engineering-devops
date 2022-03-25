# 0x03. Shell, init files, variables and expansions

![Logo](https://www.howtogeek.com/wp-content/uploads/2021/05/laptop-with-terminal-big.png?height=200p&trim=2,2,2,50)

## About Bash projects

Unless stated, all your projects will be auto-corrected with Ubuntu 20.04 LTS.

## Resources

Read or watch :

* [Expansions](https://intranet.hbtn.io/rltoken/G5p7gU70olYFxbN_DfuXpQ) 

* [Shell Arithmetic](https://intranet.hbtn.io/rltoken/C2JAWjeSMt5I0EmuplF32A) 

* [Variables](https://intranet.hbtn.io/rltoken/zj7i19F9iE9eUdjBgR6C3Q) 

* [Shell initialization files](https://intranet.hbtn.io/rltoken/lHvzUhLmLgBVfsoJzYDj_w) 

* [The alias Command](https://intranet.hbtn.io/rltoken/5JiNabFuBFXpJKqGGh9EjQ) 

* [Technical Writing](https://intranet.hbtn.io/rltoken/lPsbE1Ecs4tmGU2RuTZ5YA) 

man or help :
*  ` printenv ` 
*  ` set ` 
*  ` unset ` 
*  ` export ` 
*  ` alias ` 
*  ` unalias ` 
*  ` . ` 
*  ` source ` 
*  ` printf ` 

## Learning Objectives

At the end of this project, you are expected to be able to  [explain to anyone](https://intranet.hbtn.io/rltoken/73iGFpBHBJtQgO1RmDM-_A) 
 ,  without the help of Google :

### General

* What happens when you type  ` $ ls -l *.txt ` 

### Shell Initialization Files

* What are the  ` /etc/profile `  file and the  ` /etc/profile.d `  directory

* What is the  ` ~/.bashrc `  file

### Variables

* What is the difference between a local and a global variable

* What is a reserved variable

* How to create, update and delete shell variables

* What are the roles of the following reserved variables: HOME, PATH, PS1

* What are special parameters

* What is the special parameter  ` $? ` ?

### Expansions

* What is expansion and how to use them

* What is the difference between single and double quotes and how to use them properly

* How to do command substitution with  ` $() `  and backticks

### Shell Arithmetic

* How to perform arithmetic operations with the shell

### The alias Command

* How to create an alias

* How to list aliases

* How to temporarily disable an alias

### Other help pages

* How to execute commands from a file in the current shell

## Requirements

### General

* Allowed editors:  ` vi ` ,  ` vim ` ,  ` emacs ` 

* All your scripts will be tested on Ubuntu 20.04 LTS

* All your scripts should be exactly two lines long ( ` $ wc -l file `  should print 2)

* All your files should end with a new line ([why?](http://unix.stackexchange.com/questions/18743/whats-the-point-in-adding-a-new-line-to-the-end-of-a-file/18789) 
)

* The first line of all your files should be exactly  ` #!/bin/bash `

* A  ` README.md `  file, at the root of the folder of the project, describing what each script is doing

* You are not allowed to use  ` && ` ,  ` || `  or  ` ; ` 

* You are not allowed to use  ` bc ` ,  ` sed `  or  ` awk ` 

* All your files must be executable

## More Info

Read your   ` /etc/profile `  ,   ` /etc/inputrc `   and   ` ~/.bashrc `   files.

Look at some files in the   ` /etc/profile.d `   directory.

Note: You do not have to learn about   ` awk `  ,   ` tar `  ,   ` bzip2 `  ,   ` date `  ,   ` scp `  ,   ` ulimit `  ,   ` umask `  , or shell scripting, yet.

## Installation

` git clone https://github.com/Imanolasolo/holberton-system_engineering-devops.git ` for command line.

[link to repo](https://github.com/Imanolasolo/holberton-system_engineering-devops.git)

## Tasks

### 0. <o>

Create a script that creates an alias.

* Name:  ` ls ` 

* Value:  ` rm * ` 

```bash
julien@ubuntu:/tmp/0x03$ ls
0-alias  file1  file2
julien@ubuntu:/tmp/0x03$ source ./0-alias 
julien@ubuntu:/tmp/0x03$ ls
julien@ubuntu:/tmp/0x03$ \ls
julien@ubuntu:/tmp/0x03$ 

```

Github information Repo:

* GitHub repository:  ` holberton-system_engineering-devops ` 

* Directory:  ` 0x03-shell_variables_expansions ` 

* File:  

[0-alias](https://github.com/Imanolasolo/holberton-system_engineering-devops/blob/main/0x03-shell_variables_expansions/0-alias) ` 
 
### 1. Hello you

Create a script that prints   ` hello user `  , where user is the current Linux user.

```bash
julien@ubuntu:/tmp/0x03$ id
uid=1000(julien) gid=1000(julien) groups=1000(julien),4(adm),24(cdrom),27(sudo),30(dip),46(plugdev),113(lpadmin),128(sambashare)
julien@ubuntu:/tmp/0x03$ ./1-hello_you 
hello julien
julien@ubuntu:/tmp/0x03$ 

```

Github information Repo:

* GitHub repository:  ` holberton-system_engineering-devops ` 

* Directory:  ` 0x03-shell_variables_expansions ` 

* File:  

[1-hello_you](https://github.com/Imanolasolo/holberton-system_engineering-devops/blob/main/0x03-shell_variables_expansions/1-hello_you) 

### 2. The path to success is to take massive, determined action

Add   ` /action `   to the   ` PATH `  .  ` /action `   should be the last directory the shell looks into when looking for a program.

```bash
julien@ubuntu:/tmp/0x03$ echo $PATH
/home/julien/bin:/home/julien/.local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin
julien@ubuntu:/tmp/0x03$ source ./2-path 
julien@ubuntu:/tmp/0x03$ echo $PATH
/home/julien/bin:/home/julien/.local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin:/action
julien@ubuntu:/tmp/0x03$ 

```

Github information Repo:

* GitHub repository:  ` holberton-system_engineering-devops ` 

* Directory:  ` 0x03-shell_variables_expansions ` 

* File:  

[2-path](https://github.com/Imanolasolo/holberton-system_engineering-devops/blob/main/0x03-shell_variables_expansions/2-path) 

### 3. If the path be beautiful, let us not ask where it leads

Create a script that counts the number of directories in the   ` PATH `  .

```bash
julien@ubuntu:/tmp/0x03$ echo $PATH
/home/julien/bin:/home/julien/.local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin
julien@ubuntu:/tmp/0x03$ . ./3-paths 
11
julien@ubuntu:/tmp/0x03$ PATH=/home/julien/bin:/home/julien/.local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin:::::/hello
julien@ubuntu:/tmp/0x03$ . ./3-paths 
12
julien@ubuntu:/tmp/0x03$ 

```

Github information Repo:

* GitHub repository:  ` holberton-system_engineering-devops ` 

* Directory:  ` 0x03-shell_variables_expansions `

* File:  

[3-paths](https://github.com/Imanolasolo/holberton-system_engineering-devops/blob/main/0x03-shell_variables_expansions/3-paths) 

### 4. Global variables

Create a script that lists environment variables.

```bash
julien@ubuntu:/tmp/0x03$ source ./4-global_variables
CC=gcc
CDPATH=.:~:/usr/local:/usr:/
CFLAGS=-O2 -fomit-frame-pointer
COLORTERM=gnome-terminal
CXXFLAGS=-O2 -fomit-frame-pointer
DISPLAY=:0
DOMAIN=hq.garrels.be
e=
TOR=vi
FCEDIT=vi
FIGNORE=.o:~
G_BROKEN_FILENAMES=1
GDK_USE_XFT=1
GDMSESSION=Default
GNOME_DESKTOP_SESSION_ID=Default
GTK_RC_FILES=/etc/gtk/gtkrc:/nethome/franky/.gtkrc-1.2-gnome2
GWMCOLOR=darkgreen
GWMTERM=xterm
HISTFILESIZE=5000
history_control=ignoredups
HISTSIZE=2000
HOME=/nethome/franky
HOSTNAME=octarine.hq.garrels.be
INPUTRC=/etc/inputrc
IRCNAME=franky
JAVA_HOME=/usr/java/j2sdk1.4.0
LANG=en_US
LDFLAGS=-s
LD_LIBRARY_PATH=/usr/lib/mozilla:/usr/lib/mozilla/plugins
LESSCHARSET=latin1
LESS=-edfMQ
LESSOPEN=|/usr/bin/lesspipe.sh %s
LEX=flex
LOCAL_MACHINE=octarine
LOGNAME=franky
[...]
julien@ubuntu:/tmp/0x03$ 

```

Github information Repo:

* GitHub repository:  ` holberton-system_engineering-devops ` 

* Directory:  ` 0x03-shell_variables_expansions ` 

* File:  

[4-global_variables](https://github.com/Imanolasolo/holberton-system_engineering-devops/blob/main/0x03-shell_variables_expansions/4-global_variables) 
 
### 5. Local variables

Create a script that lists all local variables and environment variables, and functions.

```bash
julien@ubuntu:/tmp/0x03$ . ./5-local_variables
BASH=/bin/bash
BASHOPTS=checkwinsize:cmdhist:complete_fullquote:expand_aliases:extglob:extquote:force_fignore:histappend:interactive_comments:progcomp:promptvars:sourcepath
BASH_ALIASES=()
BASH_ARGC=()
BASH_ARGV=()
BASH_CMDS=()
BASH_COMPLETION_COMPAT_DIR=/etc/bash_completion.d
BASH_LINENO=()
BASH_REMATCH=()
BASH_SOURCE=()
BASH_VERSINFO=([0]="4" [1]="3" [2]="46" [3]="1" [4]="release" [5]="x86_64-pc-linux-gnu")
BASH_VERSION='4.3.46(1)-release'
CLUTTER_IM_MODULE=xim
COLUMNS=133
COMPIZ_CONFIG_PROFILE=ubuntu
COMP_WORDBREAKS=$' \t\n"\'><=;|&(:'
DBUS_SESSION_BUS_ADDRESS=unix:abstract=/tmp/dbus-Fg27Lr20bq
DEFAULTS_PATH=/usr/share/gconf/ubuntu.default.path
DESKTOP_SESSION=ubuntu
[...]
julien@ubuntu:/tmp/0x03$ 

```

Github information Repo:

* GitHub repository:  ` holberton-system_engineering-devops ` 

* Directory:  ` 0x03-shell_variables_expansions ` 

* File:  

[5-local_variables](https://github.com/Imanolasolo/holberton-system_engineering-devops/blob/main/0x03-shell_variables_expansions/5-local_variables) 

### 6. Local variable

Create a script that creates a new local variable.

* Name:  ` BEST `

* Value:  ` School ` 

Github information Repo:

* GitHub repository:  ` holberton-system_engineering-devops ` 

* Directory:  ` 0x03-shell_variables_expansions ` 

* File:  

[6-create_local_variable](https://github.com/Imanolasolo/holberton-system_engineering-devops/blob/main/0x03-shell_variables_expansions/6-create_local_variable) 
 
### 7. Global variable

Create a script that creates a new global variable

* Name: ` BEST `

* Value:  ` School ` 

Github information Repo:

* GitHub repository:  ` holberton-system_engineering-devops ` 

* Directory:  ` 0x03-shell_variables_expansions `

* File:  

[7-create_global_variable](https://github.com/Imanolasolo/holberton-system_engineering-devops/blob/main/0x03-shell_variables_expansions/7-create_global_variable) ` 

### 8. Every addition to true knowledge is an addition to human power

Write a script that prints the result of the addition of 128 with the value stored in the environment variable  ` TRUEKNOWLEDGE `  , followed by a new line.

```bash
julien@production-503e7013:~$ export TRUEKNOWLEDGE=1209
julien@production-503e7013:~$ ./8-true_knowledge | cat -e
1337$
julien@production-503e7013:~$

```

Github information Repo:

* GitHub repository:  ` holberton-system_engineering-devops `

* Directory:  ` 0x03-shell_variables_expansions `

* File:  

[8-true_knowledge](https://github.com/Imanolasolo/holberton-system_engineering-devops/blob/main/0x03-shell_variables_expansions/8-true_knowledge) 
 
### 9. Divide and rule

Write a script that prints the result of   ` POWER `   divided by   ` DIVIDE `  , followed by a new line.
*  ` POWER `  and  ` DIVIDE `  are environment variables

```bash
julien@production-503e7013:~$ export POWER=42784
julien@production-503e7013:~$ export DIVIDE=32
julien@production-503e7013:~$ ./9-divide_and_rule | cat -e
1337$
julien@production-503e7013:~$

```

Github information Repo:

* GitHub repository:  ` holberton-system_engineering-devops `

* Directory:  ` 0x03-shell_variables_expansions ` 

* File:  

[9-divide_and_rule](https://github.com/Imanolasolo/holberton-system_engineering-devops/blob/main/0x03-shell_variables_expansions/9-divide_and_rule) 

### 10. Love is anterior to life, posterior to death, initial of creation, and the exponent of breath

Write a script that displays the result of   ` BREATH `   to the power   ` LOVE `

*  ` BREATH `  and  ` LOVE `  are environment variables

* The script should display the result, followed by a new line

```bash
julien@production-503e7013:~/$ export BREATH=4
julien@production-503e7013:~/$ export LOVE=3
julien@production-503e7013:~/$ ./10-love_exponent_breath
64
julien@production-503e7013:~/$

```

Github information Repo:

* GitHub repository:  ` holberton-system_engineering-devops `

* Directory:  ` 0x03-shell_variables_expansions `

* File:  

[10-love_exponent_breath](https://github.com/Imanolasolo/holberton-system_engineering-devops/blob/main/0x03-shell_variables_expansions/10-love_exponent_breath)  

### 11. There are 10 types of people in the world -- Those who understand binary, and those who don't

Write a script that converts a number from base 2 to base 10.

* The number in base 2 is stored in the environment variable  ` BINARY `

* The script should display the number in base 10, followed by a new line

```bash
julien@production-503e7013:~/$ export BINARY=10100111001
julien@production-503e7013:~/$ ./11-binary_to_decimal
1337
julien@production-503e7013:~/$

```

Github information Repo:

* GitHub repository:  ` holberton-system_engineering-devops `

* Directory:  ` 0x03-shell_variables_expansions `

* File:  

[11-binary_to_decimal](https://github.com/Imanolasolo/holberton-system_engineering-devops/blob/main/0x03-shell_variables_expansions/11-binary_to_decimal) 

### 12. Combination

Create a script that prints all possible combinations of two letters, except   ` oo `  .
* Letters are lower cases, from  ` a `  to  ` z `

* One combination per line

* The output should be alpha ordered, starting with  ` aa ` 

* Do not print  ` oo `

* Your script file should contain maximum 64 characters

```bash
julien@ubuntu:/tmp/0x03$ echo $((26 ** 2 -1))
675
julien@ubuntu:/tmp/0x03$ ./12-combinations | wc -l
675
julien@ubuntu:/tmp/0x03$ 
julien@ubuntu:/tmp/0x03$ ./12-combinations | tail -303 | head -10
oi
oj
ok
ol
om
on
op
oq
or
os
julien@ubuntu:/tmp/0x03$ 

```

 Task URLs  Github information Repo:

* GitHub repository:  ` holberton-system_engineering-devops `

* Directory:  ` 0x03-shell_variables_expansions `

* File: 

[12-combinations](https://github.com/Imanolasolo/holberton-system_engineering-devops/blob/main/0x03-shell_variables_expansions/12-combinations) 
 
### 13. Floats

Write a script that prints a number with two decimal places, followed by a new line.

The number will be stored in the environment variable   ` NUM `  .

```bash
ubuntu@ip-172-31-63-244:~/0x03$ export NUM=0
ubuntu@ip-172-31-63-244:~/0x03$ ./13-print_float
0.00
ubuntu@ip-172-31-63-244:~/0x03$ export NUM=98
ubuntu@ip-172-31-63-244:~/0x03$ ./13-print_float
98.00
ubuntu@ip-172-31-63-244:~/0x03$ export NUM=3.14159265359
ubuntu@ip-172-31-63-244:~/0x03$ ./13-print_float
3.14
ubuntu@ip-172-31-63-244:~/0x03$

```

Github information Repo:

* GitHub repository:  ` holberton-system_engineering-devops ` 

* Directory:  ` 0x03-shell_variables_expansions ` 

* File:  

[13-print_float](https://github.com/Imanolasolo/holberton-system_engineering-devops/blob/main/0x03-shell_variables_expansions/13-print_float) 

### 14. Decimal to Hexadecimal

Write a script that converts a number from base 10 to base 16.

* The number in base 10 is stored in the environment variable  ` DECIMAL ` 

* The script should display the number in base 16, followed by a new line

```bash
julien@production-503e7013:~/$ export DECIMAL=16
julien@production-503e7013:~/$ ./100-decimal_to_hexadecimal
10
julien@production-503e7013:~/$ export DECIMAL=1337
julien@production-503e7013:~/$ ./100-decimal_to_hexadecimal | cat -e
539$
julien@production-503e7013:~/$ export DECIMAL=15
julien@production-503e7013:~/$ ./100-decimal_to_hexadecimal | cat -e
f$
julien@production-503e7013:~/$

```

Github information Repo:

* GitHub repository:  ` holberton-system_engineering-devops ` 

* Directory:  ` 0x03-shell_variables_expansions `

* File:  

[100-decimal_to_hexadecimal](https://github.com/Imanolasolo/holberton-system_engineering-devops/blob/main/0x03-shell_variables_expansions/100-decimal_to_hexadecimal) 
 
### 15. What is the difference between a hard link and a symbolic link?

Write a blog post explaining what are hard and symbolic links on Linux, how to create them, and what is the difference between the two. Use examples to illustrate.

* Have at least one picture, at the top of the blog post

* Publish your blog post on Medium or LinkedIn

* Share your blog post at least on LinkedIn

When done, please add all urls below (blog post, LinkedIn post, etc.)

Please, remember that these blogs must be written in English to further your technical ability in a variety of settings

[https://codecodix.blogspot.com/2021/10/what-are-hard-and-symbolic-links-on.html](https://codecodix.blogspot.com/2021/10/what-are-hard-and-symbolic-links-on.html) 

Repo:

* GitHub repository:  ` holberton-system_engineering-devops ` 
 
### 16. Everyone is a proponent of strong encryption

Write a script that encodes and decodes text using the rot13 encryption. Assume ASCII.

```bash
julien@production-503e7013:~/shell/fun_with_the_shell$ cat quote
"Everyone is a proponent of strong encryption."
- Dorothy E. Denning
julien@production-503e7013:~/shell/fun_with_the_shell$ ./101-rot13 < quote
"Rirelbar vf n cebcbarag bs fgebat rapelcgvba."
- Qbebgul R. Qraavat
julien@production-503e7013:~/shell/fun_with_the_shell$


```

Github information Repo:

* GitHub repository:  ` holberton-system_engineering-devops ` 

* Directory:  ` 0x03-shell_variables_expansions ` 

* File:  

[101-rot13](https://github.com/Imanolasolo/holberton-system_engineering-devops/blob/main/0x03-shell_variables_expansions/101-rot13) 

### 17. The eggs of the brood need to be an odd number

Write a script that prints every other line from the input, starting with the first line.

```bash
ubuntu@ip-172-31-63-244:/$ \ls -1
bin
boot
dev
etc
home
initrd.img
lib
lib32
lib64
libx32
lost+found
media
mnt
opt
proc
root
run
sbin
srv
sys
t
#t#
t~
tmp
usr
var
vmlinuz
whoareyou
ubuntu@ip-172-31-63-244:/$ \ls -1 | ./102-odd
bin
dev
home
lib
lib64
lost+found
mnt
proc
run
srv
t
t~
usr
vmlinuz
ubuntu@ip-172-31-63-244:/$

```

Github information Repo:

* GitHub repository:  ` holberton-system_engineering-devops ` 

* Directory:  ` 0x03-shell_variables_expansions `

* File:  

[102-odd](https://github.com/Imanolasolo/holberton-system_engineering-devops/blob/main/0x03-shell_variables_expansions/102-odd) 
 
### 18. I'm an instant star. Just add water and stir.

Write a shell script that adds the two numbers stored in the environment variables   ` WATER `    and   ` STIR `    and prints the result.

*  ` WATER `   is in base  ` water ` 

*  ` STIR `   is in base  ` stir. `

* The result should be in base  ` bestchol `

```bash
julien@production-503e7013:~$ export WATER="ewwatratewa"
julien@production-503e7013:~$ export STIR="ti.itirtrtr"
julien@production-503e7013:~$ ./103-water_and_stir
shtbeolhc
julien@production-503e7013:~$

```

Github information Repo:

* GitHub repository:  ` holberton-system_engineering-devops `

* Directory:  ` 0x03-shell_variables_expansions `

* File:  

[103-water_and_stir](https://github.com/Imanolasolo/holberton-system_engineering-devops/blob/main/0x03-shell_variables_expansions/103-water_and_stir) 

## Credits

## Author(s):blue_book:

Work is owned and maintained by:

* Imanol Asolo <[3848](mailto:3848@holbertonschool.com)> [![M](https://upload.wikimedia.org/wikipedia/commons/thumb/9/91/Octicons-mark-github.svg/25px-Octicons-mark-github.svg.png)](https://github.com/Imanolasolo) [![M](https://upload.wikimedia.org/wikipedia/fr/thumb/c/c8/Twitter_Bird.svg/25px-Twitter_Bird.svg.png)](https://twitter.com/jjusturi) [![M](https://upload.wikimedia.org/wikipedia/commons/thumb/c/ca/LinkedIn_logo_initials.png/25px-LinkedIn_logo_initials.png)](https://www.linkedin.com/in/imanol-asolo-5ba9b42a/)


## Acknowledgments :mega: 

### **`Holberton School`** (*providing guidance*)

This program was written as part of the curriculum for Holberton School.
Holberton School is a campus-based full-stack software engineering program
that prepares students for careers in the tech industry using project-based
peer learning. For more information, visit [this link](https://www.holbertonschool.com/).
<p align="center">
	<img src="https://assets.website-files.com/6105315644a26f77912a1ada/610540e8b4cd6969794fe673_Holberton_School_logo-04-04.svg" alt="This is a secret;)">
</p>