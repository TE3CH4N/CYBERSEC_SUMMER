---
title: "Week 6 Reflection"
date: 2020-03-01T02:01:58+05:30
---

***
***
#### Introduction
***
***

This is the 6th and final week of Cyber Security Summer Studio and since most of us have completed a `hackthebox` machine already, we were further challenged to complete another `Hackthebox` machine. Yet again, although we have experience from one of the `hackthebox` boxes from last week, I still needed to do a lot of research into different technical content since we are not allowed to refer to online write-ups (nor are there any published).

Furthermore, two other major highlights of this week was the Google SecTalks event and our Thursday Summer Studio presentation. During the Google SecTalks event, I was mixed up with a random team (shoutout MACSHACK), who already had a variety of beginner and intermediate hackers on the team. Unfortunately our team did not win the CTF challenge, however what I got away from the winning team was the most important. From the experience, I have developed strong communication skills whilst I worked with the other team to reach a common goal and at the end of the day, we all learn something whether it is the process to reach the common goal or how to get there from the winning team.

Moreover, the Thursday presentation went really well as we discussed many key factors about the penetration testing methodology (3 E's) and presented a short, yet guided in-depth demo to two different stakeholders who happen to approach our table.

This last week of summer studio was definitely still ***chaotic*** for me as this was a wrap for our summer studio course and along with the write-ups and the presentations, we would have to submit our final portfolio along with our final two reflections.

***
***
`Hackthebox` **deliverable** due for this week can be found under [logs](https://teechan.me/logs/).

**|OR|**

You can manually visit this **link** here:
1. [HACKTHEBOX:Traverxec](https://www.teechan.me/logs/hackthebox-traverxec/)
***
***

#### Week 6: Pros & Cons
###### To-do list:
- Prepare for studio presentation on Thursday
- Complete writeup for the `Traverxec` box and make sure it is password protected and not released to the public
- Try and complete [Biohazard](https://tryhackme.com/room/biohazard) on `tryhackme` if possible (might updated after portfolio is due)
- Continuing adding screenshots of my chat logs and team collaboration to further show proof of my understanding of the learning outcomes

***
***
###### Pros:
- I was able to retrieve the flag from users.txt in the `Traverxec` box
- Engaged with other students and tutors for help on the `Traverxec` box and helped other students on `Openadmin` as they are required to that box this week
- I was also able to escalate my privileges to become a `root` user!
- Logged my `Hackthebox` achievement [here](https://www.teechan.me/logs/hackthebox-traverxec/)
- Successful Presentation on Thursday to different stakeholders that approached our group during the showcase of our `Openadmin` box presentation
- Continuously learnt different technical concepts throughout the challenges and write-ups which was a really enjoyable experience
- Reflect back on my old reflections and really see how far I have come in terms of skillsets and how much I have accomplished
***
***

###### Cons:
- My procrastination management has definitely gotten a lot better, however, there are times I feel conflicted on whether that procrastination is crucial as I require a break here and there, or is it still an old habit of mine?
- Did not research into coming up with a problem statement as I was too focused on preparing for the final studio presentation with my group and finishing off my reflections and final portfolio
- Could not find the time to collaborate with Tyrone to finish off Tryhackme's `Biohazard`, however, I will update it after the final reflections and portfolio are due, since they are definitely more of a priority.

***
***
#### Weekly Recap
***
***
###### Monday (24/02):
***
***
Today was just a final clarification/face-to-face session with our tutors to see where everyone's current status with our `hackthebox` boxes and to decide on which 'box' to present on Thursday, even if they were the same as other groups, as every group will have a different presentation style. Later in the day, we had our final stand-up scrum meeting for the studio, and a common strength I discovered from the team was that everyone had acquired a decent set of skills when it comes to basic penetration testing and have improved a fair amount. Likewise, we also shared a common weakness as a class, where we all still struggled with minor procrastination (maybe just a uni student thing), however, we are all still diligently working towards it!

Moreover, I started to work on `Traverxec` from `hackthebox` after our lunch break and immediately saw similarities from `openadmin`, which I completed last week. This really assisted in me completing the early steps of the box, as some initial technical content such as using `ssh2john` and discovering files in the `/var ` directory were learnt last week, therefore, understanding which exploit to use immediately, which saved me a `lot` of time.
***
***
###### Tuesday (25/02):
***
***
Today my group and I met up at uni to work on the presentation. I suggested we first allocate sub topics of the presentation among the group, so it will be easier to explain our whole process. Additionally, we then split each of the `3 E's` (Enumeration --> Exploitation --> Escalation) amongst ourselves so it would lighten the workload. We would then proceed to do a practice run to go over the whole presentation, treating it like a `stall` of some sort, where we would pretend that stakeholders would walk up to our group and we would have formally introduce ourselves and what we did throughout the whole summer studio.

Later on in the day, we then decided that Hayden (fellow group member) would record the demonstration as he had the most experience with `openadmin`, but he was also the first member in our group to achieve `root` access for that particular box. Consequently, I volunteered to edit the video as I have some decent prior experience in video editing, while Nicholas and Tyrone (other group members) would polish up the slides and decide which other parts of our 'script' needed fixing up. I also suggested we should purchase a pack of candy to provide to stakeholders for actively listening to our presentation or even to lure them in (`haha you never know`)

You can view our video demonstration [here](https://youtu.be/18uakx2QGEM).

Later that night, there was a **Sectalks** `ninja night` from 6pm to 8:30pm that I attended at Google. It was a capture the flag event where anyone could join, ranging from beginner to intermediate. This event can be viewed [here](https://www.meetup.com/SecTalks/events/268794019/). Here are some `cool and aesthetic` photos of Google and some `awkward` "poses" from our UTS CSec team.

![Screenshot4.png](/google/google2.jpg)
![Screenshot4.png](/google/google3.jpg)
![Screenshot4.png](/google/google1.jpg)
***

From the event, I learnt a lot of technical content, especially about how server-less websites operate and how easily .YAML files can be tricked into re-directing to a different URL. I also learnt that effective collaboration and communication was necessary within a team in order to succeed, and the the winning team did this really well, as they knew each other strengths and weaknesses, which tools to use and constant status updates from each member to see if everyone was on the same page. After the event, our UTS CSec group had a little discussion of the solution to this CTF.

![Screenshot4.png](/images/unhackable1.png)
![Screenshot4.png](/images/unhackable2.png)
!![Screenshot4.png](/images/unhackable3.jpg)

***
***
###### Wednesday (26/02):
Met up with Hayden today for our final drop-in session to discuss further in depth about our presentation style and to see how much we needed to cut down if it comes down to it.

Additionally, we then accomplished a few tasks along with clarifying some points with the teaching team:
- Confirm with the teaching team whether we can discuss the same HTB box as other groups and how long will the presentation be
- Ask whether or not we require slides and how formal does the presentation need to be
- Teach Hayden how to use the screen capture software (Kazam) in Kali Linux
- Edit video with voiceover (realised we did not need it as it would be more interactive to explain the our steps and technical concepts to them on the spot)
- Maybe consider adding title pages as pauses throughout video so team members can talk over it?
- Design slides some `aesthetic` looking slides on Canva as prompt for discussing our project, which can be viewed [here](https://www.canva.com/design/DAD06vZ1_Gc/MKdqoUsrheucawdP7wEbsw/view?utm_content=DAD06vZ1_Gc&utm_campaign=designshare&utm_medium=link&utm_source=sharebutton)

![Screenshot4.png](/images/openadminpres1.png)

At night:
I successfully retrieved `Traverxec's` user.txt flag and continued to document the write-up as I go, so I do not have to rush it last minute.
***
***
###### Thursday (27/02):

Today was UTS' Open day, but also our UTS Summer Studio booth presentation to Roger and other facilitators. It was showcase day and our group are required to present our project, which is a box that we hacked into, successfully captured the user and root flag and acquired `root` access to the virtual box. Despite not having many stakeholders showing up to our specific stall (mainly because we were allocated to a corner), I still had a great opportunity to practice my `on-the-spot` presentation skills, which is crucial in the IT workplace.

It was definitely not as intimidating as I thought it would be, as I believe we were one of the studios where you would need to have a passion about info security or just curious about ethical hacking to come visit our studio. Since Tyrone (fellow group member) could not make it today due to his sickness, he had made sure to inform me the night before that he was not coming, but more so on how he would present his section, ensuring that I would not be confused when it came around to this section.

One of the fellow stakeholders who came along to our 'stall' was a middle-aged professor in the FEIT Faculty. We could immediately tell he has some experience with UNIX systems with his frequent nodding, thus, we did not feel the need to hold back when describing some difficult technical content to him. However, there was another stakeholder who had basic UNIX knowledge, but had forgotten most of the content because he has not been in touch with UNIX systems for over a decade. Therefore, this prompted me and my group to explain the content-heavy portions of the demonstration in more simpler words and using a scenario to demonstrate a real poor exploit for example, and even relating the `enumeration` process of Pen-Testing to the `evaluation` period of a `Gantt Chart` where both processes are to be performed throughout the whole project.

Moreover, after our presentation was over, I listened in to one of our fellow group members (Hayden) having a conversation with the professor about cyber security subjects in general at UTS. One of the key points I got away from the conversation was that, Hayden to tried to persuade the professor that understanding cyber security concepts are overwhelming and intimidating and just having lectures and lab content is definitely not enough. Thus, having an intensive 6 week summer studio course along with your normal 12 week lecture + lab semester will definitely help you and put you above other students who are just doing the 12 week semester. Furthermore, another fact that Hayden brought up to the professor, which I can definitely relate with, is the fact that although we were thrown into the deep end of how to `hack` a box, especially because we have no experience in hacking any virtual boxes, the final technical skillset you achieve comes with a lot of practice and continuous feedback from the teaching team.


***Here are some photos of:***

1. ***Our showcase group***

2. ***Our cybersecurity summer studio group***

3. ***All studios together :)***

![Screenshot4.png](/images/summer05.jpg)
![Screenshot4.png](/images/summer1.jpg)
![Screenshot4.png](/images/summer2.jpg)
![Screenshot4.png](/images/summer3.jpg)



***
***
###### Friday + Weekend (28/02 - 01/03):
- Finished off `Traverxec` by finding the `root` flag.

![Screenshot4.png](/images/htbownedmachines.png)

- Polish up Reflections 5 and 6
- Start Final Portfolio along with polishing the 2 final reflections
***
***
#### Conclusion `TLDR`
***
***
To summarise, my final week here at my cybersecurity summer studio has been quite stressful and chaoctic, since not only do we have to prepare a presentation to different stakeholders, but we also have to construct another write-up on how we achieved `root` in another HTB box and finally to document our reflection for week 5 and 6, along with a final portfolio submission.

Consequently, this stressful week taught me a lot of new technical content such as learning how `JournalCTL` works in the `Traverxec` box and how serverless architecture works along with .YAML files being easily manipulated on the Google SECtalks event on Tuesday night. Moreover, I polished and re-skilled my presentation skills during Thursday's summer studio presentation and further learnt how to effectively communicate with stakeholders with different skillsets. Furthermore, from my knowledge gained from completing the `openadmin` box last week, I was able to utilise that knowledge into acquiring both the user and root flag in `Traverxec`!

Overall, looking back at my previous reflections, there has been serious changes in my workflow, my technical understanding and my attitude towards frustrating moments, and I am definitely happy to see some positive change in all those areas :)
***
***


***
***
