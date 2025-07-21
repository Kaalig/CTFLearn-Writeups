**Forensics - Tux! - 20 Pts**

Challenge :

*The flag is hidden inside the Penguin! Solve this challenge before solving my 100 point Scope challenge which uses similar techniques as this one.* followed with a Tux.jpg file.

I  don't have much clues on this one so I'm gonna make my routine which consist first of using `file` to see what type of files we're dealing with. 

![]()
![](https://github.com/Kaalig/CTFLearn-Writeups/blob/1f3eac0b6f3c29b95ce2a7aed3da081ab4eb4a0b/images/Pasted%20image%2020250625201024.png)

Luckily we came across a weird comment that looked like base encrypted, let's give a try with a base64, and it looks like we need a password somewhere, let's store it somewhere.
For me that means the file contain much more things, let's use `binwalk` to see.

![](https://github.com/Kaalig/CTFLearn-Writeups/blob/1f3eac0b6f3c29b95ce2a7aed3da081ab4eb4a0b/images/Pasted%20image%2020250625201427.png)


It actually has a zip archive that contains the flag when the flag password is entered. Nice little challenge :)
