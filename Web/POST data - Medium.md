**POST data - Medium - 40 Pts**

Challenge : *This website requires authentication, via POST. However, it seems as if someone has defaced our site. Maybe there is still some way to authenticate ? http://165.227.106.113/post.php*



Another Web challenge. By clicking on the link we get to this. I immediately checked the source code, and then found some crendentials :

![](https://github.com/Kaalig/CTFLearn-Writeups/blob/364aeb1ad13c436beff73c967f50e8d58badc2f3/images/Pasted%20image%2020250824232049.png)

POST here suggest that we're talking about POST Method. In order to send data via POST or PUT we can use the command : `curl`
We're gonna use this command such as this template : 

![](https://github.com/Kaalig/CTFLearn-Writeups/blob/364aeb1ad13c436beff73c967f50e8d58badc2f3/images/Pasted%20image%2020250824232535.png)

where we input the credentials in the -d value, one for username, one for password :

![](https://github.com/Kaalig/CTFLearn-Writeups/blob/364aeb1ad13c436beff73c967f50e8d58badc2f3/images/Pasted%20image%2020250824232956.png)

and just like that, we got the flag.
