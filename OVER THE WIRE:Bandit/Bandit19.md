# Level Goal
The password for the next level is stored in a file readme in the homedirectory. Unfortunately, someone has modified .bashrc to log you out when you log in with SSH.
# Solution
1.Login:ssh -p 2220 bandit18@bandit.labs.overthewire.org \
<img width="634" height="104" alt="image" src="https://github.com/user-attachments/assets/ebd5596b-339c-4636-b4a9-faab846e2995" /> \
Immediatelly logod out. \
2.Bypass timeout. \
The only way to do that is to attach the command in our ssh connect command. \
3.ssh -p 2220 bandit18@dandit.labs.overthewire.org "ls" : see files \
<img width="858" height="335" alt="image" src="https://github.com/user-attachments/assets/2a9a0545-8154-4b71-9376-ac293062d601" /> \
4.ssh -p 2220 bandit18@dandit.labs.overthewire.org "cat readme" : SEE details \
<img width="926" height="337" alt="image" src="https://github.com/user-attachments/assets/019d3cd8-bc0a-47d1-8099-ed0b49b0f2a9" /> \
Password for bandit 19: cGWpMaKXVwDUNgPAVJbWYuGHVn9zl3j8



