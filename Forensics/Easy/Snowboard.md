** Snowboard - Forensics - 20 Pts**

Challenge :

*Find the flag in the jpeg file. Good Luck!* + a file .jpg attached to it.



This one got me a little trouble. First of all we download the image, then I use the exiftool :

![](https://github.com/Kaalig/CTFLearn-Writeups/blob/c18f5ad4d142efd4c4702ff9960438e59d34d1f9/images/Pasted%20image%2020250625194444.png)

There's a flag in the comment section. At first I was like "Another one done, nice" but then I realized it was a false flag and not the real one.
I, then, try to see if there's another flag that I have overlooked, no success. I used the `binwalk` command but it wasn't successful neither.

![](https://github.com/Kaalig/CTFLearn-Writeups/blob/c18f5ad4d142efd4c4702ff9960438e59d34d1f9/images/Pasted%20image%2020250625194557.png)

Maybe there was some hidden files that I've didn't see ? 

![](https://github.com/Kaalig/CTFLearn-Writeups/blob/c18f5ad4d142efd4c4702ff9960438e59d34d1f9/images/Pasted%20image%2020250625194739.png)

Still not. At this point I'm telling myself that I should go back to the bases of what I know for this challenge, using `file` to understand it better.

![](https://github.com/Kaalig/CTFLearn-Writeups/blob/c18f5ad4d142efd4c4702ff9960438e59d34d1f9/images/Pasted%20image%2020250625194910.png)

What's this ? It looks like a base64 message with the == at the end and it wasn't showed when I used my exiftool. Let's decrypt it :

![](https://github.com/Kaalig/CTFLearn-Writeups/blob/c18f5ad4d142efd4c4702ff9960438e59d34d1f9/images/Pasted%20image%2020250625195020.png)

Luckily, this one is the REAL flag !

Pretty good for a very easy challenge.
