---
title: "Week 5 Reflection"
date: 2020-02-23T02:01:58+05:30
---

***
***
#### Introduction
***
***

This is the 5th week of Cyber Security Summer Studio and since we have some experience with hacking virtual machines, we were challenged to `Hackthebox` machines. It has been much more difficult to seek more help online since you are not allowed to post writeups/solutions to current boxes unless they are officially retired online. Therefore, the only way I could seek out help if I was ever stuck (was stuck a lot actually) was either from my experience in approaching boxes learnt previously from the `tryhackme` boxes that I attempted last week, and by asking around fellow students and tutors. This week was definitely an ***eye opener*** for me as it can be really difficult to attempt a box without a step by step guide, especially if you are attempting it for the first time, and also how relevant the vulnerabilities that these boxes present are to the real world today.

Furthermore, I would have hoped I had time to fix up my `Biohazard` box from `tryhackme` with one of my fellow students (Tyrone), however this week was mainly focused on further improving upon my penetration testing skills on a more ***well-known*** platform called `Hackthebox` instead. Consequently, at the end of the week, with the guidance of fellow students and teachers, I was able to retrieve the flag from users.txt and escalate my privileges to become a root user! This has been a huge accomplishment for me, since without a rough guide, I still am quite confused on what to do and remember what the general approach to attempt a box is. Luckily, the teaching team has constantly reminded me that whenever it comes to attempting boxes, you will always have to undergo constant research and trial and error, and should always remember the **3 E's:**
- `Enumerating`
- `Exploiting`
- `Escalation`

