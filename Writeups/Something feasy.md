# Category : Crypto

## Something feasy

![chall](https://github.com/sachin320/The-CyberGrabs-CTF/blob/main/Chall%20Img/img/Something%20Feasy.PNG)

In this challenge first you got the [file](https://github.com/sachin320/The-CyberGrabs-CTF/blob/main/Chall%20file/feasy.txt)

It has Encrypted text  and as its description says

```Key to unlock anything is already with you ```

So if u apply Xor decryption on it you with the key as ```key``` you can get the decrypted text like this 

```
Are You Sure You Used Correct Key : ^$#^^&###$&$#$&!^&&&%f&@#*^*&^^f^f#^#^@f#&^$&!^a^##(#&^d&@#$@f^a#%&(^#^(^##^^&#(&!#$^%@b

```
Now if you look at the hint given in the challenge 

![pic](https://github.com/sachin320/The-CyberGrabs-CTF/blob/main/Chall%20Img/img/feasy%20hint.PNG)

So As hint says keyboard wil help so if you look at the keyboard you will get that it was alphanumberic Characters you have to replace them by digits 

so i just write a quick simple script for this 

```
s = "^$#^^&###$&$#$&!^&&&%f&@#*^*&^^f^f#^#^@f#&^$&!^a^##(#&^d&@#$@f^a#%&(^#^(^##^^&#(&!#$^%@b"
l = len(s)


i = 0

while i<l:
    if(s[i] == '!'):
        print("1" , end='')
    elif(s[i] == '@'):
        print("2", end='')
    elif(s[i] == '#'):
        print("3", end='')
    elif(s[i] == '$'):
        print("4", end='')
    elif(s[i] == '%'):
        print("5", end='')
    elif(s[i] == '^'):
        print("6", end='')
    elif(s[i] == '&'):
        print("7", end='')
    elif(s[i] == '*'):
        print("8", end='')
    elif(s[i] == '('):
        print("9", end='')
    elif(s[i] == ')'):
        print("0", end='')
    else:
        print(s[i], end='')

    i = i+1
   ```
After Running this script you will get the hex value 

```
643667333474347167775f723868766f6f36362f3764716a6339376d72342f6a35796369633667397134652b

```

After Decode it online you will get the another Encoded Cipher 

```
d6g34t4qgw_r8hvoo66/7dqjc97mr4/j5ycic6g9q4e+
 
```
Now if you remeber the hint we need keyboard once again so basically it was a Keyboard Shift [Cipher](https://www.dcode.fr/keyboard-shift-cipher)
after Decoding it you will get 

```cybergrabs{fin4llyy0ucam3ou7fr0mth3k3yboard}```

Seperate each Word By _ and you have your final flag 
```
Flag : cybergrabs{fin4lly_y0u_cam3_ou7_fr0m_th3_k3yboard}

```
