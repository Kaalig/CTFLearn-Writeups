**Abandoned Place - Forensics - 30 Pts**

Challenge :

*the flag is outside of the pic, try to find it. another hint: dimensions, dimensions, everything is in dimensions.*


The challenge give us a big hint : there's a part of the image that are not visible because of the dimension of the image.
Didn't know how to manually do it so I found a great website to explain in depth , and basically all we need to do is :
- Using CyberChef, puttin my image in the input in order to have the Hex of it.
- Because it is a .jpg image, it has the signature `ff d8` at first.

![](https://github.com/Kaalig/CTFLearn-Writeups/blob/d407f6e185c0db1af480898eb6e753a0912272b9/images/Pasted%20image%2020250721211707.png)

- Then we put our hex value in the input and find the `ff c0` values and what"s after. Those hex values are the marker identifier baseline that is the most used to change the width and height of a file :

- 
![](https://github.com/Kaalig/CTFLearn-Writeups/blob/d407f6e185c0db1af480898eb6e753a0912272b9/images/Pasted%20image%2020250721211837.png)

We follow what it says right behind : 
![](https://github.com/Kaalig/CTFLearn-Writeups/blob/d407f6e185c0db1af480898eb6e753a0912272b9/images/Pasted%20image%2020250721211917.png)

I changed the 03 to 05 and had found the flag :

![](https://github.com/Kaalig/CTFLearn-Writeups/blob/d407f6e185c0db1af480898eb6e753a0912272b9/images/Pasted%20image%2020250721212114.png)

Don't forget to render the image in cyberchef.
