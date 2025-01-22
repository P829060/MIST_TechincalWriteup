# Over The Wire Levels 0 to 12

## My Experience 

I would like to say that it was really informative and doing it actually introduced me to various ciphers ( one level had ROT 13 and so when i searched for it, i found various other ciphers like caeser cipher, vigenere cipher etc. ). I do like to take part in future CTF's and feel the happiness of actually solving it. However, the 12 levels isn't enough to make it through a CTF (which is obvious). The only bad part is that you have to keep searching for documentation and its uses which isn't bad but some people on the internet with their half baked knowledge can mislead us into thinking some things are correct. The documentation that OTW provides is too long. I mean i get that we have to learn the documentation, but we can't remember all of them and it doesn't highlight what's important to know. In that case, Linux Luminarium does a great job of teaching us what's important and what's not. It's not that it's bad but i think they can be more specific on what to learn or what's important for us to know. Needless to say, i did enjoy a lot solving the levels. This feels much closer to a CTF exposure as it teaches basic linux commands, which can help in CTF challenges. Thanks a lot for providing us with these resourceful and helpful websites where we can increase our knowledge not only for CTF's but also basic cmd or cli commands :) .

# Level 0 Of Bandit (Acquiring Password for level 1)

level 0
username: bandit0
pass: bandit0

This level says how we can read the contents of the file on the cli, that is through the **cat** command.
(Yeah i know there is a lot of unimportant stuff but that is just me trying to figure out commands and stuff like what does the **file** command do, what does **data** do etc.....)

![Level 0 pics](https://github.com/P829060/LinuxLuminariumAndBandit/blob/315d4ca3bb6e51dd54dbb8afdb973ab790753485/Screenshot%202024-12-13%20120654.png) 
![level 0 pics](https://github.com/P829060/LinuxLuminariumAndBandit/blob/54eac5764041c392d9994c46ab544c130641a07e/Screenshot%202024-12-13%20120720.png)

# Level 1 Of Bandit (Acquiring Password for level 2)

level 1
username: bandit1
pass: ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If

This level required us to read a file which had a name "-" which can't be done directly. Because "-" in linux is used to take input from user, so just putting "-" wont do anything. To mention it as a file you need to use either of the 
two commands mentioned below in the photo, i.e, **cat < -** or **cat ./-** which gives you the password for the next level. Again it's the cat command you require to read the file, so nothing special here except to read a file that has
hyphen as the start letter of the filename.

![level 1 pics](https://github.com/P829060/LinuxLuminariumAndBandit/blob/4a707a78f20fbc862c4f3fe7ec4d276f29b59fea/Screenshot%202024-12-13%20120816.png)
![level 1 pics](https://github.com/P829060/LinuxLuminariumAndBandit/blob/4a707a78f20fbc862c4f3fe7ec4d276f29b59fea/Screenshot%202024-12-13%20120856.png)


