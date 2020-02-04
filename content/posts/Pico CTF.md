---
title: "PicoCTF Logs"
date: 2020-01-30T02:01:58+05:30
---



### Pico CTF

- Register an account on Pico CTF and join a collaborative team with Hayden
- Start the game and go through general skills (as I am a total beginner to CTF's)

#### General Skills

Binary Conversion Table [here](https://www.systutorials.com/4670/ascii-table-and-ascii-code/)

##### 1. 2Warm - `Can you convert the number 42 (base 10) to binary (base 2)?`

- Literally just used a base 10 to base 2 converter online lol (not sure if you can might have to double check Jason/Larry next week
- Solution: `PicoCTF{101010}`

![Pico%20CTF/Untitled.png](/images/pico5.png)

***

##### 2. Let's Warm up - `If I told you a word started with 0x70 in hexadecimal, what would it start with in ASCII?`

- Used an online converter, or you can refer to the Binary Conversion [Table](https://www.systutorials.com/4670/ascii-table-and-ascii-code/) again
- Solution `picoCTF{p}`

***

##### 3. Warmed Up - What is 0x3D (base 16) in decimal (base 10).

- 0x3D base 16 to decimal is 61
- Thus, solution is `picoCTF{61}`

***

##### Current view for tasks:

![Pico%20CTF/Untitled%201.png](/images/pico1.png)

![Pico%20CTF/Untitled%202.png](/images/pico2.png)

##### 4. Bases - What does this `bDNhcm5fdGgzX3IwcDM1` mean? I think it has something to do with bases.

- Had to do some research into the bases and bound base64 encoding (literally looked up what type of base encoding is bDnhcm...)
- "Each Base64 digit represents exactly 6 bits of data. Three 8-bit bytes (i.e., a total of 24 bits) can therefore be represented by four 6-bit Base64 digits."
- Did some research on StackExchange:

    ![Pico%20CTF/Untitled%203.png](/images/pico3.png)

- Thus, I would have to decode from base64 format —> using the command `echo` to show the contents and `| base64 --decode` to decode the base64 string.
- Go back to shell and type: `echo "bDNhcm5fdGgzX3IwcDM1" | base64 --decode`
    - Giving you:

        ![Pico%20CTF/Untitled%204.png](/images/pico4.png)

- Thus solution is `picoCTF{l3earn_th3_r0p35}`

***

##### 5.  First Grep - `Can you find the flag in file? This would be really tedious to look through manually, something tells me there is a better way. You can also find the file in /problems/first-grep_3_2e09f586a51352180a37e25913f5e5d9 on the shell server.`

- As suggested by the challenge name —> we would need to execute the bash command `grep` to search for the flag within the pico file.
