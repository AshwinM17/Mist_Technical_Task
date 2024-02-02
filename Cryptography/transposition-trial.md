# Transposition-trial
## Description
Our data got corrupted on the way here. Luckily, nothing got replaced, but every block of 3 got scrambled around! The first word seems to be three letters long, maybe you can use that to recover the rest of the message.
Download the corrupted message here.
## Hint:
1) Split the message up into blocks of 3 and see how the first block is scrambled
## data given
heTfl g as iicpCTo{7F4NRP051N5_16_35P3X51N3_V6E5926A}4
## Approach
On dividing into blocks of three 
```
'heT','fl ','g a','s i','icp','CTo','{7F','4NR','P05','1N5','_16','_35','P3X','51N','3_V','6E5','926','A}4'
```
in each block 3rd letter should be moved to 1st place thus we obtain the flag
## flag
The flag is picoCTF{7R4N5P051N6_15_3XP3N51V3_56E6924A}
