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

-TCP/UDP

    > What are the 2 mainly used data transfer protocols for IP (transfer level on the OSI schema)

    > What is the main difference between TCP and UDP

    > What is a port

    > Memorize SSH, HTTP and HTTPS port numbers

    > What tool/protocol is often used to check if a device is connected to a network

## Dependences 

	
> [0-OSI_model](https://github.com/Imanolasolo/holberton-system_engineering-devops/blob/main/0x06-regular_expressions/0-simply_match_school.rb) --> Answer to:

Questions:

- What is the OSI model?

1. Set of specifications that network hardware manufacturers must respect

2. The OSI model is a conceptual model that characterizes the communication functions of a telecommunication system without regard to their underlying internal structure and technology

3. The OSI model is a model that characterizes the communication functions of a telecommunication system with a strong regard for their underlying internal structure and technology

- How is the OSI model organized?

    1. Alphabetically

    2. From the lowest to the highest level

    3. Randomly

> [README.md](https://github.com/Imanolasolo/holberton-system_engineering-devops/blob/main/0x06-regular_expressions/README.md) ---> README file to show the project insights. 

>[1-types_of_network](https://github.com/Imanolasolo/holberton-system_engineering-devops/blob/main/0x06-regular_expressions/1-repetition_token_0.rb) ---> Answer to:

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

>[2-MAC_and_IP_address](https://github.com/Imanolasolo/holberton-system_engineering-devops/blob/main/0x06-regular_expressions/2-repetition_token_1.rb) ---> Answer to:

- What is a MAC address?

    1. The name of a network interface

    2. The unique identifier of a network interface

    3. A network interface

- What is an IP address?

    1. Is to devices connected to a network what postal address is to houses

    2. The unique identifier of a network interface

    3. Is a number that network devices use to connect to networks

>[3-repetition_token_2.rb](https://github.com/Imanolasolo/holberton-system_engineering-devops/blob/main/0x06-regular_expressions/3-repetition_token_2.rb) --> Ruby script that accepts one argument and pass it to a regular expression matching method.
	![image](https://user-images.githubusercontent.com/86312558/155395077-950bf7e1-dd62-484a-88d8-6af9e658cea3.png)


![image](https://holbertonintranet.s3.amazonaws.com/uploads/medias/2020/9/3b6bf4aeca6a0c2de584e7f5d68d11eef57ce205.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIARDDGGGOU5BHMTQX4%2F20220223%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20220223T162015Z&X-Amz-Expires=86400&X-Amz-SignedHeaders=host&X-Amz-Signature=dc1c5e62d7c3243cbd084decc35e441c5aa55e33c65328520e87d99995a777d5)

>[4-repetition_token_3.rb](https://github.com/Imanolasolo/holberton-system_engineering-devops/blob/main/0x06-regular_expressions/4-repetition_token_3.rb) --> Ruby script that accepts one argument and pass it to a regular expression matching method.

![image](https://holbertonintranet.s3.amazonaws.com/uploads/medias/2020/9/f8dbcb9cf5ae569a8645027dc46e81cb372ce28e.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIARDDGGGOU5BHMTQX4%2F20220223%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20220223T162015Z&X-Amz-Expires=86400&X-Amz-SignedHeaders=host&X-Amz-Signature=e000bf87085ef963cd47e22ca255b31fd9e4b045484a7315b0e19f04d0ba536b)

>[5-dont_stop_me_now](https://github.com/Imanolasolo/holberton-system_engineering-devops/blob/main/0x06-regular_expressions/5-beginning_and_end.rb) --> Ruby script that accepts one argument and pass it to a regular expression matching method.

- The regular expression must be exactly matching a string that `starts with h ends with n and can have any single character in between`

>[6-phone_number.rb](https://github.com/Imanolasolo/holberton-system_engineering-devops/blob/main/0x06-regular_expressions/6-phone_number.rb) --> The regular expression must match a 10 digit phone number

>[7-OMG_WHY_ARE_YOU_SHOUTING.rb](https://github.com/Imanolasolo/holberton-system_engineering-devops/blob/main/0x06-regular_expressions/7-OMG_WHY_ARE_YOU_SHOUTING.rb) --> The regular expression must be only matching: capital letters

>[100-textme.rb](https://github.com/Imanolasolo/holberton-system_engineering-devops/blob/main/0x06-regular_expressions/100-textme.rb) --> ne afternoon, a TextMe VoIP Engineer comes to you and explains she wants to run some statistics on the TextMe app text messages transactions.

Your script should output: [SENDER],[RECEIVER],[FLAGS]

The sender phone number or name (including country code if present)

The receiver phone number or name (including country code if present)

The flags that were used

>[101-passed_linkedin_regex_challenge.jpg](https://github.com/Imanolasolo/holberton-system_engineering-devops/blob/main/0x06-regular_expressions/101-passed_linkedin_regex_challenge.jpg) -->  One way to get started in getting a Software Engineering job at LinkedIn is to solve their regex puzzle.

Requirements:

Solve LinkedIn regex puzzle: https://engineering.linkedin.com/puzzle

Provide as an answer file a screenshot of the “Congratulations” screen with the date and time of completion


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

[Regular expressions - basics](https://intranet.hbtn.io/rltoken/SJ2eQ7V2iQlCgLc-L96zWg)

[Regular expressions - advanced](https://intranet.hbtn.io/rltoken/qyjWL-J1_qUaZGR690gH1Q)

[Rubular is your best friend](https://intranet.hbtn.io/rltoken/WCjn8NgohbQ5NGXEObWZvQ)

[Use a regular expression against a problem: now you have 2 problems](https://intranet.hbtn.io/rltoken/Zfvv_ydOCvJ_YaBB6eDqVw)

[Learn Regular Expressions with simple, interactive exercises](https://intranet.hbtn.io/rltoken/Y-OVGcJ5cskdXWIBowiE_A)


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
