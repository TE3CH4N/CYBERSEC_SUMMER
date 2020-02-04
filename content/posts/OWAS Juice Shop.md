---
title: "OWASP Juice Shop logs"
date: 2020-01-30T02:01:58+05:30
---

### OWASP Juice shop

##### This page is still under maintenance!



1. Went on hacksplaining and relearnt how to execute SQL commands to force login
2. Check if email and password to be true in database (TRUE & TRUE) (1 = 1)

![OWAS%20Juice%20Shop/Untitled.png](/images/OWASP5.png)

Object object just shows error handling —> shows a successful sql injection attempt

![OWAS%20Juice%20Shop/Untitled%201.png](/images/OWASP1.png)

Now that I've seen my scoreboard, I can pick the next task to accomplish

![OWAS%20Juice%20Shop/Untitled%202.png](/images/OWASP2.png)

Accidentally did the privacy policy task as I logged in

I chose to pick Confidential Document task:

- "Sensitive data exposure occurs when an application, company, or other entity inadvertently exposes personal data. Sensitive data exposure differs from a data breach, in which an attacker accesses and steals information."

List of steps I took:

- Read the guide on hacksplaining
-

Next task was the Missing Encoding task:

1. Go to Photo Wall
2. Right Click + Inspect Element
3. Ctrl + F to search by filter and find the image link with hashtags
4. Replaced all # in the image link to %23 (html code for hastag)
5. Clicked outside the elements box and the page refreshed, allowing the image to be recognisd and voila!

![OWAS%20Juice%20Shop/Untitled%203.png](/images/OWASP3.png)

2.  By replacing it with %23, html code can recognise the image link

![OWAS%20Juice%20Shop/Untitled%204.png](/images/OWASP4.png)

##### Next Task: Accessing a Confidential Document
