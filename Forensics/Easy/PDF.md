**PDF - Forensics - 20 Pts**

Challenge :

*Hi, just as we talked during a break, you have this file here and check if something is wrong with it. That's the only thing we found strange with this suspect, I hope there will be a password for his external drive
Bye* + a "dontopen.pdf" file attached to it.

After downloading the file, that looks like that :

![](https://github.com/Kaalig/CTFLearn-Writeups/blob/main/images/Pasted%20image%2020250714204220.png)

I make sure that it's really a pdf file by using the command `file dontopen.pdf`

After that I search for meaningful strings into the document with the command `strings dontopen.pdf`. I tend to pipeline it with a `grep "flag_template"` but I don't have much creativity today.

![](https://github.com/Kaalig/CTFLearn-Writeups/blob/6f7c353da4979f13eb7e12eb63e71f5842160272/images/Pasted%20image%2020250714204431.png)
![](https://github.com/Kaalig/CTFLearn-Writeups/blob/6f7c353da4979f13eb7e12eb63e71f5842160272/images/Pasted%20image%2020250714204459.png)


It's obviously a base64 encoding because of the classic '= =' at the end. Anyway, we get the password by decoding it :)
