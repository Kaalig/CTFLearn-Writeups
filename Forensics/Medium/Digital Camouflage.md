**Digital Camouflage - Forensics - 40 Pts** 

Challenge :

*We need to gain access to some routers. Let's try and see if we can find the password in the captured network data: https://mega.nz/#!XDBDRAQD!4jRcJvAhMkaVaZCOT3z3zkyHre2KHfmkbCN5lYpiEoY Hint 1: It looks like someone logged in with their password earlier. Where would log in data be located in a network capture?<br /> Hint 2: If you think you found the flag, but it doesn't work, consider that the data may be encrypted.
Credit: picoCTF 2017*

So we got everything covered in the challenge. Basically a .pcap file, and because of the hints, we now it's somewhere in the http stream : 

![](https://github.com/Kaalig/CTFLearn-Writeups/blob/c03169b2bff35acd2a6acce7b4778ce534a4f173/images/Pasted%20image%2020250720210439.png)

Here we go, we got the password that is a bit encrypted and it returned this (it's a flag don't worry, I took 1 hour to understand that THIS is our flag even though it's a RAW string) :

![](https://github.com/Kaalig/CTFLearn-Writeups/blob/c03169b2bff35acd2a6acce7b4778ce534a4f173/images/Pasted%20image%2020250720211752.png)
