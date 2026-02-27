# Level Goal
The password for the next level is stored somewhere on the server and has all of the following properties: \
owned by user bandit7 \
owned by group bandit6 \
33 bytes in size \
# Solution 
Terminal : \
1. find / -type f -user bandit7 -group bandit6 -size 33c 2>/dev/null \
   / - Searches from root (entire server) \
   -user - search for user
   -group - search for group
   2>/dev/null - ignore denied permission \
<img width="948" height="103" alt="image" src="https://github.com/user-attachments/assets/3cf0ef60-b373-4255-a1e3-be54974d2e85" /> \
2.open file \
<img width="752" height="85" alt="image" src="https://github.com/user-attachments/assets/fa82cbd5-aedc-423e-a542-2ec265616af0" /> \
3.ssh bandit7@bandit.labs.overthewire.org -p 2220 \
 Password: morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj \
<img width="310" height="122" alt="image" src="https://github.com/user-attachments/assets/f3649cb1-a65d-4f5d-a80f-cbde5bf5d58c" /> \
ACCESS GRANTED.
