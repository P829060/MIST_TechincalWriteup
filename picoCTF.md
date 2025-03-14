# picoCTF Challs

## 1. Cryptography

### 1) Susbtitution0 
  A message has come in but it seems to be all scrambled. Luckily it seems to have the key at the beginning. Can you crack this substitution cipher?
  Download the message. [Click here for the challenge](https://play.picoctf.org/practice/challenge/307?category=2&page=2)
### Solving
  Pretty simple way to solve it. It's just that you require a deciphering tool or use frequency analysis on a website as they have mentioned. I used a deciphering tool. The last line in the file allows us to solve it easily because
  you can guess what it means - "The flag is picoCTF{.....}". Looking at the cipher, it looks like a subtitution cipher. You can use a tool that can guess what kind of cipher it is, but i didnt use it in this case because substituting the 
  letters using the last line in other parts of the cipher gave a meaningful message in this case. I used the quipqiup tool, a cryptogram solver [Click here for the tool](https://quipqiup.com/). So that's it, put it in there, get the         answer. :)
### Flag
  > picoCTF{5UB5717U710N_3V0LU710N_357BF9FF}

### 2) Substitution1
  A second message has come in the mail, and it seems almost identical to the first one. Maybe the same thing will work again.
  Download the message here. [Click here for the challenge](https://play.picoctf.org/practice/challenge/308?category=2&page=2)
### Solving
  Same as the previous one, nothing much to stress upon. Use the tool, get the answer the way mentioned before. [Click here for the tool](https://quipqiup.com/)
### Flag
  > picoCTF{FR3QU3NCY_4774CK5_4R3_C001_4871E6FB}

### 3) Substitution2
  It seems that another encrypted message has been intercepted. The encryptor seems to have learned their lesson though and now there isn't any punctuation! Can you still crack the cipher?
  Download the message. [Click here for the challenge](https://play.picoctf.org/practice/challenge/309?category=2&page=2)
### Solving
  You can use the quipqiup tool again but because of punctuation not being there, the tool might enable patristocrat mode, just change it to solve using statistics, which will give the flag in the correct format at the end of the 
  paragraph. [Click here for the tool](https://quipqiup.com/)
### Flag
  > picoCTF{N6R4M_4N41Y515_15_73D10U5_702F03FC}

### 4) la cifra de
  I found this cipher in an old book. Can you figure out what it says? Connect with nc jupiter.challenges.picoctf.org 58295
### Solving
  This required a seperate tool because the previous tool wasn't as great as this one at solving. I used boxentriq website [Click here for website](https://www.boxentriq.com/). First, you can use any tool on website for identifying which 
  type of cipher it is. You can use dcode website [Click here for the website](https://www.dcode.fr/cipher-identifier). After identifying which cipher, (in this case it was Vignere Cipher) use boxentriq website and autosolve the cipher 
  on the website. The autosolved website shows the **keys** it used. If you already found the proper flag format with autosolve, then that's your answer, However, if it could'nt find the proper key, check the keys used and try doing a 
  trial error method of what the key can be. I got a mix of the words **flag**, so i used it as key and turns out that it's the actualy correct key for the cipher. So that's the way you can solve this chall.
### Flag
  > picoCTF{b311a50_0r_v1gn3r3_c1ph3ra966878a}

### 5) Waves Over Lambda
  We made a lot of substitutions to encrypt this. Can you decrypt it? Connect with nc jupiter.challenges.picoctf.org 43522.
### Solving 
  This was a bit confusing at first about the flag format, later found it out that you are only supposed to put text inside the curly braces of the flag. First you put this in a cipher decoder to know what type of cipher it is like 
  mentioned above for dcode website. Later you can use planetcalc website, to autocheck for the key [Click here for link](https://planetcalc.com/8047/) . This gives the decoded cipher and you get the flag mentioned specifically by the 
  text.
### Flag
  > FREQUENCY_IS_C_OVER_LAMBDA_OGFMAUNRAF 
  ##### Weird that the prompt says to write picoCTF{} but the hint suggests otherwise which is the way it accepts the flag as mentioned above
### 6) Pixelated
  I have these 2 images, can you make a flag out of them? [Click for link to challenge](https://play.picoctf.org/practice/challenge/100?category=2&page=3)
### Solving
  Tried this through normal web-based tools. But, stacking these images always failed for some reason, even when taking either of the 2 as reference. So i had to get a python code, to merge these 2 images and then print the new png of 
  the 2 combined scrambled pngs. The code is as follows
  ```
from PIL import Image # pip install Pillow
img1 = Image.open("scrambled1.png")
pixels1 = img1.load()
img2 = Image.open("scrambled2.png")
pixels2 = img2.load()

flag = Image.new("RGB" ,img1.size)
flagpix = flag.load()
for row in range(img1.size[1]):
     for col in range(img1.size[0]):
           flagpix[col,row]=(
                        (pixels1[col,row][0]+pixels2[col,row][0])%256,
                        (pixels1[col,row][1]+pixels2[col,row][1])%256,
                        (pixels1[col,row][2]+pixels2[col,row][2])%256)
flag.save("flag.png")
```
### Flag
  > picoCTF{2a4d45c7}
