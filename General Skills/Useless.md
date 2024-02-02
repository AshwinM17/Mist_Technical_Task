# useless
## Description
There's an interesting script in the user's home directory
Additional details will be available after launching your challenge instance
## Given:
```
Hostname: saturn.picoctf.net
Port:     57884
Username: picoplayer
Password: password
```
## commands 
```
ssh picoplayer@saturn.picoctf.net -p 57884 
man useless
```
## Approach
On catting the useless file we can observe shell script for for a basic calculator ,which prompts us to read the manual when we dont enter any of the valid functions

On opening the manual by
```
man useless
```
we get the flag in the authors section of the manual
## Flag
```
picoCTF{us3l3ss_ch4ll3ng3_3xpl0it3d_5136}```