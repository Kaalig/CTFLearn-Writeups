**Minions - Forensics - 20 Pts**


Challenge :

*Hey! Minions have stolen my flag, encoded it few times in one cipher, and then hidden it somewhere there: https://mega.nz/file/1UBViYgD#kjKISs9pUB4E-1d79166FeX3TiY5VQcHJ_GrcMbaLhg Can you help me? TIP: Decode the flag until you got a sentence.* 


A mix of forensics and cryptography I guess. I'll first see if I can have more information with `exiftool` and `file` and then `binwalk`

![](https://github.com/Kaalig/CTFLearn-Writeups/blob/0a3a1f46de3a068a5370c9a48787f55e1d7b79bb/images/Pasted%20image%2020250625201950.png)
![](https://github.com/Kaalig/CTFLearn-Writeups/blob/0a3a1f46de3a068a5370c9a48787f55e1d7b79bb/images/Pasted%20image%2020250625202008.png)

We have few archive and compressed data, after we extracted them, we have  an useless 5B file with his zlib data and a directory full of others directory in the rar archive. It looks boring to find something manually so let's apply some filters first :

![](https://github.com/Kaalig/CTFLearn-Writeups/blob/0a3a1f46de3a068a5370c9a48787f55e1d7b79bb/images/Pasted%20image%2020250625202623.png)
![](https://github.com/Kaalig/CTFLearn-Writeups/blob/0a3a1f46de3a068a5370c9a48787f55e1d7b79bb/images/Pasted%20image%2020250625202702.png)

Strange, let's look at it since it's a supposedly ".txt" file.

![](https://github.com/Kaalig/CTFLearn-Writeups/blob/0a3a1f46de3a068a5370c9a48787f55e1d7b79bb/images/Pasted%20image%2020250625202745.png)

Another image to download !

![](https://github.com/Kaalig/CTFLearn-Writeups/blob/0a3a1f46de3a068a5370c9a48787f55e1d7b79bb/images/Pasted%20image%2020250625203018.png)

Im doing the same thing I did for the first image. Again nothing interesting in the image.

![](https://github.com/Kaalig/CTFLearn-Writeups/blob/0a3a1f46de3a068a5370c9a48787f55e1d7b79bb/images/Pasted%20image%2020250625203238.png)

A suspicious CTF flag that looks encrypted, let's decrypt it. In the challenge context, it says that multiple decoding is pretty much necessary. I'll keep on trying decoding in base64 multiple time as long as the output coming out is shorter till I have a phrase.

![](https://github.com/Kaalig/CTFLearn-Writeups/blob/0a3a1f46de3a068a5370c9a48787f55e1d7b79bb/images/Pasted%20image%2020250625203552.png)

And here it is ! The flag ! Awesome challenge, I've enjoyed it a lot.


