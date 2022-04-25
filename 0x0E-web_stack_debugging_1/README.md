0x0E. Web stack debugging #1
============================

This was the second in a series of web stack debugging projects. In these projects, I was given broken/bugged webstacks in isolated containers, and tasked with fixing the web stack to a working state. For each task, I wrote a script automating the commands necessary to fix the web stack.

![Logo](https://www.howtogeek.com/wp-content/uploads/2021/05/laptop-with-terminal-big.png?height=200p&trim=2,2,2,50)

Concepts
--------

_For this project, students are expected to look at these concepts:_

*   [Network basics](https://intranet.hbtn.io/concepts/33)
*   [Web stack debugging](https://intranet.hbtn.io/concepts/68)

Tasks
-----

### 0\. Nginx likes port 80

Using your debugging skills, find out what’s keeping your Ubuntu container’s Nginx installation from listening on port `80`. Feel free to install whatever tool you need, start and destroy as many containers as you need to debug the issue. Then, write a Bash script with the minimum number of commands to automate your fix.

Requirements:

*   Nginx must be running, and listening on port `80` of all the server’s active IPv4 IPs
*   Write a Bash script that configures a server to the above requirements

    root@966c5664b21f:/# curl 0:80
    curl: (7) Failed to connect to 0 port 80: Connection refused
    root@966c5664b21f:/#
    root@966c5664b21f:/# ./0-nginx_likes_port_80 > /dev/null 2&>1
    root@966c5664b21f:/#
    root@966c5664b21f:/# curl 0:80
    <!DOCTYPE html>
    <html>
    <head>
    <title>Welcome to nginx!</title>
    <style>
        body {
            width: 35em;
            margin: 0 auto;
            font-family: Tahoma, Verdana, Arial, sans-serif;
        }
    </style>
    </head>
    <body>
    <h1>Welcome to nginx!</h1>
    <p>If you see this page, the nginx web server is successfully installed and
    working. Further configuration is required.</p>
    
    <p>For online documentation and support please refer to
    <a href="http://nginx.org/">nginx.org</a>.<br/>
    Commercial support is available at
    <a href="http://nginx.com/">nginx.com</a>.</p>
    
    <p><em>Thank you for using nginx.</em></p>
    </body>
    </html>
    root@966c5664b21f:/#
    

**Repo:**

*   GitHub repository: `holberton-system_engineering-devops`
*   Directory: `0x0E-web_stack_debugging_1`
*   File: [0-nginx_likes_port_80]()

### 1\. Make it sweet and short

Using what you did for task #0, make your fix short and sweet.

Requirements:

*   Your Bash script must be 5 lines long or less
*   There must be a new line at the end of the file
*   You must respect usual Bash script requirements
*   You cannot use `;`
*   You cannot use `&&`
*   You cannot use `wget`
*   You cannot execute your previous answer file (Do not include the name of the previous script in this one)
*   `service` (init) must say that `nginx` is not running ← for real

    root@966c5664b21f:/# curl 0:80
    curl: (7) Failed to connect to 0 port 80: Connection refused
    root@966c5664b21f:/#
    root@966c5664b21f:/# cat -e 1-debugging_made_short | wc -l
    5
    root@966c5664b21f:/# ./1-debugging_made_short
    root@966c5664b21f:/# curl 0:80
    <!DOCTYPE html>
    <html>
    <head>
    <title>Welcome to nginx!</title>
    <style>
        body {
            width: 35em;
            margin: 0 auto;
            font-family: Tahoma, Verdana, Arial, sans-serif;
        }
    </style>
    </head>
    <body>
    <h1>Welcome to nginx!</h1>
    <p>If you see this page, the nginx web server is successfully installed and
    working. Further configuration is required.</p>
    
    <p>For online documentation and support please refer to
    <a href="http://nginx.org/">nginx.org</a>.<br/>
    Commercial support is available at
    <a href="http://nginx.com/">nginx.com</a>.</p>
    
    <p><em>Thank you for using nginx.</em></p>
    </body>
    </html>
    root@966c5664b21f:/#
    root@966c5664b21f:/# service nginx status
     * nginx is not running
    root@966c5664b21f:/# 
    

**Repo:**

*   GitHub repository: `holberton-system_engineering-devops`
*   Directory: `0x0E-web_stack_debugging_1`
*   File: [1-debugging_made_short]()

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
