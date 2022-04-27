0x0F. Load balancer
===================

In this project, I continued to build up the configuration of the web server issued in project 0x0B. I added two additional servers, one to replicate the Nginx configuration of my original server, and another to set up an HAproxy load balancer on to manage both web servers.

![Logo](https://www.howtogeek.com/wp-content/uploads/2021/05/laptop-with-terminal-big.png?height=200p&trim=2,2,2,50)

Concepts
--------

_For this project, students are expected to look at these concepts:_

*   [Load balancer](https://intranet.hbtn.io/concepts/46)
*   [Web stack debugging](https://intranet.hbtn.io/concepts/68)

Background Context
------------------

You have been given 2 additional servers:

*   gc-\[STUDENT\_ID\]-web-02-XXXXXXXXXX
*   gc-\[STUDENT\_ID\]-lb-01-XXXXXXXXXX

Let’s improve our web stack so that there is [redundancy](https://intranet.hbtn.io/rltoken/QiOC_I-8BeV4aNExIucC9Q "redundancy") for our web servers. This will allow us to be able to accept more traffic by doubling the number of web servers, and to make our infrastructure more reliable. If one web server fails, we will still have a second one to handle requests.

For this project, you will need to write Bash scripts to automate your work. All scripts must be designed to configure a brand new Ubuntu server to match the task requirements.

Resources
---------

**Read or watch**:

*   [Introduction to load-balancing and HAproxy](https://intranet.hbtn.io/rltoken/ngIXarEyu8jZwOL3Y30PLQ "Introduction to load-balancing and HAproxy")
*   [HTTP header](https://intranet.hbtn.io/rltoken/v32JmcDrSiOnFBfqzXvs_Q "HTTP header")
*   [Debian/Ubuntu HAProxy packages](https://intranet.hbtn.io/rltoken/BXGrW_6ocecWaOJb7OK_WA "Debian/Ubuntu HAProxy packages")

Dependences 
-----------

### 0\. Double the number of webservers

In this first task you need to configure `web-02` to be identical to `web-01`. Fortunately, you built a Bash script during your [web server project](https://intranet.hbtn.io/rltoken/YygI112jB085j-4C3dRX2A "web server project"), and they’ll now come in handy to easily configure `web-02`. Remember, always try to automate your work!

Since we’re placing our web servers behind a load balancer for this project, we want to add a custom Nginx response header. The goal here is to be able to track which web server is answering our HTTP requests, to understand and track the way a load balancer works. More in the coming tasks.

Requirements:

*   Configure Nginx so that its HTTP response contains a custom header (on `web-01` and `web-02`)
    *   The name of the custom HTTP header must be `X-Served-By`
    *   The value of the custom HTTP header must be the hostname of the server Nginx is running on
*   Write `0-custom_http_response_header` so that it configures a brand new Ubuntu machine to the requirements asked in this task
    *   [Ignore](https://intranet.hbtn.io/rltoken/3AOvROMUNUrzxEWhli4GTw "Ignore") [SC2154](https://intranet.hbtn.io/rltoken/i5f8DYX_rRYFz4hfbG_GJg "SC2154") for `shellcheck`

Example:

    sylvain@ubuntu$ curl -sI 34.198.248.145 | grep X-Served-By
    X-Served-By: 03-web-01
    sylvain@ubuntu$ curl -sI 54.89.38.100 | grep X-Served-By
    X-Served-By: 03-web-02
    sylvain@ubuntu$
    

If your server’s hostnames are not properly configured (`[STUDENT_ID]-web-01` and `[STUDENT_ID]-web-02`.), follow this [tutorial](https://intranet.hbtn.io/rltoken/h3tE_15RKe2QYWzPsjqNDA "tutorial").

**Repo:**

*   GitHub repository: `holberton-system_engineering-devops`
*   Directory: `0x0F-load_balancer`
*   File: [0-custom_http_response_header](https://github.com/Imanolasolo/holberton-system_engineering-devops/blob/main/0x0F-load_balancer/0-custom_http_response_header)

### 1\. Install your load balancer



Install and configure HAproxy on your `lb-01` server.

Requirements:

*   Configure HAproxy so that it send traffic to `web-01` and `web-02`
*   Distribute requests using a roundrobin algorithm
*   Make sure that HAproxy can be managed via an init script
*   Make sure that your servers are configured with the right hostnames: `[STUDENT_ID]-web-01` and `[STUDENT_ID]-web-02`. If not, follow this [tutorial](https://intranet.hbtn.io/rltoken/Tb9qeqRrtrO_b2uFpet9rw "tutorial").
*   For your answer file, write a Bash script that configures a new Ubuntu machine to respect above requirements

Example:

    sylvain@ubuntu$ curl -Is 54.210.47.110
    HTTP/1.1 200 OK
    Server: nginx/1.4.6 (Ubuntu)
    Date: Mon, 27 Feb 2017 06:12:17 GMT
    Content-Type: text/html
    Content-Length: 30
    Last-Modified: Tue, 21 Feb 2017 07:21:32 GMT
    Connection: keep-alive
    ETag: "58abea7c-1e"
    X-Served-By: 03-web-01
    Accept-Ranges: bytes
    
    sylvain@ubuntu$ curl -Is 54.210.47.110
    HTTP/1.1 200 OK
    Server: nginx/1.4.6 (Ubuntu)
    Date: Mon, 27 Feb 2017 06:12:19 GMT
    Content-Type: text/html
    Content-Length: 612
    Last-Modified: Tue, 04 Mar 2014 11:46:45 GMT
    Connection: keep-alive
    ETag: "5315bd25-264"
    X-Served-By: 03-web-02
    Accept-Ranges: bytes
    
    sylvain@ubuntu$
    

**Repo:**

*   GitHub repository: `holberton-system_engineering-devops`
*   Directory: `0x0F-load_balancer`
*   File: [1-install_load_balancer]()

### 2\. Add a custom HTTP header with Puppet

Just as in task #0, we’d like you to automate the task of creating a custom HTTP header response, but with Puppet.

*   The name of the custom HTTP header must be `X-Served-By`
*   The value of the custom HTTP header must be the hostname of the server Nginx is running on
*   Write `2-puppet_custom_http_response_header.pp` so that it configures a brand new Ubuntu machine to the requirements asked in this task

**Repo:**

*   GitHub repository: `holberton-system_engineering-devops`
*   Directory: `0x0F-load_balancer`
*   File: [2-puppet_custom_http_response_header.pp]()

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
