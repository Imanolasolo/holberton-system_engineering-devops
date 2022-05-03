0x17. Web stack debugging #3
============================

This was the fourth in a series of web stack debugging projects. In these projects, I was given broken/bugged webstacks in isolated containers, and tasked with fixing the web stack to a working state. For each task, I wrote a script automating the commands necessary to fix the web stack.

![Logo](https://www.howtogeek.com/wp-content/uploads/2021/05/laptop-with-terminal-big.png?height=200p&trim=2,2,2,50)

Concepts
--------

_For this project, students are expected to look at these concepts:_

*   [Web Server](https://intranet.hbtn.io/concepts/17)
*   [Web stack debugging](https://intranet.hbtn.io/concepts/68)

Background Context
------------------

![](https://s3.amazonaws.com/intranet-projects-files/holbertonschool-sysadmin_devops/293/d42WuBh.png)

When debugging, sometimes logs are not enough. Either because the software is breaking in a way that was not expected and the error is not being logged, or because logs are not providing enough information. In this case, you will need to go down the stack, the good news is that this is something Holberton students can do :)

Wordpress is a very popular tool, it allows you to run blogs, portfolios, e-commerce and company websites… It [actually powers 26% of the web](https://intranet.hbtn.io/rltoken/Ah9_LmUi191dqxT-Zx7uhg "actually powers 26% of the web"), so there is a fair chance that you will end up working with it at some point in your career.

Wordpress is usually run on LAMP (Linux, Apache, MySQL, and PHP), which is a very widely used set of tools.

The web stack you are debugging today is a Wordpress website running on a LAMP stack.

More Info
---------

### Install `puppet-lint`

    $ apt-get install -y ruby
    $ gem install puppet-lint -v 2.1.1

Dependences
-----------

### 0\. Strace is your friend

Using `strace`, find out why Apache is returning a 500 error. Once you find the issue, fix it and then automate it using Puppet (instead of using Bash as you were previously doing).

Hint:

*   `strace` can attach to a current running process
*   You can use [tmux](https://intranet.hbtn.io/rltoken/4KkxME6-3aY9fgfok6HNFA "tmux") to run [strace](https://intranet.hbtn.io/rltoken/OUc10nTtuZG65adFVbkYag "strace") in one window and `curl` in another one

Requirements:

*   Your `0-strace_is_your_friend.pp` file must contain Puppet code
*   You can use whatever Puppet resource type you want for you fix

Example:

    root@e514b399d69d:~# curl -sI 127.0.0.1
    HTTP/1.0 500 Internal Server Error
    Date: Fri, 24 Mar 2017 07:32:16 GMT
    Server: Apache/2.4.7 (Ubuntu)
    X-Powered-By: PHP/5.5.9-1ubuntu4.21
    Connection: close
    Content-Type: text/html
    
    root@e514b399d69d:~# puppet apply 0-strace_is_your_friend.pp
    Notice: Compiled catalog for e514b399d69d.ec2.internal in environment production in 0.02 seconds
    Notice: /Stage[main]/Main/Exec[fix-wordpress]/returns: executed successfully
    Notice: Finished catalog run in 0.08 seconds
    root@e514b399d69d:~# curl -sI 127.0.0.1:80
    root@e514b399d69d:~#
    HTTP/1.1 200 OK
    Date: Fri, 24 Mar 2017 07:11:52 GMT
    Server: Apache/2.4.7 (Ubuntu)
    X-Powered-By: PHP/5.5.9-1ubuntu4.21
    Link: <http://127.0.0.1/?rest_route=/>; rel="https://api.w.org/"
    Content-Type: text/html; charset=UTF-8
    
    root@e514b399d69d:~# curl -s 127.0.0.1:80 | grep Holberton
    <title>Holberton &#8211; Just another WordPress site</title>
    <link rel="alternate" type="application/rss+xml" title="Holberton &raquo; Feed" href="http://127.0.0.1/?feed=rss2" />
    <link rel="alternate" type="application/rss+xml" title="Holberton &raquo; Comments Feed" href="http://127.0.0.1/?feed=comments-rss2" />
            <div id="wp-custom-header" class="wp-custom-header"><img src="http://127.0.0.1/wp-content/themes/twentyseventeen/assets/images/header.jpg" width="2000" height="1200" alt="Holberton" /></div>  </div>
                                <h1 class="site-title"><a href="http://127.0.0.1/" rel="home">Holberton</a></h1>
            <p>Yet another bug by a Holberton student</p>
    root@e514b399d69d:~#
    

**Repo:**

*   GitHub repository: `holberton-system_engineering-devops`
*   Directory: `0x17-web_stack_debugging_3`
*   File: [0-strace_is_your_friend.pp](https://github.com/Imanolasolo/holberton-system_engineering-devops/blob/main/0x17-web_stack_debugging_3/0-strace_is_your_friend.pp)

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

