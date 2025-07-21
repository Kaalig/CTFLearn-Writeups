**Chalkboard - Forensics - 30 Pts**

Challenge :

*Solve the equations embedded in the jpeg to find the flag. Solve this problem before solving my Scope challenge which is worth 100 points.*


After downloading the file, I check for embedded content with `file` and `binwalk` :

![](https://github.com/Kaalig/CTFLearn-Writeups/blob/48c6b358424fb37a4f4d415446bef444a1cb4588/images/Pasted%20image%2020250714212334.png)

Then I use `strings`  and I basically have the flag. You just have to resolve this cute equation :

![](https://github.com/Kaalig/CTFLearn-Writeups/blob/48c6b358424fb37a4f4d415446bef444a1cb4588/images/Pasted%20image%2020250714212358.png)
