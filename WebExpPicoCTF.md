# WebExp PicoCTF Challs

## 1) Don't use client side
Can you break into this super secure portal? https://jupiter.challenges.picoctf.org/problem/17682/ (link) or http://jupiter.challenges.picoctf.org:17682
[Click here for the challenge](https://jupiter.challenges.picoctf.org/problem/17682/)

### Solving 
This was pretty simple. You just inspect and if you check html, you will see that it authenticates the password based on the string. So arrange the string according to how they have mentioned it 
(meaning according to the substring checking).<br>
![Solving img](https://github.com/P829060/MIST_TechincalWriteup/blob/6dcea96fd8653fecefb1c1ba5b6b7795744e13bf/images/dont-use-client-side%20chall%20solving%20photo.png)  
<br> So you finally get the flag **picoCTF{no_clients_plz_b706c5}**

### Flag
> picoCTF{no_clients_plz_b706c5}

## 2) IntroToBurp
Additional details will be available after launching your challenge instance.
[Click here for the challenge](https://play.picoctf.org/practice/challenge/419?category=1&page=1&search=Intro)

### Solving 
You Require Burp Suite Community Edition for this. You just intercept the request being sent to the server. Register with random info, doesn't matter. 2fa authentication asks for an otp. Enter a random number or anything and intercept the request being sent to the server. When you intercept it, remove the entire otp = (whatever you wrote) line. This will bypass the otp checking and you get the flag. In my case i had also intercepted the responses, which isn't required in this case. Just intercept the requests sent and you are good to go. <br>

![Burp suite img with sol after intercepting and sending the request](https://github.com/P829060/MIST_TechincalWriteup/blob/e15c954c1ad076dd89bbd62033986d984d5e2d71/images/IntroToBurp%20chall.png)

<br> So this is what you get: **Welcome, bruh you sucessfully bypassed the OTP request. Your Flag: picoCTF{#0TP_Bypvss_SuCc3$S_3e3ddc76}**

### Flag
> picoCTF{#0TP_Bypvss_SuCc3$S_3e3ddc76}


