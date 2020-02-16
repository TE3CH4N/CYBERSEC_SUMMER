---
title: "TRYHACKME: Biohazard Writeup"
date: 2020-02-16T02:01:58+05:30
---


#### Biohazard:

- `Welcome to Biohazard room, a puzzle-style CTF. Collecting the item, solving the puzzle and escaping the nightmare is your top priority. Can you survive until the end?`
- My first impressions of this tryhackme box is that it looks intimidating and long as this is suggested for intermediate levels, but lets give it a try anyway and see how far we go...

---


#### Task 0.5: Set up VPN

#### Task 1: Introduction:

Deploy the machine!

![TRYHACKME%20Biohazard/Untitled.png](/BIOHAZARD/bio05.png)

Hence, we are given an hour before this active machine expires, so lets get cracking!

(if you need more time, don't hesitate to `add 1 hour` to keep the server running)

#### Task 2: The Mansion

- Now we are tasked with finding `open ports` and `team name in operation`:
- Lets use `nmap` to scan for open ports and find what we can exploit/target

![TRYHACKME%20Biohazard/Untitled%201.png](/BIOHAZARD/bio1.png)

And as we can see from the above nmap scan, we see that the http port 80 is open, thus, meaning that it has something to do with the webpage

I then typed in the ip address in a new browser window and I was brought into main page.

- Here we can see the team name in operation and another link which brings you to the `main` hall page as shown below
- I then pressed `ctlr+u` to open the page source and found a few clues which is also indicated down below:

    ![TRYHACKME%20Biohazard/Untitled%202.png](/BIOHAZARD/bio2.png)

- The next step was to find the emblem and input it.
- However, there was nothing there when i entered it.
- Therefore, I had another look at the page source then found a weird base64 format code.
- I chucked this formatted code to decode it from Base64, which gives me the clue to the next room:

    ![TRYHACKME%20Biohazard/Untitled%203.png](/BIOHAZARD/bio3.png)

From the information, i went into the `/teaRoom/`:

- After inspecting the page source, I found the lockpick emblem flag:

    ![TRYHACKME%20Biohazard/Untitled%204.png](/BIOHAZARD/bio4.png)

- Then, i proceeded into the `/artRoom/` as suggested by the last sentence

    ![TRYHACKME%20Biohazard/Untitled%205.png](/BIOHAZARD/bio5.png)

**Within /artRoom/:**

![TRYHACKME%20Biohazard/Untitled%206.png](/BIOHAZARD/bio6.png)

- Let's head into and investigate it by clicking on the link `yes`

    ![TRYHACKME%20Biohazard/Untitled%207.png](/BIOHAZARD/bio7.png)

    We got ourselves a map of the different directories

    Lets have a look around and see what we find...

First, I entered the `/barRoom/` and entered the key

- First attempt didn't work as i forgot to include `lock_pick` before the bracket
- After that we are brought to the room called: `/barRoom357162e3db904857963e6e0b64b96ba7/`
- Here we can play the piano by finding the piano flag:
- Had to play around the Cyberchef a little bit since the retrieved format from the music sheet page was not in base 64 but rather it was base 32...

![TRYHACKME%20Biohazard/Untitled%208.png](/BIOHAZARD/bio8.png)

Then it prompts me to the `secret bar room`

- I clicked the 'yes' prompt, which takes me to a "gold emblem flag" which can be used to progress further...

    ![TRYHACKME%20Biohazard/Untitled%209.png](/BIOHAZARD/bio9.png)

    However, the gold emblem retrieved from the prompt, does not work within the secret bar room, nevertheless I thought of  inputting the old emblem flag retrieved earlier and see if that works...

    - Well, it did work...
    - However it only displayed a user called `Rebecca`
    - Strange.. Let's explore other rooms
    - The other rooms did not show anything interesting as they require flag emblems, however `/diningRoom2F` was quite special. It had random text under the paragraph after i viewed the page source:

    `A simple caesar substitution cipher which rotates alphabet characters by the specified amount (default 13).`

    ![TRYHACKME%20Biohazard/Untitled%2010.png](/BIOHAZARD/bio10.png)

    ![TRYHACKME%20Biohazard/Untitled%2011.png](/BIOHAZARD/bio11.png)

- After some playing around with Cyberchef's top 10 decoders, me and Tyrone found out that this was actually encoded in ceasar substitution cipher called ROT13:
- `A simple caesar substitution cipher which rotates alphabet characters by the specified amount (default 13).`

    ![TRYHACKME%20Biohazard/Untitled%2012.png](/BIOHAZARD/bio12.png)

- With that information known, we can head back and check the other rooms...
- First we need to head to the dining room and add `sapphire.html` at the end of the url to obtain the blue_jewel flag. Let's see if this works...
- Nope. `Nothing happens` interesting...

Let's check the other rooms and see what we can find...

- There's something interesting in `/galleryRoom` :

    ![TRYHACKME%20Biohazard/Untitled%2013.png](/BIOHAZARD/bio13.png)

- If we view page source, we can see a given clue:

    ![TRYHACKME%20Biohazard/Untitled%2014.png](/BIOHAZARD/bio14.png)

- From that information, we can head over to [Cyberchef]([https://gchq.github.io/CyberChef/](https://gchq.github.io/CyberChef/)) and determine what its encoding was, since it has been encoded twice and the final output has a length of `18 letters`
- Therefore, based on the given information and what i've researched, the only base format that has a length of `18 letters` is `base58:`
- Thus, I put these encoders into Cyberchef

    ![TRYHACKME%20Biohazard/Untitled%2015.png](/BIOHAZARD/bio15.png)

- This should be used for `Crest 2`  —> let's save this for later, as we need to use all crests and decode that to get the combination:

For now, let's have a look at the other rooms for clues...

- Recalling back to `/diningRoom/` and the successfully retrieved `golden emblem` flag. Since the original `emblem flag` worked on the secret bar room, that meants the `golden emblem` flag must work in the `/diningRoom`!

    ![TRYHACKME%20Biohazard/Untitled%2016.png](/BIOHAZARD/bio16.png)

    - Now, when entered the golden emblem flag, it prompts me to a a `.php` file with random text.
    - Following the hint on the tryhackme page: I figured out that it should be a `Vigenere  Cipher`
        - From further research: `A Vigenere cipher is a poly-alphabetic substitution system that use a key and a double-entry table.`
    - Here, Tyrone also added that alongside the Vigenere cipher, there needs to be a key that was needed t to decode the cipher. Thus, I immediately thought "Hey, we haven't used rebecca yet right? And it doesn't fit into any answers on tryhackme, so lets give this a go

Let's convert this `fuzz` with the retrieved key `rebecca`, on cyberchef:

- `rebecca` was the key!

    ![TRYHACKME%20Biohazard/Untitled%2017.png](/BIOHAZARD/bio17.png)

From the given output clue, lets head over to the dining room and add `the_great_shield_key`to the end of the URL... And VOILA! The shield emblem key!

Now, lets head over to the other rooms which require the shield emblem flag:

- `/attic/` seems like a good place to start:

    ![TRYHACKME%20Biohazard/Untitled%2018.png](/BIOHAZARD/bio18.png)

    ![TRYHACKME%20Biohazard/Untitled%2019.png](/BIOHAZARD/bio19.png)

    Here, we are brought to a new page and a new clue about `crest no.4`

    ![TRYHACKME%20Biohazard/Untitled%2020.png](/BIOHAZARD/bio20.png)

    Let's save this for now... (since we don't need to decode crest 4)

    Let's head into the `/armorRoom`:

    ![TRYHACKME%20Biohazard/Untitled%2021.png](/BIOHAZARD/bio21.png)

    - Enter the same shield emblem and we should get something here:
    - There we go! Crest 3! Only Crest 1 Left!

    ![TRYHACKME%20Biohazard/Untitled%2022.png](/BIOHAZARD/bio22.png)

    ![TRYHACKME%20Biohazard/Untitled%2023.png](/BIOHAZARD/bio23.png)

Thinking back to the `/tigerstatusRoom/` which we could not complete because we were missing the `blue_jewel` emblem flag, we now can complete it...

We can use the `blue_jewel` emblem flag retrieved earlier to see if it works here:

![TRYHACKME%20Biohazard/Untitled%2024.png](/BIOHAZARD/bio24.png)

Voila! IT WORKS and we also get `Crest no.1` as well:

![TRYHACKME%20Biohazard/Untitled%2025.png](/BIOHAZARD/bio25.png)

We stumble upon the next challenge which is to combine every crest and somehow determine what the the encoded base is using Cyberchef:

- Luckily we made a Google doc to note down our emblem flags and crest records:

![TRYHACKME%20Biohazard/Untitled%2026.png](/BIOHAZARD/bio26.png)

We should now move on to decode our crests down to its original output —> then combine everything into one huge block of text, and finally convert that password.

... TO BE CONTINUED ...

***TO BE COMPLETED BY NEXT WEEK***

- Research into different base encodings and get familiar with their character lengths ***(as its the main reason that halted my progress because I don't have a firm grasp on the different types of encoding formats)***
- Research into different ciphers and how they work
- Research into FTP and SSH Exploits

---

***My impression of this challenge so far has changed a bit since this box does not seem as intimidating as i initially thought it would be, however it is still very tedious... - D Y L A N***
