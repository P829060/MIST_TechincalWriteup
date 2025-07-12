# WebExp PicoCTF Challs

## 1) Don't use client side
Can you break into this super secure portal? https://jupiter.challenges.picoctf.org/problem/17682/ (link) or http://jupiter.challenges.picoctf.org:17682
[Click here for the challenge](https://jupiter.challenges.picoctf.org/problem/17682/)

### Solving 
This was pretty simple. You just inspect and if you check html, you will see that it authenticates the password based on the string. So arrange the string according to how they have mentioned it 
(meaning the substring checking)
![Solving img](https://github.com/P829060/MIST_TechincalWriteup/blob/6dcea96fd8653fecefb1c1ba5b6b7795744e13bf/images/dont-use-client-side%20chall%20solving%20photo.png)  
<br> So you finally get the flag **picoCTF{no_clients_plz_b706c5}**

### Flag
> picoCTF{no_clients_plz_b706c5}
