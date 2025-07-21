**A CAPture of a FLag - Forensics - 50 Pts**

Challenge :

*This isn't what I had in mind, when I asked someone to capture a flag... can you help? You should check out WireShark. https://mega.nz/#!3WhAWKwR!1T9cw2srN2CeOQWeuCm0ZVXgwk-E2v-TrPsZ4HUQ_f4*

So we already know it's a pcap file (packet capture file), which means we're going do dig in this using Wireshark.

![](https://github.com/Kaalig/CTFLearn-Writeups/blob/297722a9c8e726254ff210cd6ab8301f0dc7a52c/images/Pasted%20image%2020250720201741.png)

There's roughly 7000 entries. Generally speaking, I want to understand what is going on, and the first thing I read is the HTTP and the info part precisely :

![](https://github.com/Kaalig/CTFLearn-Writeups/blob/297722a9c8e726254ff210cd6ab8301f0dc7a52c/images/Pasted%20image%2020250720200955.png)

I really just started and found the flag encoded in a HTTP request because of the suspicious info : there is a query with "msg" and some encoded gibberish characters. Got quite lucky on this one : 

![](https://github.com/Kaalig/CTFLearn-Writeups/blob/297722a9c8e726254ff210cd6ab8301f0dc7a52c/images/Pasted%20image%2020250720202355.png)

