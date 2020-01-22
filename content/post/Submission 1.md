---
title: "Reflection 1"
date: 2019-01-25T02:01:58+05:30
description: "Reflection on the first sprint submission."

---



# Submission 1:

## Things to include in motivation intro:

- SS of pre form before summer studio started (what I wanted out of tutors and etc)
- SS of written notes of what i want to get out of Summer Studio Cyber Security

## SLO's:

Upon successful completion of this subject students should be able to:

1. Engage with stakeholders to identify a problem or scope a defined problem.
2. Apply design and systems thinking to respond to a defined or newly identified problem.
3. Apply technical skills to develop, model and/or evaluate designs.
4. Demonstrate effective collaboration and communication skills.
5. Conduct critical self, peer, and group review and performance evaluation.

## List of steps that I followed (to create my first sprint submission):

- Get familiar with the subject outline and its SLO's
- Join MS Teams
- Open Wiki tab under Cyber Security Summer Studio and follow instructions under Week 1
- Github education pack —> [Namecheap.com](http://namecheap.com) —> link Github with namecheap domain —> Install Hugo and start creating a site with one of Hugo's Themes —> Creating markdown files under quickstart/content/post folder, which will be used to display your sprint submissions (personal portfolio) as a static site —> Look up on how to upload files onto GitHub manually because i had troubles in CLI (images down below) —> Login to Netlify with GitHub and change dns servers to custom on namecheap dashboard to point to Netlify dns' (instructions: [https://skilstak.io/changing-dns-on-namecheap-to-point-to-netlify/](https://skilstak.io/changing-dns-on-namecheap-to-point-to-netlify/)) —> Deploy server (learn how to gain remote access/push + pull)
-

![Screenshot4.png](/images/screenshot4.png)

keep having "error: 'themes/' does not have a commit checked out fatal: adding files failed" issue when trying to upload local repos to GitHub

![Screenshot1.png](/images/screenshot1.png)

![Screenshot2.png](/images/screenshot2.png)

Add files to stage —> Commit the files —> push the file onto online repo

Another Problem I had was deploying site on netlify was it wans't the right hugo version:

- I fixed this by checking the version of HUGO on my terminal (version 0.62.2) and then i matched it on Netlify under Site Settings/build & deploy/Environment

![Screenshot3.png](/images/screenshot3.png)
