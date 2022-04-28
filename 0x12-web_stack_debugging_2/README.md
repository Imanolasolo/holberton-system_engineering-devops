0x12. Web stack debugging #2
============================

This was the third in a series of web stack debugging projects. In these projects, I was given broken/bugged webstacks in isolated containers, and tasked with fixing the web stack to a working state. For each task, I wrote a script automating the commands necessary to fix the web stack.

![Logo](https://www.howtogeek.com/wp-content/uploads/2021/05/laptop-with-terminal-big.png?height=200p&trim=2,2,2,50)

Concepts
--------

_For this project, students are expected to look at this concept:_

*   [Web stack debugging](https://intranet.hbtn.io/concepts/68)

Dependences
-----------

### 0\. Run software as another user

The user `root` is, on Linux, the “superuser”. It can do anything it wants, that’s a good and bad thing. A good practice is that one should never be logged in the `root` user, as if you fat finger a command and for example run `rm -rf /`, there is no comeback. That’s why it is preferable to run as a privileged user, meaning that the user also has the ability to perform tasks that the `root` user can do, just need to use a specific command that you need to discover.

For the containers that you are given in this project as well as the checker, everything is run under the `root` user, which has the ability to run anything as another user.

Requirements:

*   write a Bash script that accepts one argument
*   the script should run the `whoami` command under the user passed as an argument
*   make sure to try your script by passing different users

Example:

    root@ubuntu:~# whoami
    root
    root@ubuntu:~# ./0-iamsomeoneelse www-data
    www-data
    root@ubuntu:~# whoami
    root
    root@ubuntu:~#
    

**Repo:**

*   GitHub repository: `holberton-system_engineering-devops`
*   Directory: `0x12-web_stack_debugging_2`
*   File: [0-iamsomeoneelse](https://github.com/Imanolasolo/holberton-system_engineering-devops/blob/main/0x12-web_stack_debugging_2/0-iamsomeoneelse)

### 1\. Run Nginx as Nginx

The `root` user is a superuser that can do anything on a Unix machine, the top administrator. Security wise, you must do everything that you can to prevent an attacker from logging in as `root`. With this in mind, it’s a good practice not to run your web servers as `root` (which is the default for most configurations) and instead run the process as the less privileged `nginx` user instead. This way, if a hacker does find a security issue that allows them to break-in to your server, the impact is limited by the permissions of the `nginx` user.

Fix this container so that Nginx is running as the `nginx` user.

Requirements:

*   `nginx` must be running as `nginx` user
*   `nginx` must be listening on all active IPs on port `8080`
*   You cannot use `apt-get remove`
*   Write a Bash script that configures the container to fit the above requirements

After debugging:

    root@ab6f4542747e:~# ps auxff | grep ngin[x]
    nginx      884  0.0  0.0  77360  2744 ?        Ss   19:16   0:00 nginx: master process /usr/sbin/nginx
    nginx      885  0.0  0.0  77712  2772 ?        S    19:16   0:00  \_ nginx: worker process
    nginx      886  0.0  0.0  77712  3180 ?        S    19:16   0:00  \_ nginx: worker process
    nginx      887  0.0  0.0  77712  3180 ?        S    19:16   0:00  \_ nginx: worker process
    nginx      888  0.0  0.0  77712  3208 ?        S    19:16   0:00  \_ nginx: worker process
    root@ab6f4542747e:~#
    root@ab6f4542747e:~# nc -z 0 8080 ; echo $?
    0
    root@ab6f4542747e:~#
    

**Repo:**

*   GitHub repository: `holberton-system_engineering-devops`
*   Directory: `0x12-web_stack_debugging_2`
*   File: [1-run_nginx_as_nginx](https://github.com/Imanolasolo/holberton-system_engineering-devops/blob/main/0x12-web_stack_debugging_2/1-run_nginx_as_nginx)

### 2\. 7 lines or less

Using what you did for task #1, make your fix short and sweet.

Requirements:

*   Your Bash script must be 7 lines long or less
*   There must be a new line at the end of the file
*   You respect Bash script requirements
*   You cannot use `;`
*   You cannot use `&&`
*   You cannot use `wget`
*   You cannot execute your previous answer file (Do not include the name of the previous script in this one)

**Repo:**

*   GitHub repository: `holberton-system_engineering-devops`
*   Directory: `0x12-web_stack_debugging_2`
*   File: [100-fix_in_7_lines_or_less]()

## Installing, compiling and using
	
> Only install cloning this repository on your local device:  https://github.com/Imanolasolo/holberton-system_engineering-devops.git

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
