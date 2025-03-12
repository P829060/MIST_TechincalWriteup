# picoCTF Challs

# 1. Cryptography

## 1) Susbtitution0 
  A message has come in but it seems to be all scrambled. Luckily it seems to have the key at the beginning. Can you crack this substitution cipher?
  Download the message. [Click here for the challenge](https://play.picoctf.org/practice/challenge/307?category=2&page=2)
## Solving
  Pretty simple way to solve it. It's just that you require a deciphering tool or use frequency analysis on a website as they have mentioned. I used a deciphering tool. The last line in the file allows us to solve it easily because
  you can guess what it means - "The flag is picoCTF{.....}". Looking at the cipher, it looks like a subtitution cipher. You can use a tool that can guess what kind of cipher it is, but i didnt use it in this case because substituting the 
  letters using the last line in other parts of the cipher gave a meaningful message in this case. I used the quipqiup tool, a cryptogram solver [Click here for the tool](https://quipqiup.com/). So that's it, put it in there, get the         answer. :)
## Flag
  > picoCTF{5UB5717U710N_3V0LU710N_357BF9FF}

## 2) Substitution1
  A second message has come in the mail, and it seems almost identical to the first one. Maybe the same thing will work again.
  Download the message here. [Click here for the challenge](https://play.picoctf.org/practice/challenge/308?category=2&page=2)
## Solving
  Same as the previous one, nothing much to stress upon. Use the tool, get the answer the way mentioned before. [Click here for the tool](https://quipqiup.com/)
## Flag
  > picoCTF{FR3QU3NCY_4774CK5_4R3_C001_4871E6FB}

## 3) Substitution2
  
