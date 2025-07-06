**I'm a dump - Forensics - 10 Pts**

Challenge :

*The keyword is hexadecimal, and removing an useless H.E.H.U.H.E. from the flag. The flag is in the format CTFlearn{*}* + a file attached named "file".



For this challenge, I checked  first what type of file we working on with the command  `file` : 

![](https://github.com/Kaalig/CTFLearn-Writeups/blob/6a8087ffe8eef4804cace12d37aa1da0a1c77de5/images/Pasted%20image%2020250624212954.png)

It's an ELF file. These type of files are generally used to stock libraries, binaries and essentials dumps in the disk on a linux platform. 
I, then, tried to open the file with a simple  `cat`

![](https://github.com/Kaalig/CTFLearn-Writeups/blob/6a8087ffe8eef4804cace12d37aa1da0a1c77de5/images/Pasted%20image%2020250624213339.png)

If we look closely, we can see a beginning of flag but in a weird way. We also know that there's strings so in order to read it well, just use the `strings` command.

![](https://github.com/Kaalig/CTFLearn-Writeups/blob/6a8087ffe8eef4804cace12d37aa1da0a1c77de5/images/Pasted%20image%2020250624213455.png)


We got the flag but still, don't forget that we need to delete a H in the flag, as they tell us in the challenge. 

Ta-da, another success !!
