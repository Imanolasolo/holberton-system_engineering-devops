# 0x07. Networking basics #0

<div style="text-align: justify">

Thank you for visiting this repository which contain my work about to introducing networking concepts. In this project, I answered a few quiz-like questions and wrote a couple bash scripts while learning about the OSI model, LAN and WAN networks, and TCP/UDP data transfer protocols.


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
    
- OSI Model

    > What it is

    > How many layers it has

    > How it is organized

- What is a LAN

    > Typical usage

    > Typical geographical size

- What is a WAN

    > Typical usage

    > Typical geographical size

- What is the Internet

    > What is an IP address

    > What are the 2 types of IP address

    > What is localhost

    > What is a subnet

    > Why IPv6 was created

- TCP/UDP

    > What are the 2 mainly used data transfer protocols for IP (transfer level on the OSI schema)

    > What is the main difference between TCP and UDP

    > What is a port

    > Memorize SSH, HTTP and HTTPS port numbers

    > What tool/protocol is often used to check if a device is connected to a network

## Dependences 

	
> [0-OSI_model](https://github.com/Imanolasolo/holberton-system_engineering-devops/blob/main/0x07-networking_basics/0-OSI_model) --> Answer to:

Questions:

- What is the OSI model?

    1. Set of specifications that network hardware manufacturers must respect

    2. The OSI model is a conceptual model that characterizes the communication functions of a telecommunication system without regard to their underlying internal structure and technology

    3. The OSI model is a model that characterizes the communication functions of a telecommunication system with a strong regard for their underlying internal structure and technology

- How is the OSI model organized?

    1. Alphabetically

    2. From the lowest to the highest level

    3. Randomly

> [README.md](https://github.com/Imanolasolo/holberton-system_engineering-devops/blob/main/0x07-networking_basics/README.md) ---> README file to show the project insights. 

>[1-types_of_network](https://github.com/Imanolasolo/holberton-system_engineering-devops/blob/main/0x07-networking_basics/1-types_of_network) ---> Answer to:

- What type of network a computer in local is connected to?

    1. Internet

    2. WAN

    3. LAN

- What type of network could connect an office in one building to another office in a building a few streets away?

    1. Internet

    2. WAN

    3. LAN

- What network do you use when you browse www.google.com from your smartphone (not connected to the Wifi)?

    1. Internet

    2. WAN

    3. LAN

>[2-MAC_and_IP_address](https://github.com/Imanolasolo/holberton-system_engineering-devops/blob/main/0x07-networking_basics/2-MAC_and_IP_address) ---> Answer to:

- What is a MAC address?

    1. The name of a network interface

    2. The unique identifier of a network interface

    3. A network interface

- What is an IP address?

    1. Is to devices connected to a network what postal address is to houses

    2. The unique identifier of a network interface

    3. Is a number that network devices use to connect to networks

>[3-UDP_and_TCP](https://github.com/Imanolasolo/holberton-system_engineering-devops/blob/main/0x07-networking_basics/3-UDP_and_TCP) --> Answer to:
	![image](https://user-images.githubusercontent.com/86312558/155395077-950bf7e1-dd62-484a-88d8-6af9e658cea3.png)

Given the draw, fill the gaps with the answers below.

- Which statement is correct for the TCP box:

    1. It is a protocol that is transferring data in a slow way but surely

    2. It is a protocol that is transferring data in a fast way and might loss data along in the process

- Which statement is correct for the UDP box:
    1. It is a protocol that is transferring data in a slow way but surely

    2. It is a protocol that is transferring data in a fast way and might loss data along in the process

- Which statement is correct for the TCP worker:

    1. Have you received boxes x, y, z?

    2. May I increase the rate at which I am sending you boxes?



>[4-TCP_and_UDP_ports](https://github.com/Imanolasolo/holberton-system_engineering-devops/blob/main/0x07-networking_basics/4-TCP_and_UDP_ports) --> Bash script that displays listening ports:

That only shows listening sockets

That shows the PID and name of the program to which each socket belongs


>[5-dont_stop_me_now](https://github.com/Imanolasolo/holberton-system_engineering-devops/blob/main/0x07-networking_basics/5-is_the_host_on_the_network) --> Bash script that pings an IP address passed as an argument.

Requirements:

Accepts a string as an argument

Displays Usage: 5-is_the_host_on_the_network {IP_ADDRESS} if no argument passed

Ping the IP 5 times




## Installing, compiling and using
	
> Only install cloning this repository on your local device:  https://github.com/Imanolasolo/holberton-system_engineering-devops.git
	
> Make the files executable with `chmod +x *(or filename)`
	
> Run the executable files with `./` 

## Builtins

No builtins created
		
## Man page

-  No man page

## Flowchart
	
- No flowchart

## Resources

**Read or watch**:

- [OSI model](https://intranet.hbtn.io/rltoken/ERGikvYsVP3sa9ZdlAAV4w)

- [Different types of network](https://intranet.hbtn.io/rltoken/H2peG3mV1MDDEK9c9FpGjA)

- [LAN network](https://intranet.hbtn.io/rltoken/GLVy5U4Ja4c2BnKYDPwT5Q)

- [WAN network](https://intranet.hbtn.io/rltoken/IghQOBbQi3Y-H82l3s9ERg)

- [Internet](https://intranet.hbtn.io/rltoken/osfQ04v-6oWuX4LdcpMYfQ)

- [MAC address](https://intranet.hbtn.io/rltoken/DjY02-vo10kphmiYSa2Msg)

- [What is an IP address](https://intranet.hbtn.io/rltoken/_pRm6TVS3zWV_cKg51Gn4Q)

- [Private and public address](https://intranet.hbtn.io/rltoken/Tj1tSxadTHv8kS9Q7lzTpQ)

- [IPv4 and IPv6](https://intranet.hbtn.io/rltoken/dhF14mh64BX6hULm9XPstg)

- [Localhost](https://intranet.hbtn.io/rltoken/uqDHdS73W-CJQakM8vERtQ)

- [TCP and UDP](https://intranet.hbtn.io/rltoken/nOeDjXQrw-N8eFmTBiuzqw)

- [TCP/UDP ports List](https://intranet.hbtn.io/rltoken/nOeDjXQrw-N8eFmTBiuzqw)

- [What is ping /ICMP](https://intranet.hbtn.io/rltoken/OPrB4crHtTLwUynA5YjVNw)

- [Positional parameters](https://intranet.hbtn.io/rltoken/yN_ZinFzBaLXuJhOhKiMfw)

man or help:
```
netstat
ping
```


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
