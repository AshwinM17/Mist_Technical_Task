# mini rsa
## Description
Let's decrypt this: ciphertext? Something seems a bit small.
## Data given

N: 29331922499794985782735976045591164936683059380558950386560160105740343201513369939006307531165922708949619162698623675349030430859547825708994708321803705309459438099340427770580064400911431856656901982789948285309956111848686906152664473350940486507451771223435835260168971210087470894448460745593956840586530527915802541450092946574694809584880896601317519794442862977471129319781313161842056501715040555964011899589002863730868679527184420789010551475067862907739054966183120621407246398518098981106431219207697870293412176440482900183550467375190239898455201170831410460483829448603477361305838743852756938687673

e: 3

ciphertext (c): 2205316413931134031074603746928247799030155221252519872649649212867614751848436763801274360463406171277838056821437115883619169702963504606017565783537203207707757768473109845162808575425972525116337319108047893250549462147185741761825125 

## Hints
1) RSA tutorial
2) How could having too small an e affect the security of this 2048 bit key?
3) Make sure you don't lose precision, the numbers are pretty big (besides the e value)
## SOLUTION
We are given large values for N(=p*q) and C(Cipher Text).but e is small<br>
as e is 3 .we can check by cubing and adding the cipher text and converting to ascii and check if 'pico' is there or not.

The script aims to find the padding value by iterating over a range of possible values of k from 0 to 9,999.
For each k, it performs a calculation to reverse the encryption operation, effectively computing m as the e-th(3rd) root of (k * N + c). This operation undoes the RSA encryption and extracts the padded message.
The result m is then converted to ASCII using the int_to_ascii function.
If the string "pico" is found in the ASCII representation of m, it means the correct padding has been found, and the value of k is recorded as the padding.
The loop breaks when the correct padding is found.

we had even set the precision to 700 so that no error is present
so we get the flag and padding=0
## Flag
Flag: picoCTF{n33d_a_lArg3r_e_606ce004}

## RSA Algorithm
RSA algorithm uses the following procedure to generate public and private keys:
Select two large prime numbers, p and q.
Multiply these numbers to find **n = p x q,** where n is called the modulus for encryption and decryption.
Choose a number e less than n, such that n is relatively prime to (p - 1) x (q -1). It means that e and (p - 1) x (q - 1) have no common factor except 1. Choose "e" such that 1<e < φ (n), e is prime to φ (n),
gcd (e,d(n)) =1
If n = p x q, then the public key is <e, n>. A plaintext message m is encrypted using public key <e, n>. To find ciphertext from the plain text following formula is used to get **ciphertext C**.<br>
**C = m<sup>e</sup> mod n**<br>
Here, m must be less than n. A larger message (>n) is treated as a concatenation of messages, each of which is encrypted separately.
To determine the private key, we use the following formula to calculate the d such that:<br>
**D<sub>e</sub> mod {(p - 1) x (q - 1)} = 1**
Or **D<sub>e</sub> mod φ (n) = 1**<br>
The private key is <d, n>. A ciphertext message c is decrypted using private key <d, n>. To calculate plain text m from the ciphertext c following formula is used to get plain text m.
m = c<sup>d</sup> mod n