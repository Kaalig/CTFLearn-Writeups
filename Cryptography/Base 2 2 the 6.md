**Base 2 2 the 6 - 20 Pts - Crypto**

Challenge :

*There are so many different ways of encoding and decoding information nowadays... One of them will work! Q1RGe0ZsYWdneVdhZ2d5UmFnZ3l9*


For this exercice, we got a string of character encoded in a base. base64 is the most known base. In the title it says "Base 2 2 the 6" and for some reason, 2+2 = 4 and we got the 6 which means base 64 haha. Let's see if we're onto something, using the "Magic" of  CyberChef :

![](https://github.com/Kaalig/CTFLearn-Writeups/blob/326a07b6100e49ba826fb0ad3aacec582dc7f606/images/Pasted%20image%2020250624011125.png)

Not even need to check it manually, we already got a good result snippet !

However, we can also do this exercice faster by using only one command and one pipeline : `echo "Q1RGe0ZsYWdneVdhZ2d5UmFnZ3l9" | base64 -d` and it will also give us the flag.
