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
> 19704762736204164635843

### 2) Inferius Prime
Here is my super-strong RSA implementation, because it's 1600 bits strong it should be unbreakable... at least I think so!
[Click here for the challenge](https://cryptohack.org/challenges/rsa/)

### Solving
This required basic RSA formulae implementation like:

-   a ^ b % c | pow(a,b,c) in python
-   cipher = msg ^e % N
-   N = p * q
-   d = e ^(-1) mod [(p-1) * (q-1)]
-   msg = cipher ^ d % N '''
  
![Inferius Prime](https://github.com/P829060/MIST_TechincalWriteup/blob/abcdbcfaf0cfab819f4c5819b0e0d29853f86f11/images/inferius%20whatever%20primes.png)

Python Code As Follows:
``` from Crypto.Util.number import long_to_bytes
n = 984994081290620368062168960884976209711107645166770780785733
e = 65537
ct = 948553474947320504624302879933619818331484350431616834086273
p = 848445505077945374527983649411 
q = 1160939713152385063689030212503
d = pow(e,-1,(p-1)*(q-1))
pt = pow(ct,d,n)
print(long_to_bytes(pt))
```

### Flag
> crypto{N33d_b1g_pR1m35}
