# Category : Web

## Baby Web

![web](https://github.com/sachin320/The-CyberGrabs-CTF/blob/main/Chall%20Img/img/web_chall.PNG)

So when you follow the url you will redirected to the Blank webpage which has written

```
Welcome Buddy :)
You Know How to get it :)
```
But When you open the network tab and reload the webpage you got hex value stored in the cookie 

![network](https://github.com/sachin320/The-CyberGrabs-CTF/blob/main/Chall%20Img/img/baby_web_network.PNG)  

```
6d2c4f667040764e4d525a2e602e4953312c51684e2829476225597374454f6f692c2a614d28247b5123692e3a6d4b73

```

Decode it and you will get Base91 Encoded data

```
m,Ofp@vNMRZ.`.IS1,QhN()Gb%YstEOoi,*aM(${Q#i.:mKs

```
As i released the hint for this challenge so the players can get they will getting base encoded data  

![hint](https://github.com/sachin320/The-CyberGrabs-CTF/blob/main/Chall%20Img/img/web_hint.PNG)

After Decode the Base91 you will get the Flag for Baby Web Challenge 

Flag : ```cybergrabs{v3ryyy_3asy_f0r_y0u_i_gu3ss}```
