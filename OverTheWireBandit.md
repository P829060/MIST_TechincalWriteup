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

# Level 2 Of Bandit (Acquiring Password for level 3)

level 2
username: bandit2
pass: 263JGJPfgU6LtdEvgfWU1XP5yac29mFx

This is again the **cat** command. This time it's spaces in the filename, so just use two double quotation marks after the cat command and then mention the file name with spaces within the the double quotation marks. Again nothing much 
special here.

![Level 2 pics](https://github.com/P829060/LinuxLuminariumAndBandit/blob/19779c5d9e0891e88a60e9a6a35239237d5fe9ad/Screenshot%202024-12-13%20122805.png)

# Level 3 Of Bandit (Acquiring Password for level 4)

level 3
username: bandit3
pass: MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx

Here we had to go to a particular directory and find a file. But yes the fun part was, if you use **ls** command to list the files, it doesn't list anything in the directory. You can use **find** command which allows you to search for files and directories based on various criteria such as name, size, type, and modification date. When i used the command without , it showed me the directory name and the files listed in it, from there I found the file which was hiding in the directory. I didn't mention any specifics, just used the find command and the directory name as argument. Yeah i had problem with reading the file after getting to know it, but then i figured it out.

![Level 3 pics](https://github.com/P829060/LinuxLuminariumAndBandit/blob/d4bb098cbd1d5763507c4247eabe0b2287da5c56/Screenshot%202024-12-13%20124030.png)

# Level 4 Of Bandit (Acquiring Password for level 5)

level 4
username: bandit4
pass: 2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ

A VERY PAINFUL process of reading every file to see which is human-readable. Maybe there is a command to know if a file is human-readable or not, but yeah i went with reading every file through **cat** command. As you can see -file07 is an ascii text file when i read its contents and it is much more similar to passwords for the levels than the others. You can also use **find -readable** which is much easier but then my first line of thought was as below. So i went with it.

![Level 4 pics](https://github.com/P829060/LinuxLuminariumAndBandit/blob/348c76215d301c4c4a0663a07824c038d53b076b/Screenshot%202024-12-13%20130013.png)

# Level 5 Of Bandit (Acquiring Password for level 6)

level 5
username: bandit5
pass: 4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw

I can't **cat** through all those directories and their files, so i had to find an alternative way to get it. I did think of using **du** command to see disk usage but then i read that, by 9.6M they mean megibytes or something and not megabytes. So i wasted time thinking its megabytes and saw every file size but couldn't find a file with 1033 bytes. Later i realized it's wrong. So then i used the **find -readable 1033c ! -executable** where c means bytes and ! is basically "not", so a not executable file. So yeah did that, got the file with the password.(Yeah because of hurry, i did cd instead of cat 2 times before realizing it).

![Level 5 pics](https://github.com/P829060/LinuxLuminariumAndBandit/blob/f2ea7b7379d69299e964f0e8a354bb5a58ddd997/Screenshot%202024-12-14%20105806.png)

# Level 6 Of Bandit (Acquiring Password for level 7)

level 6
username: bandit6
pass: HWasnPhtq9AVKe0dmk45nxy20cvUa6EG

Here we again use the find command but we also search for specific things, like the user who owns it, which group owns it and its size. Giving **find / -user bandit7 -group bandit6 -size33c** searches file which meets the requirements as well as specifies if the file can be accessed by us or not. As some files require you to be the root user or atleast a part of the group where users of that group have been given access to read files by the root user. Well there is only file that we can read, and i have highlighted it, so that you neednot search where it is. So use the **cat** command with the filename and read the file for the password of the next level.

![Level 6 pics](https://github.com/P829060/LinuxLuminariumAndBandit/blob/8c6f3a1f91fd033d1b2b1e7628ea0cf01fc7432e/Screenshot%202024-12-14%20110247.png)
![Level 6 pics](https://github.com/P829060/LinuxLuminariumAndBandit/blob/8c6f3a1f91fd033d1b2b1e7628ea0cf01fc7432e/Screenshot%202024-12-14%20110404.png)
![Level 6 pics](https://github.com/P829060/LinuxLuminariumAndBandit/blob/8c6f3a1f91fd033d1b2b1e7628ea0cf01fc7432e/Screenshot%202024-12-14%20110428.png)

# Level 7 Of Bandit (Acquiring Password for level 8)

level 7
username: bandit7
pass: morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj

This level is easy if you know the **grep** command. You can search for a specific word using this command. Some might not understand its significance for the first time, as who will actually write so many lines? But there is a chance like this challenge, where there is almost 1,000 lines of text in a file and you might take an eternity to solve it. So yeah i realised it's importance during this challenge. So yeah **grep (your word to search) (filename)** will print the entire line that contains the word you mentioned.

![Level 7 pics](https://github.com/P829060/LinuxLuminariumAndBandit/blob/f5c78565025c501c9d55afc96d86a72134eeb166/Screenshot%202024-12-15%20084816.png)

# Level 8 Of Bandit (Acquiring Password for level 9)

level 8
username: bandit8
pass: dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc



![Level 8 pics](https://github.com/P829060/LinuxLuminariumAndBandit/blob/a1c84bbecdeeb7200db9c87815bf45707c4ecfa8/Screenshot%202024-12-15%20222234.png)

# Level 9 Of Bandit (Acquiring Password for level 10)

level 9
username: bandit9
password: 4CKMh1JI91bUIZZPXDqGanal4xvAg0JM

### I have shown 2 ways here:

### 1st Way:

![Level 9 pics](https://github.com/P829060/LinuxLuminariumAndBandit/blob/d6c51fe6fb16f9ce5bea6f5e55dace54de5e5ee1/Screenshot%202024-12-15%20222351.png)
![Level 9 pics](https://github.com/P829060/LinuxLuminariumAndBandit/blob/d6c51fe6fb16f9ce5bea6f5e55dace54de5e5ee1/Screenshot%202024-12-15%20222411.png)
![Level 9 pics](https://github.com/P829060/LinuxLuminariumAndBandit/blob/d6c51fe6fb16f9ce5bea6f5e55dace54de5e5ee1/Screenshot%202024-12-15%20222444.png)
![Level 9 pics](https://github.com/P829060/LinuxLuminariumAndBandit/blob/d6c51fe6fb16f9ce5bea6f5e55dace54de5e5ee1/Screenshot%202024-12-15%20222456.png)

### 2nd Way:

![Level 9 pics](https://github.com/P829060/LinuxLuminariumAndBandit/blob/d6c51fe6fb16f9ce5bea6f5e55dace54de5e5ee1/Screenshot%202024-12-15%20222512.png)

# Level 10 Of Bandit (Acquiring Password for level 11)

level 10
username: bandit10
pass: FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey

![Level 10 pics](https://github.com/P829060/LinuxLuminariumAndBandit/blob/4b9254e56f055d4f8d4e05c031a1e6bb6d822090/Screenshot%202024-12-15%20222745.png)

# Level 11 Of Bandit (Acquiring Password for level 12)

level 11
username: bandit11
pass: dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr

![Level 11 pics](https://github.com/P829060/LinuxLuminariumAndBandit/blob/c64f459d5f0072b916237d16980fb7b037aabafe/Screenshot%202024-12-15%20222820.png)

# Level 12 Of Bandit (Acquiring Password for level 13)

level 12
username: bandit12
pass: 7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4

![Level 12 pics]()

didn't continue after this: 

level 13
username; bandit13
pass: FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn
