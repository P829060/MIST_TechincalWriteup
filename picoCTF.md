# picoCTF Challs

# 1. Cryptography

## Susbtitution0 
  A message has come in but it seems to be all scrambled. Luckily it seems to have the key at the beginning. Can you crack this substitution cipher?
  Download the message [Click here for the challenge](https://play.picoctf.org/practice/challenge/307?category=2&page=2)
## Solving
  Pretty simple way to solve it. It's just that you require a deciphering tool or use frequency analysis on a website as they have mentioned. I used a deciphering tool. The last line in the file allows us to solve it easily because
  you can guess what it means - "The flag is picoCTF{.....}". Looking at the cipher, it looks like a subtitution cipher. You can use a tool that can guess what kind of cipher it is, but i didnt use it in this case because substituting the 
  letters using the last line in other parts of the cipher gave a meaningful message in this case. I used the quipqiup tool, a cryptogram solver [Click here for that link](https://quipqiup.com/). So that's it, put it in there, get the         answer. :)
## Flag
  > picoCTF{5UB5717U710N_3V0LU710N_357BF9FF}
