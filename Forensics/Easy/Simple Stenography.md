**Simple Steganography - Forensics - 30 Pts**

Challenge :

*Think the flag is somewhere in there. Would you help me find it? hint-" Steghide Might be Helpfull"*

So before using the tool `steghide` , a steganographic tool allowing us to embed secret data into various type of files like `jpeg wav bmp` and much, we're going to use `strings` to find some data that could lead us to a password that is going to be mandatory in order to unlock the secret password.

![](https://github.com/Kaalig/CTFLearn-Writeups/blob/426a03cddef0290a4bf50c82de1d0c2e0bde8637/images/Pasted%20image%2020250714215648.png)

We have a `myadmin` string that looks awfully suspicious, and a string of character that we're gonna keep under the belt.

![](https://github.com/Kaalig/CTFLearn-Writeups/blob/426a03cddef0290a4bf50c82de1d0c2e0bde8637/images/Pasted%20image%2020250714215648.png)


Let's see if with those few info we can have the secret data with this command `steghide extract --sf file.jpg` :

![](https://github.com/Kaalig/CTFLearn-Writeups/blob/426a03cddef0290a4bf50c82de1d0c2e0bde8637/images/Pasted%20image%2020250714220108.png)

*Note : refer to `steghide --help` for a complete understanding of the tool, there is not much argument so it is easily understandable. You can do it in less than 5 minutes.*

Alright, so we input the `myadmin` string and it works on the first try ! Let's see what we got in this text file : 

![](https://github.com/Kaalig/CTFLearn-Writeups/blob/426a03cddef0290a4bf50c82de1d0c2e0bde8637/images/Pasted%20image%2020250714220121.png)

Basically we got a base encoded data. Since base64 is the most used in these types of challenge, I tried it and found the flag.
