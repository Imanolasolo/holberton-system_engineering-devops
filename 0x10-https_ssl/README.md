0x10. HTTPS SSL
===============

In this project, I learned about the importance of HTTPS and how it works. I configured my HolbertonBnB web servers with certbot certificate and HAproxy SSL termination.

![Logo](https://www.howtogeek.com/wp-content/uploads/2021/05/laptop-with-terminal-big.png?height=200p&trim=2,2,2,50)

Concepts
--------

_For this project, students are expected to look at these concepts:_

*   [DNS](https://intranet.hbtn.io/concepts/12)
*   [Web stack debugging](https://intranet.hbtn.io/concepts/68)

Background Context
------------------

### What happens when you don’t secure your website traffic?

![](https://s3.amazonaws.com/intranet-projects-files/holbertonschool-sysadmin_devops/276/xCmOCgw.gif)

Resources
---------

**Read or watch**:

*   [What is HTTPS?](https://intranet.hbtn.io/rltoken/pawxG_0c1o86psexBOikIw "What is HTTPS?")
*   [What are the 2 main elements that SSL is providing](https://intranet.hbtn.io/rltoken/jXCB9Hn-ALcP78kPMHtnSA "What are the 2 main elements that SSL is providing")
*   [HAProxy SSL termination on Ubuntu16.04](https://intranet.hbtn.io/rltoken/UkbvWfKF6ZAY_CUvlM32lA "HAProxy SSL termination on Ubuntu16.04")
*   [SSL termination](https://intranet.hbtn.io/rltoken/VFq2MQ9qHXw2Nb11tnWF6Q "SSL termination")
*   [Bash function](https://intranet.hbtn.io/rltoken/16bxrQvaOSIywA_fHEdsiA "Bash function")

**man or help**:

*   `awk`
*   `dig`

Learning Objectives
-------------------

At the end of this project, you are expected to be able to [explain to anyone](https://intranet.hbtn.io/rltoken/DiMDOA6KHirT2gz-fjNEiA "explain to anyone"), **without the help of Google**:

### General

*   What is HTTPS SSL 2 main roles
*   What is the purpose encrypting traffic
*   What SSL termination means

Dependences
-----------

### 0\. World wide web

Configure your domain zone so that the subdomain `www` points to your load-balancer IP (`lb-01`). Let’s also add other subdomains to make our life easier, and write a Bash script that will display information about subdomains.

Requirements:

*   Add the subdomain `www` to your domain, point it to your `lb-01` IP (your domain name might be configured with default subdomains, feel free to remove them)
*   Add the subdomain `lb-01` to your domain, point it to your `lb-01` IP
*   Add the subdomain `web-01` to your domain, point it to your `web-01` IP
*   Add the subdomain `web-02` to your domain, point it to your `web-02` IP
*   Your Bash script must accept 2 arguments:
    1.  `domain`:
        *   type: string
        *   what: domain name to audit
        *   mandatory: yes
    2.  `subdomain`:
        *   type: string
        *   what: specific subdomain to audit
        *   mandatory: no
*   Output: `The subdomain [SUB_DOMAIN] is a [RECORD_TYPE] record and points to [DESTINATION]`
*   When only the parameter `domain` is provided, display information for its subdomains `www`, `lb-01`, `web-01` and `web-02` \- in this specific order
*   When passing `domain` and `subdomain` parameters, display information for the specified subdomain
*   Ignore `shellcheck` case `SC2086`
*   Must use:
    *   `awk`
    *   at least one Bash function
*   You do not need to handle edge cases such as:
    *   Empty parameters
    *   Nonexistent domain names
    *   Nonexistent subdomains

Example:

    sylvain@ubuntu$ dig www.holberton.online | grep -A1 'ANSWER SECTION:'
    ;; ANSWER SECTION:
    www.holberton.online.   87  IN  A   54.210.47.110
    sylvain@ubuntu$ dig lb-01.holberton.online | grep -A1 'ANSWER SECTION:'
    ;; ANSWER SECTION:
    lb-01.holberton.online. 101 IN  A   54.210.47.110
    sylvain@ubuntu$ dig web-01.holberton.online | grep -A1 'ANSWER SECTION:'
    ;; ANSWER SECTION:
    web-01.holberton.online. 212    IN  A   34.198.248.145
    sylvain@ubuntu$ dig web-02.holberton.online | grep -A1 'ANSWER SECTION:'
    ;; ANSWER SECTION:
    web-02.holberton.online. 298    IN  A   54.89.38.100
    sylvain@ubuntu$
    sylvain@ubuntu$
    sylvain@ubuntu$ ./0-world_wide_web holberton.online
    The subdomain www is a A record and points to 54.210.47.110
    The subdomain lb-01 is a A record and points to 54.210.47.110
    The subdomain web-01 is a A record and points to 34.198.248.145
    The subdomain web-02 is a A record and points to 54.89.38.100
    sylvain@ubuntu$
    sylvain@ubuntu$ ./0-world_wide_web holberton.online web-02
    The subdomain web-02 is a A record and points to 54.89.38.100
    sylvain@ubuntu$
    

**Repo:**

*   GitHub repository: `holberton-system_engineering-devops`
*   Directory: `0x10-https_ssl`
*   File: [0-world_wide_web]()

### 1\. HAproxy SSL termination

“Terminating SSL on HAproxy” means that HAproxy is configured to handle encrypted traffic, unencrypt it and pass it on to its destination.

Create a certificate using `certbot` and configure `HAproxy` to accept encrypted traffic for your subdomain `www.`.

Requirements:

*   HAproxy must be listening on port TCP 443
*   HAproxy must be accepting SSL traffic
*   HAproxy must serve encrypted traffic that will return the `/` of your web server
*   When querying the root of your domain name, the page returned must contain `Holberton School`
*   Share your HAproxy config as an answer file (`/etc/haproxy/haproxy.cfg`)

The file `1-haproxy_ssl_termination` must be your HAproxy configuration file

Make sure to install HAproxy 1.5 or higher, [SSL termination](https://intranet.hbtn.io/rltoken/VFq2MQ9qHXw2Nb11tnWF6Q "SSL termination") is not available before v1.5.

Example:

    sylvain@ubuntu$ curl -sI https://www.holberton.online
    HTTP/1.1 200 OK
    Server: nginx/1.4.6 (Ubuntu)
    Date: Tue, 28 Feb 2017 01:52:04 GMT
    Content-Type: text/html
    Content-Length: 30
    Last-Modified: Tue, 21 Feb 2017 07:21:32 GMT
    ETag: "58abea7c-1e"
    X-Served-By: 03-web-01
    Accept-Ranges: bytes
    sylvain@ubuntu$
    sylvain@ubuntu$ curl https://www.holberton.online
    Holberton School for the win!
    sylvain@ubuntu$
    

**Repo:**

*   GitHub repository: `holberton-system_engineering-devops`
*   Directory: `0x10-https_ssl`
*   File: [1-haproxy_ssl_termination]()

### 2\. No loophole in your website traffic

A good habit is to enforce HTTPS traffic so that no unencrypted traffic is possible. Configure HAproxy to automatically redirect HTTP traffic to HTTPS.

Requirements:

*   This should be transparent to the user
*   HAproxy should return a [301](https://intranet.hbtn.io/rltoken/Oe04HFEd_PTgWAvWBTr1rA "301")
*   HAproxy should redirect HTTP traffic to HTTPS
*   Share your HAproxy config as an answer file (`/etc/haproxy/haproxy.cfg`)

The file `100-redirect_http_to_https` must be your HAproxy configuration file

Example:

    sylvain@ubuntu$ curl -sIL http://www.holberton.online
    HTTP/1.1 301 Moved Permanently
    Content-length: 0
    Location: https://www.holberton.online/
    Connection: close
    
    HTTP/1.1 200 OK
    Server: nginx/1.4.6 (Ubuntu)
    Date: Tue, 28 Feb 2017 02:19:18 GMT
    Content-Type: text/html
    Content-Length: 30
    Last-Modified: Tue, 21 Feb 2017 07:21:32 GMT
    ETag: "58abea7c-1e"
    X-Served-By: 03-web-01
    Accept-Ranges: bytes
    
    sylvain@ubuntu$
    

**Repo:**

*   GitHub repository: `holberton-system_engineering-devops`
*   Directory: `0x10-https_ssl`
*   File: [100-redirect_http_to_https]()

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
