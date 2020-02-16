---
title: "Week 4 Reflection"
date: 2020-02-16T02:01:58+05:30
---

***
***
#### Introduction
***
***
This is the 4th week of Cyber Security Summer Studio and we have been introduced to virtual machine hacking challenges called boot2roots. Last week I felt a little disappointed in myself that I had not put that much time in my weekly goals since I had a huge deliverable for my other careers management class. Thus, with that motivation in mind, I convinced myself to power through this week. At first, it seemed rather intimidating and time consuming, however, Jason and the rest of the teaching team made it easy to learn through a quick demo of `Wakanda box,` and also discussed the main objectives of basic penetration testing.

Having learnt the basics of Pen testing, we were then set the deliverable to attempt as many hacking challenges as possible, even if they were failed attempts (some were really difficult!). I found this as an excellent opportunity to test my pre-existing Linux skills and learn new Pen testing skills. I was first introduced to Basic Pen testing 1 by Max. This was rather straightforward, however I did not have a sense of direction of where I wanted to head, so I decided to look up guides, walkthroughs and even asking other fellow students for help because I was confused with what my task at hand was. Luckily, Hayden (fellow student) had some minor experience with basic Pen testing, thus, with his guidance, I was able to complete Basic Pentesting 1 box from [Vulnhub](https://www.vulnhub.com/entry/basic-pentesting-1,216/). However, I did not feel that a major sense of accomplishment from completing this box, as it was mainly through the help of others that I was able to get through this task.

Thus, I navigated over to [tryhackme](https://tryhackme.com/) and began attempting a beginner box called [Vulnerversity](https://tryhackme.com/room/vulnversity) where I could learn the basic skills of Pen-testing through a step by step task completion process. Consequently, I learnt a lot of basic skills from this virtual box and would recommend it to anyone who is new to Pen-testing or just wants to polish up their basic skills in order to move on to more complex ones.

***
***

`boot2root` **deliverable** due for this week can be found under [logs](https://teechan.me/logs/).

**|OR|**

You can manually visit these **links** here:
1. [Basic Pentesting 1](www.teechan.me/logs/basic1/)
2. [Vulnversity](www.teechan.me/logs/tryhackme-vulnerversity/)
3. [Biohazard](www.teechan.me/logs/tryhackme-biohazard/)

***
***

#### Week 4: Pros & Cons
**To-do List:**
- Try Basic Pentesting 1
- Learn more skills on [tryhackme](https://tryhackme.com/)
- Complete writeup for Basic Pentesting 1 from Vulnhub
- Attempt and finish [Vulnerversity](https://tryhackme.com/room/vulnversity) on tryhackme
- Attempt [Biohazard](https://tryhackme.com/room/biohazard) on tryhackme
- Add some screenshots of my chat logs to show collaboration efforts between team members, especially in Reflection 3, since my feedback from last week was to demonstrate more collaboration work

***
***
###### Pros:
- Logged my`boot2root`writeups [here](https://teechan.me/logs/)
- Recorded some notes regarding Jason's demo of the `Wakanda Box`, which can be viewed [here](https://drive.google.com/file/d/1IsHY-CPG_5-xzf4QWlV5iBUOZHxNufIC/view?usp=sharing)
- Engaged with other students for help on certain tryhackme challenges/tasks and helped others accordingly if I could
- Learnt a lot of different Pen-testing skills and Linux skills throughout the challenges and writeups which was a really enjoyable experience
- Asked what I wanted during the 1 on 1 consultation session regarding my boot2root writeup layout/format and just some general questions on my progress so far to keep myself motivated (`Is this what a Dopamine high feels like?`)

***
###### Cons:
- I still struggled a little on procrastinating on polishing up links to my notes + write-up logs, as I had to focus on another important deliverable up until the weekend again
- Attempted CTF challenges, but not as much as I wanted to, due to another presentation preparation for the careers subject I mentioned in week 1 was more of a priority
- Could not complete the `Biohazard` box that me and another fellow student (Tyrone) we chose, since we were stuck on intermediate encoding conversions and we didn't want to just follow a guided walkthrough throughout the whole box. This is because we wanted to try it out for ourselves before we DO decide to follow the guide as a last resort method. `(To be completed by next week!!)`

***
***
#### Weekly Recap
***
***

###### Monday (03/02):
***
***
I missed the initial scrum meeting as I had to attend the careers management class then rush over to the summer studio class. However, my classmates soon filled me in what our deliverable was for this week and explained how we are attempting to `boot2root` and start learning penetration testing skills.

I was having troubles with my Kali Machine as file transfers were slow (slow Toshiba EXT hard drive = slow transfer speeds), which often resulted in my Virtual Machines (VMs) crashing as there were memory allocation issues. However, I fixed this issue by asking the teaching team for permission to borrow a Samsung T5 SSD, which would be used to store my VMs instead.

After doing some in-depth research at home about penetration testing, Kali Linux and the different tools that you can use I have found a **potential industry problem:**
***
`P: Penetration Testing is not comprehensive enough and can do real damage`
***
Thus, I decide to take a break from learning about boot2roots and decided to read a few articles regarding this issue. [Here's](https://www.cybersecuritymastersdegree.org/2018/01/is-penetration-testing-a-complete-waste-of-time/) one that I found to be extremely interesting that discusses about this topic. Despite the fact that I did not bring up this industry problem to tutors, I still felt that it was necessary to write about as it would understand the pros of penetration testing and what could be the severe outcomes if performed properly. Here's a propsed solution I came up with, along with the guide of the article I linked above:
***
**A**: According to [CSMD](https://www.cybersecuritymastersdegree.org/2018/01/is-penetration-testing-a-complete-waste-of-time/): `"Penetration testing, of course, is working off just that catalog of ideas, testing only vulnerabilities that are, by definition, enumerated somewhere."` Despite the fact that the general approach to tackle common vulnerabilities is easy enough to figure out, a similar attack performed at a later date `"might not work a second time, or against another set of employees."` Thus, meaning that the nature of attacks will definitely change in most businesses and `"valid tests are only valid for a short period of time"`.

Nevertheless, penetration testing is still extremely useful in detecting exploits in certain businesses when used correctly and when the pen-tester is fully aware of its capabilities. Therefore, it is still definitely relevant for companies, especially ones that hold highly sensitive data to hire pen-testers or pen-tester companies so they can actively test, continuously assess vulnerabilities (scanning) and continuously monitor their system (IDS, SEM) in order to successfully patch and address these issues accordingly and immediately before the next planned attack.

***
***
###### Tuesday (04/02):
***
***
Me and Hayden had met up again to focus on completing a simple virtual box called `Basic Pen testing 1.` Today was primarily focused on getting `root` access to the directory, which was one of the first tasks that needed to be completed. Thus, under Hayden's guidance and many walkthroughs later I had managed to get this working. Furthermore, I immediately had another go at the box but this time, logging every step, dead-end and accomplishment on the `Notion` note-taking app, as I work through the box.

![Screenshot4.png](/images/basic1.png)


At home, I decided to have a look at Yukari's (fellow student) recorded video of the in-class demonstration of the `Wakanda Box`, which can be viewed [here](https://www.youtube.com/playlist?list=PLI6vqVtN06dVeLYvbLAbYkayfiSeE7drR). Since I arrived late on Monday and was not aware of what happened during the demo, I decided to try and absorb the information that I have missed through watching Yukari's recorded video. Consequently, I learnt a lot more through the video demonstration over reading other online walkthroughs, so massive props to Yukari for recording the demonstration :)

![Screenshot4.png](/images/wakanda1.png)
***
***
###### Wednesday (05/02):
***
***
Today's focus was mainly on Vulnversity and getting used to Tryhackme's platform. I met up with fellow students and the teaching team today at our usual room for a drop-in session. I had several questions that I needed to ask regarding Vulnversity, and it turns out that I tend to skip lines when I read and did not remember to allow the `openvpn` service to run on my Kali Linux VM before attempting the task ***(please forgive me Jason <3)***. After fixing the annoying minor setback, I powered through learning how to effectively use `Nmap` and was quickly onto the next stages afterwards.

At home, I watched Max's video on how to setup `BurpSuite` (better late than never), to help me get a better understanding of how `BurpSuite` works and learnt Max's method on how to set it up, which turned out to be much more effective and useful than reading an online guide with too many technical knowledge assumptions. This can be viewed [here](/images/maxburp.mp4).

![Screenshot4.png](/images/burpsuite.png)

***
***
###### Thursday (06/02):
Through our weekly Thursday scrum meeting, I have learnt that many of us had common problems with different strengths. One common problem that I found that was prevalent in all of us was the fact that we all needed some sort of motivation to make it easier to ***"make a start"***. However, when we were introduced to a demonstration by Jason and the teaching team, or even a simple guided walkthrough helped out a lot. This is because when we were thrown into the deep end to simply ***"gain root access"*** we struggled a little, despite our strengths.

Furthermore, we continued working on our boxes for the rest of the day. I happened to check up on a Tyrone, who's also working on `Vulnversity` along with Anthony. Therefore I asked him whether or not he wants to work on a section of a `BurpSuite` task that we were both stuck on so we could help each other out (screenshot shown below). Additionally, I had another 1 on 1 session with Jason and Larry. Overall, they seem happy with my progress so far, however Jason still mentioned my logs and write-ups still need to be in-depth (showing `how` I get there instead of `what` I got). This is something that I definitely need to work on, especially when the final weeks are approaching fast.

![Screenshot4.png](/images/tyrone05.png)

***
***
###### Friday + Weekend (07/02 - 09/02):
I decided to focus on completing the `boot2root` deliverable and polishing up the reflection, in hopes of getting it finished before Sunday. Not only is that so Jason and the rest of teaching team can give me early feedback, it also leaves me some time to work on another short presentation deliverable that is due on the following Monday for the careers subject (mentioned in week 1).

Although me and Tyrone (fellow student) did not completely finish our box `Biohazard` for this week due to certain obstacles which halted our progression, we are still very keen to complete by sometime next week after we have done some in-depth research about certain tools. This is because without in-depth research and without running certain questions by the teaching team, we cannot progress, as we would spend countless hours trying to figure out which appropriate techniques to use. Whereas in this case, if we have asked the tutors in the first place, especially about which sites are a 'good read' to discover more about different base encodings and ciphers, then a lot more progress would be made.

Nevertheless, we still communicated through Messenger and Discord to accomplish some tasks collaboratively with our port scanning knowledge gained from completing the `Vulnversity` box and through countless hours of going through trial and error of the top 10 encoding formats on [Cyberchef](https://gchq.github.io/CyberChef/).

![Screenshot4.png](/images/tyrone2.png)
![Screenshot4.png](/images/tyrone1.png)

Furthermore, we accomplished as much as we can without receiving too much help from a completed guide for now but will definitely complete it by next week! Moreover, I spent the rest of the weekend finishing up the write-ups, polishing reflection logs with added communication screenshots based on the given feedback from Jason this week, and with the remaining time left, I spent it with my other group to work on a final presentation for my careers management subject.

***
***
#### Conclusion `TLDR`
***
***
To summarise, this week was pretty chaotic as we were introduced to `boot2roots` and the basics of Penetration Testing as we were thrown into the 'deep end' and had to hack into our own chosen box. I chose to work collaboratively with another fellow student, Tyrone to hack a box but didn't succeed due to time restraints. Nevertheless, we have already completed the `Vulnversity` box and I have completed the `Basic Pentesting 1` box from Vulnhub, which heightened my understanding on many different techniques to start basic Pen-testing and each with their specific uses such as: `Nmap` `Gobuster` `BurpSuite` `CyberChef` and `GTFObins.`
***
***

Next week I would like to achieve:
- Continue to be more disciplined and keep updating reflection whenever possible
- Do more Linux hacking levels and even attempt a CTF solo or in a group if I can
- Conduct more research into more technical Cyber security content and re-evaluate my problem statement or come up with a new one! (does not have to be same every time - which was addressed from feedback)
- Me and Tyrone hope to learn more in depth about other tools that you can use and even ask the teaching team about it so that progress can be made.
- Finish the `Biohazard` box by next sprint, with assistance if needed
- Try to attempt to meet more learning outcomes by next week if possible

***
***
