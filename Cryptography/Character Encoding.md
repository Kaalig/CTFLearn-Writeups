**Character Encoding - Crypto - 20 Pts**

Challenge :

*In the computing industry, standards are established to facilitate information interchanges among American coders. Unfortunately, I've made communication a little bit more difficult. Can you figure this one out? 41 42 43 54 46 7B 34 35 43 31 31 5F 31 35 5F 55 35 33 46 55 4C 7D*



So basically, we only have to decode this string of character that looks like Hexadecimal encoding.

There's 2 methods that popped in my mind for this exercice : 
- 1. Using CyberChef and simple convert from Hexadecimal. You can see the flag directly.
 
  ![](https://github.com/Kaalig/CTFLearn-Writeups/blob/f651f6f4d3cd93c007e0b683dac8be64cf84374f/images/Pasted%20image%2020250624000637.png)

  - 2. Manually decrypting using the ASCII Table. For each symbol that we can see on our computer, we can also write those symbols in decimal, octal, binaries and hexadecimal because of a international standardisation of the ASCII Table over the year such as  :
   
  ![](https://github.com/Kaalig/CTFLearn-Writeups/blob/f651f6f4d3cd93c007e0b683dac8be64cf84374f/images/Pasted%20image%2020250624001151.png)

  Just find the HEX number that correlates with the symbol and applies it manually, that's it !

  *Note : ASCII is pretty much not used at all in 2025. In fact, UTF-8, who's the big dog in town for a decade or more now, is used by 95% of people around the globe.*