***
***
`Hackthebox` **deliverable** due for this week can be found under [logs](https://teechan.me/logs/).

**|OR|**

You can manually visit this **link** here:
1. [HACKTHEBOX:Openadmin](https://www.teechan.me/logs/hackthebox-openadmin/)

***
***

#### Week 5: Pros & Cons
###### To-do list:
- Get the invite code for `Hackthebox` to signup for an account
- Pick one of the easy boxes recommended by the teaching team
- Complete writeup for the `Openadmin` box and make sure it is password protected and not released to the public
- Prepare for the Thursday Deloitte demonstration by downloading the VM before they arrive to show self-alacrity
- Try and complete [Biohazard](https://tryhackme.com/room/biohazard) on `tryhackme` if possible
- Continuing adding screenshots of my chat logs and team collaboration to further show proof of my understanding of the learning outcomes

***
***
###### Pros:
- I was able to retrieve the flag from users.txt in the `openadmin` box
- I was also able to escalate my privileges to become a `root` user!
- Logged my `Hackthebox` achievement [here](https://www.teechan.me/logs/hackthebox-openadmin/)
- Took some brief notes of Deloitte's demonstration on Thursday, which can be viewed [here](https://drive.google.com/open?id=1kucfAyXD3nf-ZXIayyRGFdoLF-EBJQbY)
- Engaged with other students and tutors for help on `openadmin` and helped others accordingly if I could
- Continuously learnt different Pen-testing + Linux skills throughout the challenges and write-ups which was a really enjoyable experience
- Managed to have a little more self-control and worked on my procrastinating by adopting the "Work on this for just 5 minutes" mindset

***
***

###### Cons:
- Although my procrastinating seems more controllable now, I still struggle with it sometimes when there are not as many tasks or If i spend too long trying to plan for something
- Only attempted one box from `Hackthebox`, as I thought it would take up the whole week to complete just one box
- Had a final presentation and interview for the careers subject, which was more of a priority since this was the last week for it
- I still could not find the time to complete the `Biohazard` box that me and another fellow student (Tyrone) said we would complete by this sprint, since we had other important priorities this week, and was told to focus on a `Hackthebox` box for this week's deliverable instead. `(But don't worry, It will be completed by next week!)` `(I say that but...)`
***
***
#### Weekly Recap
***
***
###### Monday (17/02):
***
***
This week, from what I saw, the teaching team have realised the fact that certain students usually arrive a little late and some students (me included) still have their last week of CMITP left and thus, to accommodate for this, they have moved the stand up meeting to after lunch, so that every student benefits from the meeting and no one missed out. I really enjoy this change as I usually miss the opportunity to communicate with the rest of the class on Mondays, as I have the careers class (CMITP) right before summer studio.  

Today, we were introduced to the `Hackthebox` platform, and how it is much more of a challenge than `tryhackme` or even `vulnhub` boxes. We were first tasked with finding the invite code to `Hackthebox`in order to create an account. This seemed overwhelming at first because there were no clear indicators of where to look at first. Thus, with the help of the fellow students and the teaching team I was able to push through and manage to take a step in the right direction. Here are few screenshots below to demonstrate the 2 main applications that I have learnt to use to decode the invite code, which are `Postman` from the Chrome Web store (1st and 2nd Image) and `CyberChef` (3rd Image) for the ultimate decoding tool.

![Screenshot4.png](/images/inv1.png)
![Screenshot4.png](/images/inv2.png)
![Screenshot4.png](/images/inv3.png)

Furthermore, what I have learnt from today was that the constant research + countless hours trying to trial and error potential solutions to see what could be exploited is very essential in the learning process. `Google` was honestly to ***go-to*** place for learning new concepts and techniques. It can also be extremely satisfying to find out that the technique/command you are trying to find is already demonstrated through a similar box, thus, revealing how it can be similarly used. However, although some commands are extremely similar, it sometimes might not be the case. This is because you might require different privilege rights or sometimes you might even end of mistyping commands and passwords, and quickly assume that you have the wrong approach when you were correct all this time! `(grr)`

***
***
###### Tuesday & Wednesday (18/02 - 19/02):
***
***
I decided to combine both Tuesday's and Wednesday's recap since I did not accomplish much on Tuesday as I had a final 'marked' interview for my careers subject.

Throughout the rest of the day we decided to take it easy a little and watched some pen-testing tips videos. [Here](https://www.youtube.com/watch?v=OrjcnFTTDj8was) was a really good one we found.

![Screenshot4.png](/images/pentesttips.png)

***
During Wednesday's class, not much was accomplished as the AU servers constantly went down and were having request issues. The constant going back and forth of resetting the box and not having access to the box really frustrated me. However, I did not waste anytime as I Googled some exploits while I was waiting for the server. I ended up learning about how there was an exploit for the `openadmin` version on `Exploit-DB`, found out I took so many unnecessary steps to get to a directory because I did not what the correct command was and many more.

Later that day, to counter this waiting issue, I ended up deciding to find an alternative server (US) to switch to, and this worked seamlessly :)

***
***
###### Thursday (20/02):
We were first introduced to two guest speakers (Pieter Westein and Nathan Jones) from Deloitte, where they talked about what Penetration Testing is and how important Information Security to businesses they are. They also touched upon topics that I was not too sure of or did not have much clarity on. This included the notion that red team offensive operations are crucial for a client company in order to target a specific exploit, and also the idea that simple 'plug-in' IoT devices can be used to access a company's Intranet and have access to their local files is very dangerous. These brief notes can be viewed [here](https://drive.google.com/open?id=1kucfAyXD3nf-ZXIayyRGFdoLF-EBJQbY). Consequently, through one of our fellow students asking the speakers regarding the ***"human element"*** of threat assessment, it prompted me to do more research into a new **problem statement**.
***
`P: How costly are Cyber risks from the human element and how will they affect businesses?`
***
 [Here's](https://threatpost.com/assessing-the-human-element-in-cyber-risk-analysis/137644/) one that I found to be extremely interesting that discusses about this topic. Although the guest speakers have already briefly answered the question in class, I still feel that it was necessary to do some external research at home. Hence, here's a proposed solution I came up with, influenced by the article I linked above and Deloitte's answer:
***
`A:` According to [ThreatPost](https://threatpost.com/assessing-the-human-element-in-cyber-risk-analysis/137644/): We need to acquire a deep understanding of our employees in a business in order to better understand how human elements are crucial to cyber risk. This is because we need to ask ourselves: `"what’s the likelihood that the employee will fall for a phishing email or accidentally forward a spreadsheet with customer sensitive information again?` Thus, by analysing the probability how this action will cause a `data breach or system disruption` and what is the potential financial loss, we can actively train employees to be more aware of social engineering attacks and how to spot a potential attacker.
***
Later that day, we were told to attempt Deloitte's own box. It presented a variety of different medium and approach than what we were used to. Since it has a Git repository, we were scrambling away at what ways we could copy/clone that directory locally so we can access it. The box at first was immediately intimidating as I was not used to this format. To be fair I was just worried that everyone else was using `Netdiscover` and I starting off with `Nmap` which did concern me a little initially. However, with the guidance from the guest speakers and fellow students, we later decided a plan of action from the given hint that would slowly eat into our time. Despite the fact that not much progress was made due to time constraints, I still learnt a lot in terms of how to effectively 'search' for exploits and how to execute them and also how to plan a better course of action if I face a similar intensive task in the future.

![Screenshot4.png](/images/delphotos.jpeg)

Through our weekly Thursday scrum meeting, I have learnt that many of us still share common problems with differing strengths. One common problem that I found that was prevalent in all of us was the fact that we all loathed the idea of `enumerating` and how tiresome it can be to do in-depth research into a single topic that we did not understand. However, we all shared a common perseverance mindset, even when we struggled, despite all the hints that we have been given.



Furthermore, through my 1 on 1 session with the teaching team, I made it clear that I was struggling to find a clear and concise approach to tackle boxes and asked them what I should do. They responded along the lines of: "To not panic when you are struggling to find the 'right' command for something as its all part of the trial and error + learning process." `Enumerate Enumerate Enumerate!`



***
***
###### Friday + Weekend (21/02 - 23/02):
To keep it short and simple, for the rest of my weekend (+ Friday), I decided to completely focus on completing the `Hackthebox` deliverable, start a write-up for it as I am doing the task and polishing up the reflection whenever possible. Once again, although me and Tyrone (fellow student) did not completely finish our box `Biohazard` for this week due to the fact that our `Hackthebox` deliverable was more a priority, we still managed to work well together again to work on our `openadmin` box. Nevertheless, with the help from the teaching team and fellow students, I still communicated with them through MS Teams, Messenger and Discord to accomplish some tasks collaboratively.

![Screenshot4.png](/images/jasoncold.png)
![Screenshot4.png](/images/jasonhot.png)
![Screenshot4.png](/images/larry1.png)

Furthermore, I manage to retrieve the users.txt flag and gain root access which is definitely a huge accomplishment for me but I completely forgot about the incomplete box that I mentioned I was ***"going to"*** complete by this sprint. Moreover, I also spent the rest of the weekend finishing up the write-ups, polishing reflection logs and spent some time preparing some sub-topics to talk about for our final studio presentation. I did research based on the relevance of our chosen box `Vulnversity` to the Information security industry, the sub-topics that we need to allocate to each team member and who will be in charge of the exploit demonstration.

![Screenshot4.png](/images/hacktheboxprofile.png)

***
***
#### Conclusion `TLDR`
***
***
To summarise, this week was not as chaotic as last week but definitely more stressful. This was because we were immediately challenged with a box from `Hackthebox`. As a result, I was constantly researching into new technical tools, whilst constantly reminding myself on how to utilise previously learnt tools. Nevertheless, this tedious week was surprisingly an 'eye-opener' for me as I have discovered that I have learnt so many new techniques and approaches, compared to over the past 4 weeks, and have been constantly keen to learn more about cyber security.

Furthermore, from my knowledge gained from completing boxes from other platforms, it has allowed me to complete the `openadmin`box from `Hackthebox`, which heightened my understanding on many different techniques to conduct Pen-testing and each with their specific uses such as: `finding sub-directories of /root`, `Curl`, `Netstat`, `CyberChef` and `GTFObins.`
***
***

Next week I would like to achieve:
- Continue to be more disciplined and keep updating reflection whenever possible
- Conduct more research into more technical Cyber security content and re-evaluate my problem statement
- Be more consistent in time management techniques
- Actually finish the `Biohazard` box by next sprint this time, with assistance if needed
- Try to attempt to stay consistent in meeting subject learning outcomes

***
***
