# repetitions
## Description
Can you make sense of this file?
Download the file here.
## data provided
VmpGU1EyRXlUWGxTYmxKVVYwZFNWbGxyV21GV1JteDBUbFpPYWxKdFVsaFpWVlUxWVZaS1ZWWnVh
RmRXZWtab1dWWmtSMk5yTlZWWApiVVpUVm10d1VWZFdVa2RpYlZaWFZtNVdVZ3BpU0VKeldWUkNk
MlZXVlhoWGJYQk9VbFJXU0ZkcVRuTldaM0JZVWpGS2VWWkdaSGRXCk1sWnpWV3hhVm1KRk5XOVVW
VkpEVGxaYVdFMVhSbHBWV0VKVVZGWmFWMDVHV2tkYVNHUlZDazFyY0ZkVWJGWlhZVlpLU0dWRlZs
aGkKYlRrelZERldUMkpzUWxWTlJYTkxDZz09Cg==
## Hints:
1)Multiple decoding is always good.

## Approach
Noticed the == sign at the end which suggeststhat this is base64 encoded

Thus on one by one piping base64 decoder we can obtain the flag
## Commands
```
cat enc_flag |base64 -d |base64 -d |base64 -d | base64 -d| base64 -d  |base64 -d 
```
ie after 6 times base64 decoding we get the flag
## flag
```
picoCTF{base64_n3st3d_dic0d!n8_d0wnl04d3d_de523f49}

```