# CryptoHack Challs

## PRIMES PART 1

### 1) Factoring
Factorise the 150-bit number 510143758735509025530880200653196460532653147 into its two constituent primes. Give the smaller one as your answer.
[Click here for the challenge](https://cryptohack.org/challenges/rsa/)

### Solving 
I had to use a website tool [Click here for the website](https://factordb.com/index.php?query=). This generated 2 prime factors of the given number. From this, I selected the smallest among them and that was the required flag.

Alternate Solution:
You can even use a python code (which i found online and seems easier to implement).
Refer the image below:
![Python Code](https://github.com/P829060/MIST_TechincalWriteup/blob/5acefd2ecba7b992f2df71170f4e637553bf0690/images/FactoringPrimesPythonCode.png)

### Flag
The flag was 
> 19704762736204164635843
