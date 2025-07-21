**Pho is tasty! - Forensics - 30 Pts**

Challenge :

*The flag is hidden in the jpeg file. Good Luck! Have some Pho! Solve this challenge before solving my Scope challenge for 100 points.*

So I have a lot of tools to find something in a file. Basically I used all of the below tools without success :
- `file Pho.jpg` that confirm it's only a jpg file.
- `binwalk Pho.jpg` but nothing comes out.
- `strings Pho.jpg` but I didn't found something at first glance.
- `exiftool Pho.jpg` but nothing interesting.

 ![](https://github.com/Kaalig/CTFLearn-Writeups/blob/00dc4ffb6ff97dd5471d90121e55d77658dabf23/images/Pasted%20image%2020250714214328.png)

Then I tried to create an hexadecimal image out of the binary file we have, to see the strings better and maybe spot something in the hex :

![](https://github.com/Kaalig/CTFLearn-Writeups/blob/00dc4ffb6ff97dd5471d90121e55d77658dabf23/images/Pasted%20image%2020250714214429.png)


That is why we couldn't see the flag with the strings and a keyword : it was sort of hidden.
