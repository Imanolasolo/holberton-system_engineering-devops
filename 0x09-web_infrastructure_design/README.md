# 0x08. Networking basics #1

<div style="text-align: justify">

Thank you for visiting this repository which contain my work about to introducing networking concepts. In this project, I drawed some diagrams covering the web stack that i built with the sysadmin/devops track projects.

![Logo](https://www.howtogeek.com/wp-content/uploads/2021/05/laptop-with-terminal-big.png?height=200p&trim=2,2,2,50)

# Getting Started :running:
<div style="text-align: justify">

## Table of Contents
* [AUTHORS](./AUTHORS)
* [MIT License](./LICENSE)
* [About](#about)
* [Dependences](#dependences)
* [Installing, compiling and using](#installing, compiling and using)
* [Builtins](#builtins)
* [Man page]
* [Credits](#credits)

## About
This directory contains a collection of files, functions, structs and scripts used to build and manage this repository. If there are any issues regarding the intention of a particular script (or even part of a certain script), please reach out to us.
	
	Contents:
    
- You must be able to explain what each component is doing

- You must be able to explain system redundancy

- Know all the mentioned acronyms: LAMP, SPOF, QPS

## Dependences 

>[README.me]() --> README file to show the project insights.
	
> [0-simple_web_stack](https://github.com/Imanolasolo/holberton-system_engineering-devops/blob/main/0x07-networking_basics/0-OSI_model) -->File where web direction of design is allocated.

> [0-simple_web_stack.jpg](https://github.com/Imanolasolo/holberton-system_engineering-devops/blob/main/0x07-networking_basics/README.md) ---> Design of one server web infrastructure that hosts the website that is reachable via www.foobar.com. 

>[0-simple_web_stack.md](https://github.com/Imanolasolo/holberton-system_engineering-devops/blob/main/0x07-networking_basics/1-types_of_network) ---> Extended explanation about one server web infrastructure that hosts the website that is reachable via www.foobar.com.

You must be able to explain some specifics about this infrastructure:

- What is a server

- What is the role of the domain name

- What type of DNS record www is in www.foobar.com

- What is the role of the web server

- What is the role of the application server

- What is the role of the database

- What is the server using to communicate with the computer of the user requesting the website

You must be able to explain what the issues are with this infrastructure:

- SPOF

- Downtime when maintenance needed (like deploying new code web server needs to be restarted)

- Cannot scale if too much incoming traffic

>[1-distributed_web_infrastructure](https://github.com/Imanolasolo/holberton-system_engineering-devops/blob/main/0x07-networking_basics/2-MAC_and_IP_address) ---> File where web direction of design is allocated.

>[1-distributed_web_infrastructure.png]() --> Design of a three server web infrastructure that hosts the website www.foobar.com.

>[1-distributed_web_infrastructure.md]() --> Extended explanation about three server web infrastructure that hosts the website www.foobar.com.

You must be able to explain some specifics about this infrastructure:

- For every additional element, why you are adding it

- What distribution algorithm your load balancer is configured with and how it works

- Is your load-balancer enabling an Active-Active or Active-Passive setup, explain the difference between both

- How a database Primary-Replica (Master-Slave) cluster works

- What is the difference between the Primary node and the Replica node in regard to the application

You must be able to explain what the issues are with this infrastructure:

- Where are SPOF

- Security issues (no firewall, no HTTPS)

- No monitoring

>[2-secured_and_monitored_web_infrastructure]() --> File where web direction of design is allocated.

>[2-secured_and_monitored_web_infrastructure.png]() --> Design of a three server web infrastructure that hosts the website www.foobar.com, it must be secured, serve encrypted traffic, and be monitored.

>[2-secured_and_monitored_web_infrastructure.md]() --> Extended explanation about three server web infrastructure that hosts the website www.foobar.com, it must be secured, serve encrypted traffic, and be monitored.

You must be able to explain some specifics about this infrastructure:

- For every additional element, why you are adding it

- What are firewalls for

- Why is the traffic served over HTTPS

- What monitoring is used for

- How the monitoring tool is collecting data

- Explain what to do if you want to monitor your web server QPS

You must be able to explain what the issues are with this infrastructure:

- Why terminating SSL at the load balancer level is an issue

- Why having only one MySQL server capable of accepting writes is an issue

- Why having servers with all the same components (database, web server and application server) might be a problem

## Installing, compiling and using
	
> Only install cloning this repository on your local device:  https://github.com/Imanolasolo/holberton-system_engineering-devops.git
	

## Builtins

No builtins created
		
## Man page

-  No man page

## Flowchart
	
- No flowchart

## Resources

**Read or watch:**

Network basics concept page

Server concept page

Web server concept page

DNS concept page

Load balancer concept page

Monitoring concept page

[What is a database](https://intranet.hbtn.io/rltoken/woDFYUG0y_SrA79AaYbFCA)

[What’s the difference between a web server and an app server?](https://intranet.hbtn.io/rltoken/Nb8B47Y2D8SLqQMOKVoQyQ)

[DNS record types](https://intranet.hbtn.io/rltoken/ojwHUACZEtIWfI9M6i7c3g)

[Single point of failure](https://intranet.hbtn.io/rltoken/wYpewVpIp9PSqqL27RPafg)

[How to avoid downtime when deploying new code](https://intranet.hbtn.io/rltoken/Mlvynt0OgLQXrxjrC5Wlnw)

[High availability cluster (active-active/active-passive](https://intranet.hbtn.io/rltoken/POX3jE0S6TChQHSYQraYeQ)

[What is HTTPS](https://intranet.hbtn.io/rltoken/N4BwU4wYDNW02kdzMiekFw)

[What is a firewall](https://intranet.hbtn.io/rltoken/ZFTutaKN4wWzmL4fWhQmeg)

## Usage



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
