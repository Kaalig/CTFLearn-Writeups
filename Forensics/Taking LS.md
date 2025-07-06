**Taking LS - 10 Pts - Forensics**

Challenge :

**


Okay, we got a MEGA link in the summary, let's download it and unzip it.

![](https://github.com/Kaalig/CTFLearn-Writeups/blob/edfc8ef5021f28b3e1c0a01a5f957cf0367fba3d/images/Pasted%20image%2020250624215813.png)

We can see that there's a file named "The flag.pdf", let's read it onto our browser : 

![](https://github.com/Kaalig/CTFLearn-Writeups/blob/edfc8ef5021f28b3e1c0a01a5f957cf0367fba3d/images/Pasted%20image%2020250624215713.png)

A password ? Im checking the files but I don't see anything close to a password, and then I remember the name of the CTF and it clicked in my head. CTF's name is "taking LS" . `ls` is a command to list file, but you can also list hidden files additionally with  `ls -la` as an argument : 

![](https://github.com/Kaalig/CTFLearn-Writeups/blob/edfc8ef5021f28b3e1c0a01a5f957cf0367fba3d/images/Pasted%20image%2020250624215945.png)


Alright, just need to enter the password and we good :)
