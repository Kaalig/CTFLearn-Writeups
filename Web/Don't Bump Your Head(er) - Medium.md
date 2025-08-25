**Don't Bump Your Head(er) - Web - 40 Pts**


Challenge : *Try to bypass my security measure on this site! http://165.227.106.113/header.php*


So we have a webpage we can't see because of our user agent. A user-Agent is the browser used to arrive to the webpage. This suggest that we need to have the correct user agent to input and the only information we got besides this message is a comment.

![](https://github.com/Kaalig/CTFLearn-Writeups/blob/7dab1cd27822bcaf034d3c0560e64e55732e0522/images/Pasted%20image%2020250825223739.png)

Why not testing it as a user-agent then ? :
![](https://github.com/Kaalig/CTFLearn-Writeups/blob/7dab1cd27822bcaf034d3c0560e64e55732e0522/images/Pasted%20image%2020250825224202.png)

It partially worked. But at least we know what to do. It asks for a "referer" , which is a header to see from what **website** (and not browser/OS on this one) you came from. We just have to input this referer in our command :


![](https://github.com/Kaalig/CTFLearn-Writeups/blob/7dab1cd27822bcaf034d3c0560e64e55732e0522/images/Pasted%20image%2020250825224309.png)

Bingo !
