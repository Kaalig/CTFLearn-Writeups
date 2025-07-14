**Git is good - Forensics - 30 Pts**

Challenge : 

*The flag used to be there. But then I redacted it. Good Luck. https://mega.nz/#!3CwDFZpJ!Jjr55hfJQJ5-jspnyrnVtqBkMHGJrd6Nn_QqM7iXEuc*

After downloading the file, we unzip it. After investigating briefly the directory, i found nothing except that proof tht the flag was redacted.

![](https://github.com/Kaalig/CTFLearn-Writeups/blob/7383bec2da7155e2630191e1a8e34f62052a9bf1/images/Pasted%20image%2020250714210916.png)

I forgot that a git directory is always hidden. 
First of, i check for the commit logs to see who and what changed : 

![](https://github.com/Kaalig/CTFLearn-Writeups/blob/7383bec2da7155e2630191e1a8e34f62052a9bf1/images/Pasted%20image%2020250714211137.png)


The earliest commit is made onto the master branch, this is fishy. Let's focus on the commit of `flag.txt` with this command : `git log -p -- flag.txt` : 

![](https://github.com/Kaalig/CTFLearn-Writeups/blob/7383bec2da7155e2630191e1a8e34f62052a9bf1/images/Pasted%20image%2020250714211411.png)
