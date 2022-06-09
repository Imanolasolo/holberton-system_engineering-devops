0x18. Webstack monitoring
=========================

This project invovled setting up Sumo Logic accounts to monitor server traffic on my HolbertonBnB web-01 server.

### Concepts

_For this project, we expect you to look at these concepts:_

*   [Monitoring](https://intranet.hbtn.io/concepts/13)
*   [Server](https://intranet.hbtn.io/concepts/67)

![](https://s3.amazonaws.com/intranet-projects-files/holbertonschool-sysadmin_devops/281/hb3pAsO.png)

Background Context
------------------

“You cannot fix or improve what you cannot measure” is a famous saying in the Tech industry. In the age of the data-ism, monitoring how our Software systems are doing is an important thing. In this project, we will implement one of many tools to measure what is going on our servers.

Web stack monitoring can be broken down into 2 categories:

*   Application monitoring: getting data about your running software and making sure it is behaving as expected
*   Server monitoring: getting data about your virtual or physical server and making sure they are not overloaded (could be CPU, memory, disk or network overload)

Resources
---------

**Read or watch**:

*   [What is server monitoring](https://intranet.hbtn.io/rltoken/m8e7smqRz3k4PUBnv0zB7g "What is server monitoring")
*   [What is application monitoring](https://intranet.hbtn.io/rltoken/fGzCCVr7lwNEvarE8u1HRQ "What is application monitoring")
*   [System monitoring by Google](https://intranet.hbtn.io/rltoken/h6WV2iIVUCL-atjFIu6TZA "System monitoring by Google")
*   [Nginx logging and monitoring](https://intranet.hbtn.io/rltoken/ZUIlnid6NphRWIaGZ3MTZQ "Nginx logging and monitoring")

Learning Objectives
-------------------

At the end of this project, you are expected to be able to [explain to anyone](https://intranet.hbtn.io/rltoken/fg0tmIkt2x_pb-c2j_J4OQ "explain to anyone"), **without the help of Google**:

### General

*   Why is monitoring needed
*   What are the 2 main area of monitoring
*   What are access logs for a web server (such as Nginx)
*   What are error logs for a web server (such as Nginx)

Dependences
-----------

### 0\. Sign up for Datadog and install datadog-agent

For this task head to [https://www.datadoghq.com/](https://intranet.hbtn.io/rltoken/Uho9kxbX9KHCSYAQ-Zl1AQ "https://www.datadoghq.com/") and sign up for a free `Datadog` account. When signing up, you’ll have the option of selecting statistics from your current stack that `Datadog` can monitor for you. Once you have an account set up, follow the instructions given on the website to install the `Datadog` agent.

![](https://holbertonintranet.s3.amazonaws.com/uploads/medias/2019/6/6b0ea6345a6375437845.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIARDDGGGOU5BHMTQX4%2F20220606%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20220606T192953Z&X-Amz-Expires=86400&X-Amz-SignedHeaders=host&X-Amz-Signature=3d6e820f66f7b89451bd40c88e7aa4fb577661013bfc4f0ab0b1358dc77e6a1d)

*   Sign up for Datadog - **Please make sure you are using the US website of Datagog (.com)**
*   Install `datadog-agent` on `web-01`
*   Create an `application key`
*   Copy-paste in your Intranet user profile ([here](https://intranet.hbtn.io/rltoken/2D6j3Y6G9c8o_t278-Cu_w "here")) your DataDog `API key` and your DataDog `application key`.
*   Your server `web-01` should be visible in Datadog under the host name `XX-web-01`
    *   You can validate it by using this [API](https://intranet.hbtn.io/rltoken/CyrSkrD0zPWXK4YBRRbTvw "API")
    *   If needed, you will need to update the hostname of your server

**Repo:**

*   GitHub repository: `holberton-system_engineering-devops`
*   Directory: `0x18-webstack_monitoring`

### 1\. Monitor some metrics

Among the litany of data your monitoring service can report to you are system metrics. You can use these metrics to determine statistics such as reads/writes per second, which can help your company determine if/how they should scale. Set up some `monitors` within the `Datadog` dashboard to monitor and alert you of a few. You can read about the various system metrics that you can monitor here: [System Check](https://intranet.hbtn.io/rltoken/naY47nur2yPJNw8tdACnzQ "System Check").

![](https://holbertonintranet.s3.amazonaws.com/uploads/medias/2019/6/6a4551974aadc181e97a.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIARDDGGGOU5BHMTQX4%2F20220606%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20220606T192953Z&X-Amz-Expires=86400&X-Amz-SignedHeaders=host&X-Amz-Signature=088bb55242166139bcba5dd9562a219f181046164e8821b6f05db2aab2b14def)

*   Set up a monitor that checks the number of read requests issued to the device per second.
*   Set up a monitor that checks the number of write requests issued to the device per second.

**Repo:**

*   GitHub repository: `holberton-system_engineering-devops`
*   Directory: `0x18-webstack_monitoring`

### 2\. Create a dashboard

mandatory

Now create a dashboard with different metrics displayed in order to get a few different visualizations.

*   Create a new `dashboard`
*   Add at least 4 `widgets` to your dashboard. They can be of any type and monitor whatever you’d like
*   Create the answer file `2-setup_datadog` which has the `dashboard_id` on the first line. **Note**: in order to get the id of your dashboard, you may need to use [Datadog’s API](https://intranet.hbtn.io/rltoken/VrzQP39UUFMmAKZx0IZLuw "Datadog's API")

**Repo:**

*   GitHub repository: `holberton-system_engineering-devops`
*   Directory: `0x18-webstack_monitoring`
*   [2-setup_datadog](https://github.com/Imanolasolo/holberton-system_engineering-devops/blob/main/0x18-webstack_monitoring/2-setup_datadog)

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