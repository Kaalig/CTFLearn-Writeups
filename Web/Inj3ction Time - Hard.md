**Inj3ction Time - Web - 100 Pts**


Challenge : *I stumbled upon this website: http://web.ctflearn.com/web8/ and I think they have the flag in their somewhere. UNION might be a helpful command*


Alright so they give us one website and a hint about using a UNION SQLi statement. I am quite bad at SQL Injection but we will try it. First of all, im gonna use some common true statement to see if it responds something. After 3-4 minutes I simply used a `1 OR 1=1` and found some more informations :

![](https://github.com/Kaalig/CTFLearn-Writeups/blob/b584ef62b5d0a31b97c5f7718eac37776a081a16/images/Pasted%20image%2020250825220755.png)

I'm also pretty sure that the database reject every `'` I try to input purely by the fact that `1 OR 1=1` gave us info but `1' OR 1=1` doesn't work.

Anyway, we get some more information. Because we're going to use an UNION statement, we need to find how much columns there is to apply our payload.
Most simple use of finding columns is to use `UNION SELECT NULL` and increment `NULL` in the request until it shows something different.


![](https://github.com/Kaalig/CTFLearn-Writeups/blob/b584ef62b5d0a31b97c5f7718eac37776a081a16/images/Pasted%20image%2020250825221159.png)


One `NULL` give us nothing but **4** `NULL` ? : 
![](https://github.com/Kaalig/CTFLearn-Writeups/blob/da99e0e13eec82c17d74f2a8d48beb4fec6b90f3/images/Pasted%20image%2020250825221513.png)

Note : *Be careful to put a space after the comma, otherwise the query doesn't work. I did spent 20 minutes to find what was my problem to the point of almost finding another way of completing the challenge*

So we know the order of the column. We know it's strings after strings in every column. If it is in MySQL, it should react at this detect version query : `SELECT @@version` (same for Microsoft db)
Just change a NULL value for @@version and you'll see that it is indeed a MySQL database : 

![](https://github.com/Kaalig/CTFLearn-Writeups/blob/c4a11513924ca1650557d5a1d35765ece9a6f66a/images/Pasted%20image%2020250825222040.png)

by querying this line of code : `1 UNION SELECT NULL, table_name, NULL, NULL from information_schema.tables` give us ALL the informations for a SPECIFIC table.


![](https://github.com/Kaalig/CTFLearn-Writeups/blob/da99e0e13eec82c17d74f2a8d48beb4fec6b90f3/images/Pasted%20image%2020250825222603.png)


In all the database, this is a name for a flag, FOR SURE. Let's check this out by applying : `1 UNION SELECT * FROM w0w_y0u_f0und_m3

Unfortunately it didn't worked, and I miserably had to find the answer to this problem after 20 more minutes of suffering.

So basically by just appending this line (our name table in the same position as our last query + FROM the same table) `1 UNION SELECT NULL, f0und_m3, NULL, NULL FROM w0w_y0u_f0und_m3`:
![](https://github.com/Kaalig/CTFLearn-Writeups/blob/da99e0e13eec82c17d74f2a8d48beb4fec6b90f3/images/Pasted%20image%2020250825222908.png)
