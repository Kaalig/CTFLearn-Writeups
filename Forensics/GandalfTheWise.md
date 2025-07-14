**Gandalf The Wise - Forensics - 30 Pts**

Challenge :

*Extract the flag from the Gandalf.jpg file. You may need to write a quick script to solve this.*

First reflex after downloading the file is to use `file Gandalf.jpg` and we get this : 

![](https://github.com/Kaalig/CTFLearn-Writeups/blob/96c0741f674a55ed8a48405f2dad85a7dcd57464/images/Pasted%20image%2020250714221744.png)

The first comment, in base64 decoded, says : `CTFlearn{xor_is_your_friend}`
The others one shows nothing, so I suspect it might be the comments we're going to xor.

Basically, to use XOR we need byte strings, and we need two of them to make the calculus. On cyberChef here's what i did : From Base64 - To Hex for both

![](https://github.com/Kaalig/CTFLearn-Writeups/blob/96c0741f674a55ed8a48405f2dad85a7dcd57464/images/Pasted%20image%2020250714222848.png)
![](https://github.com/Kaalig/CTFLearn-Writeups/blob/96c0741f674a55ed8a48405f2dad85a7dcd57464/images/Pasted%20image%2020250714222908.png)

Then I use **xor.pw** to :

![](https://github.com/Kaalig/CTFLearn-Writeups/blob/96c0741f674a55ed8a48405f2dad85a7dcd57464/images/Pasted%20image%2020250714223342.png)

And then we find the flag with the result : 
![](https://github.com/Kaalig/CTFLearn-Writeups/blob/96c0741f674a55ed8a48405f2dad85a7dcd57464/images/Pasted%20image%2020250714223410.png)

I have probably done a typo but the flag always start with CTFLearn so it's no big deal.
