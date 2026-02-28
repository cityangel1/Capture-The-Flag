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
THAT WE ARE SUPPOSED TO USE A KEY.WELL HERE IT IS. \ 
4.Tool:ssh \
5.Command: ssh -i sshkey.private bandit14@localhost -p 2220 \
ssh - because we need to use it as a shell. \
-i - use a file. \
-i sshkey.private - file to use \
bandit14@localhost -p 220 - You guessed it right,we wand to do sshing in an ssh.But as a differnt user. \
<img width="940" height="183" alt="image" src="https://github.com/user-attachments/assets/b61c4f0f-1a04-455d-935b-17c9a49d865b" /> \

