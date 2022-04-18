0x0A. Configuration management
==============================

In this project, I started working with `Puppet` as a configuration management tool. I practiced writing `Puppet manifest files` to create a file, install a package, and execute a command.

![Logo](https://www.howtogeek.com/wp-content/uploads/2021/05/laptop-with-terminal-big.png?height=200p&trim=2,2,2,50)

Background Context
------------------

Thanks to Puppet, we were able to restore our infrastructure to normal operation in under 1H, pretty impressive. Imagine if we had to do everything manually: launching the servers, configuring and linking them, importing application code, starting every process, and obviously, fixing all the bugs (you should know by now that complicated infrastructure always goes sideways)…

Resources
---------

**Read or watch**:

*   [Intro to Configuration Management](https://intranet.hbtn.io/rltoken/r-NmkYO8bxIKp2qEx2ZjKQ "Intro to Configuration Management")
*   [Puppet resource type: file](https://intranet.hbtn.io/rltoken/D0-IO_SIZSXYLKJs2BitYA "Puppet resource type: file") (_check “Resource types” for all manifest types in the left menu_)
*   [Puppet’s Declarative Language: Modeling Instead of Scripting](https://intranet.hbtn.io/rltoken/Fqmb5rnChQgYAypvKoTxAQ "Puppet's Declarative Language: Modeling Instead of Scripting")
*   [Puppet lint](https://intranet.hbtn.io/rltoken/oezu0m_hJ8nEVA6a9o17Tw "Puppet lint")
*   [Puppet emacs mode](https://intranet.hbtn.io/rltoken/N70cVw8mG3707He-OxjP1w "Puppet emacs mode")

Note on Versioning
------------------

Your Ubuntu 20.04 VM should have Puppet 5.5 preinstalled.

### Install `puppet`

    $ apt-get install -y ruby=1:2.7+1 --allow-downgrades
    $ apt-get install -y ruby-augeas
    $ apt-get install -y ruby-shadow
    $ apt-get install -y puppet
    

You do **not** need to attempt to upgrade versions. This project is simply a set of tasks to familiarize you with the basic level syntax which is virtually identical in newer versions of Puppet.

[Puppet 5 Docs](https://intranet.hbtn.io/rltoken/_xOod_Lzz8WKTbhpG5SWLQ "Puppet 5 Docs")

### Install `puppet-lint`

    $ gem install puppet-lint

Dependences
-----------

### 0\. Create a file

Using Puppet, create a file in `/tmp`.

Requirements:

*   File path is `/tmp/school`
*   File permission is `0744`
*   File owner is `www-data`
*   File group is `www-data`
*   File contains `I love Puppet`

Example:

    root@6712bef7a528:~# puppet-lint --version
    puppet-lint 2.5.2
    root@6712bef7a528:~# puppet-lint 0-create_a_file.pp
    root@6712bef7a528:~# 
    root@6712bef7a528:~# puppet apply 0-create_a_file.pp
    Notice: Compiled catalog for 6712bef7a528.ec2.internal in environment production in 0.04 seconds
    Notice: /Stage[main]/Main/File[school]/ensure: defined content as '{md5}f1b70c2a42a98d82224986a612400db9'
    Notice: Finished catalog run in 0.03 seconds
    root@6712bef7a528:~#
    root@6712bef7a528:~# ls -l /tmp/school
    -rwxr--r-- 1 www-data www-data 13 Mar 19 23:12 /tmp/school
    root@6712bef7a528:~# cat /tmp/school
    I love Puppetroot@6712bef7a528:~#
    

**Repo:**

*   GitHub repository: `holberton-system_engineering-devops`
*   Directory: `0x0A-configuration_management`
*   File: [0-create_a_file.pp]()

### 1\. Install a package

Using Puppet, install `puppet-lint`.

Requirements:

*   Install `puppet-lint`
*   Version must be `2.5.0`

Example:

    root@d391259bf577:/# puppet apply 1-install_a_package.pp
    Notice: Compiled catalog for d391259bf577 in environment production in 0.14 seconds
    Notice: Applied catalog in 0.20 seconds
    root@d391259bf577:/# gem list
    
    *** LOCAL GEMS ***
    
    puppet-lint (2.5.0)
    root@d391259bf577:/#
    

**Repo:**

*   GitHub repository: `holberton-system_engineering-devops`
*   Directory: `0x0A-configuration_management`
*   File: [1-install_a_package.pp]()

### 2\. Execute a command

Using Puppet, create a manifest that kills a process named `killmenow`.

Requirements:

*   Must use the `exec` Puppet resource
*   Must use `pkill`

Example:

Terminal #0 - starting my process

    root@d391259bf577:/# cat killmenow
    #!/bin/bash
    while [[ true ]]
    do
        sleep 2
    done
    
    root@d391259bf577:/# ./killmenow
    

Terminal #1 - executing my manifest

    root@d391259bf577:/# puppet apply 2-execute_a_command.pp
    Notice: Compiled catalog for d391259bf577.hsd1.ca.comcast.net in environment production in 0.01 seconds
    Notice: /Stage[main]/Main/Exec[killmenow]/returns: executed successfully
    Notice: Finished catalog run in 0.10 seconds
    root@d391259bf577:/# 
    

Terminal #0 - process has been terminated

    root@d391259bf577:/# ./killmenow
    Terminated
    root@d391259bf577:/#
    

**Repo:**

*   GitHub repository: `holberton-system_engineering-devops`
*   Directory: `0x0A-configuration_management`
*   File: [2-execute_a_command.pp]()

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

