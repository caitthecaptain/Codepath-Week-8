# Week 8 - Pentesting Live Targets

Time spent: **7** hours spent in total

> Objective: Identify vulnerabilities in three different versions of the Globitek website: blue, green, and red.

The six possible exploits are:
* Username Enumeration
* Insecure Direct Object Reference (IDOR)
* SQL Injection (SQLi)
* Cross-Site Scripting (XSS)
* Cross-Site Request Forgery (CSRF)
* Session Hijacking/Fixation

Each version of the site has been given two of the six vulnerabilities. (In other words, all six of the exploits should be assignable to one of the sites.)

## Blue

**Vulnerability #1: SQL Injection (SQLi)**
- With this vulnerability, a user must simply be logged in and on the "Find a Salesperson" page.
- Click on any user, and you will see that each one has a number associated with them.
- Enter the SQLi [ ' OR SLEEP(5)=0--' ] after the .php session id instead of the number of the salesperson. 
- You can change the 5 to however many seconds you would like for it to take the page to refresh.
![](https://github.com/caitthecaptain/Codepath-Week-8/blob/master/sqlinjection.gif)



**Vulnerability #2: Session Hijacking/ Fixation**
- With this vulnerabiliy, a user needs to be logged in on one browser and logged out on another, with 2 different session IDs.
- Copy the Session ID from the logged in browser into the browser of the non-logged in one.
- Click "Log in."
- You are in!
![](https://github.com/caitthecaptain/Codepath-Week-8/blob/master/sessionhijack.gif)



## Green

**Vulnerability #1: Cross-Site Scripting (XSS)**
- With this vulnerability, any user can easily create an XSS using: <script>alert("write whatever you want")</script> , because the site does not properly check for <script> tags.
- Log in on one browser, go to the "contact us" page, enter a name/email/XSS. Submit.
- Go to the other browser, click "log in," then click on "Feedback." The XSS will execute.
![](https://github.com/caitthecaptain/Codepath-Week-8/blob/master/xss.gif)

**Vulnerability #2: Username Enumeration**
- 
![]()



## Red

**Vulnerability #1: Cross-Site Request Forgery (CSRF)**- 
- 
![]()



**Vulnerability #2: Insecure Direct Object Reference (IDOR)**
- 
![]()




## Notes

Describe any challenges encountered while doing the work
