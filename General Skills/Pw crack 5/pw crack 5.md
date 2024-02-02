# PW Crack 5
## Description
Can you crack the password to get the flag?
Download the password checker here and you'll need the encrypted flag and the hash in the same directory too. Here's a dictionary with all possible passwords based on the password conventions we've seen so far.
## Hints:
1) Opening a file in Python is crucial to using the provided dictionary.
2) You may need to trim the whitespace from the dictionary word before hashing. Look up the Python string function, strip
3) The str_xor function does not need to be reverse engineered for this challenge.
## Given
dictionary.txt with a blank space in front of each password 
## Approach
we want to check each of the 65500+ possible passwords 
We can do this by altering the code to automatically check all the password.

We had to add a for loop which check each line using file reader in python and used the strip function which removes the trailing spaces
## Flag:
```
Welcome back... your flag, user:
picoCTF{h45h_sl1ng1ng_40f26f81}
```