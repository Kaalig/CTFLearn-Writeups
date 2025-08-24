**Basic Injection - 30Pts - Easy**

Challenge : *See if you can leak the whole database using what you know about SQL Injection...*



Basically what we deal with is SQL because of the syntax : `SELECT * FROM webfour.webfour where name='$input'`

And we need to leak the whole database..

The easiest way to do it is by using the most knowed payload in existence : `' OR 1=1` which is always a true statement so it always work on theory. If the app is not sanitized at all, it should return everything there is.

![](https://github.com/Kaalig/CTFLearn-Writeups/blob/e4e31abd6aa45ffb73821488f3b5d0f293ff1f8d/images/Pasted%20image%2020250824231625.png)

Well it didn't, but it is expected. I like to mess with this payload a bit before moving on, becaause it can always be a typo problem. And it was absolutely this, by the way : 

![](https://github.com/Kaalig/CTFLearn-Writeups/blob/e4e31abd6aa45ffb73821488f3b5d0f293ff1f8d/images/Pasted%20image%2020250824231746.png)
