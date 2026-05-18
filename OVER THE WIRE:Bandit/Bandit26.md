# Level Goal
Logging in to bandit26 from bandit25 should be fairly easy… The shell for user bandit26 is not /bin/bash, but something else. Find out what it is, how it works and how to break out of it.
# Solution
1.Login. \
2.check contents:ls -la \
<img width="868" height="316" alt="image" src="https://github.com/user-attachments/assets/e1903fba-2e20-4198-bff6-d72fd57472ff" /> \
3.login to bandit 26 with the key at localhost:
 <img width="923" height="705" alt="image" src="https://github.com/user-attachments/assets/b0b0693d-65de-4734-ac0c-207a8d9cb993" /> \
 it disconnected us immidiately. \
4.Know what shell is running: cat /etc/passwd | grep bandit26 \
 <img width="947" height="87" alt="image" src="https://github.com/user-attachments/assets/97fde528-706d-4cf4-aea8-6937ea1babbe" /> \
5.Check Contents of file: cat /usr/bin/showtext \
  - <img width="608" height="212" alt="image" src="https://github.com/user-attachments/assets/705c8e5b-062a-4ea0-97b2-acf64e16b19c" /> \
  - It runs more and exits
  - The more command pauses when the output is longer than the screen height. We can use this to get a shell!
6.NOW LETS THINK:
 -Login to bandit26 using the private key
    -scp -P 2220 bandit25@bandit.labs.overthewire.org:/home/bandit25/bandit26.sshkey .
    -chmod 600 bandit26.sshkey
    -ssh -i bandit26.sshkey bandit26@bandit.labs.overthewire.org -p 2220
    -<img width="952" height="429" alt="image" src="https://github.com/user-attachments/assets/73b6f35f-e93d-4b15-bf3f-a79dcb3dcdc3" />
    -WE are immediately logged out
 -Resize it so only ~5–10 lines are visible(THE SCREEN)
 -Then re-run:ssh -i bandit26.sshkey bandit26@bandit.labs.overthewire.org -p 2220
 -<img width="756" height="152" alt="image" src="https://github.com/user-attachments/assets/797b9886-06eb-4bd0-85a6-2376ed4e21f9" />
 -Press v (lowercase) → opens the file in vim
          -In vim:
                -Type :set shell=/bin/bash then Enter
                -Type :shell then Enter
<img width="534" height="125" alt="image" src="https://github.com/user-attachments/assets/a1e10bf2-e30d-4760-9b89-5d71ec4df71a" /> \
7.GET PASSWORD:cat /etc/bandit_pass/bandit26 \
Password bandit26 :s0773xxkk0MXfdqOfPRVr9L3jJBUOgCZ
<img width="676" height="177" alt="image" src="https://github.com/user-attachments/assets/1c5a37ba-df38-4dd3-8ee0-22583bdea563" />
# WHAT A CONCEPT!!



