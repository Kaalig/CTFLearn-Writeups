**Milk's best friend - Forensics - 40 Pts**

Challenge :

*There's nothing I love more than oreos, lions, and winning. https://mega.nz/#!DC5F2KgR!P8UotyST_6n2iW5BS1yYnum8KnU0-2Amw2nq3UoMq0Y 
Have Fun :)*


So we download the MEGA file that is an image. Because it's an image I instantly use `exiftool` to find more informations. Unfortunately no success :

![](https://github.com/Kaalig/CTFLearn-Writeups/blob/22cb03429f3bc111239cfe81fe392472718d44b8/images/Pasted%20image%2020250624222234.png)

I, then use binwalk because maybe there's another file in the file, you never know. 

![](https://github.com/Kaalig/CTFLearn-Writeups/blob/22cb03429f3bc111239cfe81fe392472718d44b8/images/Pasted%20image%2020250624222318.png)

A RAR archive ! Perfect for us ! 

![](https://github.com/Kaalig/CTFLearn-Writeups/blob/22cb03429f3bc111239cfe81fe392472718d44b8/images/Pasted%20image%2020250624222521.png)
![](https://github.com/Kaalig/CTFLearn-Writeups/blob/22cb03429f3bc111239cfe81fe392472718d44b8/images/Pasted%20image%2020250624222541.png)

So we have multiples files from the rar archive. I didn't find anything in all of the files besides 'b.jpg'
By appyling `strings` to the `b.jpg` we come across this :

![](https://github.com/Kaalig/CTFLearn-Writeups/blob/22cb03429f3bc111239cfe81fe392472718d44b8/images/Pasted%20image%2020250624222808.png)
![](https://github.com/Kaalig/CTFLearn-Writeups/blob/22cb03429f3bc111239cfe81fe392472718d44b8/images/Pasted%20image%2020250624222820.png)


In full plain-text, couldn't hope for more :)
