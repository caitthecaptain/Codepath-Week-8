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
- [x] **Summary:**
- With this vulnerability, a user must simply be logged in and on the "Find a Salesperson" page.
- Click on any user, and you will see that each one has a number associated with them.
- Enter the SQLi [ ' OR SLEEP(5)=0--' ] after the .php session id instead of the number of the salesperson. 
- You can change the 5 to however many seconds you would like for it to take the page to refresh.
- [x] **GIF**:
![](https://github.com/caitthecaptain/Codepath-Week-8/blob/master/sqlinjection.gif)


**Vulnerability #2: Session Hijacking/ Fixation**
- [x] **Summary:**
- With this vulnerability, a user needs to be logged in on one browser and logged out on another, with 2 different session IDs.
- Copy the Session ID from the logged in browser into the browser of the non-logged in one.
- Click "Log in."
- You are in!
- [x] **GIF**:
![](https://github.com/caitthecaptain/Codepath-Week-8/blob/master/sessionhijack.gif)



## Green

**Vulnerability #1: Cross-Site Scripting (XSS)**
- [x] **Summary:**
- With this vulnerability, any user can easily create an XSS using: <script>alert("write whatever you want")</script> , because the site does not properly check for <script> tags.
- Log in on one browser, go to the "contact us" page, enter a name/email/XSS. Submit.
- Go to the other browser, click "log in," then click on "Feedback." The XSS will execute.
- [x] **GIF**:
![](https://github.com/caitthecaptain/Codepath-Week-8/blob/master/xss.gif)

**Vulnerability #2: Username Enumeration**
- [x] **Summary:**
- With this vulnerability, anyone can easily see whether or not a username exists.
- If the username does not exist, a message will appear that says, "Log in was Unsuccessful."
- However, if the username **DOES** exist, a message will appear that says, "**Log in was Unsuccessful."** in bolded letters.
- [x] **GIF**:
![](https://github.com/caitthecaptain/Codepath-Week-8/blob/master/userenumeration.gif)



## Red

**Vulnerability #1: Cross-Site Request Forgery (CSRF)**
- [x] **Summary:**
- With this vulnerability, CSRF attacks against an admin are possible. 
- Log in to the site as an admin, and open an HTML file that you create.
- The CSRF attack will change the name of a person in the "Users" tab.
- [x] **GIF**:
![](https://github.com/caitthecaptain/Codepath-Week-8/blob/master/csrf.gif)
<p><img src="https://github.com/caitthecaptain/Codepath-Week-8/blob/master/csrf.html" alt="->View my HTML file!<-"></p>



**Vulnerability #2: Insecure Direct Object Reference (IDOR)**
- [x] **Summary:**
- With this vulnerability, there are two salesperson accounts that are not visible to the public. 
- By logging in, we see that they have the ID numbers of 10 and 11.
- Go to the website (you do not have to log in) and click on "Find a Salesperson."
- Click on any of them, and replace the id # with 10 or 11 to see ones that you should not!
- [x] **GIF**:
![](https://github.com/caitthecaptain/Codepath-Week-8/blob/master/idor.gif)




## Notes

- The Codepath hints that were given were INCREDIBLY helpful.
- I found this entire exercise to be very helpful in increasing my hacking skills!

## Resources
- GIFs created with [LiceCap](http://www.cockos.com/licecap/)


