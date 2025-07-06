**Forensics - Forensics 101 - 30 Pts**

Challenge :

*Think the flag is somewhere in there. Would you help me find it? https://mega.nz/#!OHohCbTa!wbg60PARf4u6E6juuvK9-aDRe_bgEL937VO01EImM7*


We have to download the MEGA file which contains an image. Because it's an image, I first gonna use the `file` to see if its really an image, then `exiftool` to get more information. I'll also see if there's some strings in the file with the `strings` command. Lastly if all commands are unsuccessful, I will use `binwalk` to find if there's another data inside this data. 


![](https://github.com/Kaalig/CTFLearn-Writeups/blob/fa585f1aead241cf90f274e1400a2b860b06bc1d/images/Pasted%20image%2020250627190839.png)

Okay so nothing interesting. Let's see the strings in the file such as `strings IMAGE_NAME` : 

![](https://github.com/Kaalig/CTFLearn-Writeups/blob/fa585f1aead241cf90f274e1400a2b860b06bc1d/images/Pasted%20image%2020250627190934.png)


