# Level Goal
The password for the next level is stored in /etc/bandit_pass/bandit14 and can only be read by user bandit14.  \
For this level, you don’t get the next password, but you get a private SSH key that can be used to log into the next level.  \
Look at the commands that logged you into previous bandit levels, and find out how to use the key for this level. \
# Solution
1. First ,,always list the files present. \
2. see contents of files. \
 <img width="816" height="753" alt="image" src="https://github.com/user-attachments/assets/25de0fbf-150e-4de6-941f-d80b309eeaa2" /> \
<img width="817" height="240" alt="image" src="https://github.com/user-attachments/assets/b23e1ca5-57c8-4a2f-ad62-38e05fb400e2" /> \
3.AS YOU CAN SEE:ITS AN RSA KEY(CRYPTOGRAPHIC KEY),SO WHAT?,GOOD THING WE DONT HAVE DEMENTIA,,WE REMEMBER FROM THE LEVEL DESCRIPTION \
THAT WE ARE SUPPOSED TO USE A KEY.WELL HERE IT IS.  \ 
4.Tool:scp ,ssh \
Now you might be asking yourself whats scp? \
its used to copy contents of an ssh system into your local machine. \
   FOR MORE INFO: scp -h \
TERMINAL : \
5.exit - come out of the bandit session.  \
6. scp -P 2220 bandit13@bandit.labs.overthewire.org:sshkey.private . \
   -P 2220 - the port to connect to. make sure its caps. \
   bandit13@bandit.labs.overthewire.org:sshkey.private - the file we want to copy. \
   . - mean we copy the file into our working folder on our local machine. \
<img width="946" height="480" alt="image" src="https://github.com/user-attachments/assets/cfd617ee-ccb7-465e-ba2b-0c2831a7cabb" /> \
7.Modify file permissions: chmod 600 sshkey.private \
8.ssh -i sshkey.private -p 2220 bandit14@bandit.labs.overthewire.org \
-i sshhkey.private - means the file to use for auth purposes. \
<img width="437" height="100" alt="image" src="https://github.com/user-attachments/assets/6df5b62d-eb51-4bf6-8042-f5b02a11a790" /> \
9. view the file contents:cat /etc/bandit_pass/bandit14 \
10. <img width="625" height="117" alt="image" src="https://github.com/user-attachments/assets/430372a2-dde5-42a2-a342-f7ca227d93f4" /> \
    THRILLED.

12. Password:MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS

