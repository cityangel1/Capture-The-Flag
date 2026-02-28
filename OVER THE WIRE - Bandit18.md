# Level Goal
There are 2 files in the homedirectory: passwords.old and passwords.new.  \
The password for the next level is in passwords.new and is the only line that has been changed between passwords.old and passwords.new
# Solution
REMEMBER THE FILE YOU MADE PREVOUSLY. \
1. chmod 600 bandit17_key.private
2. ssh -i bandit17_key.private bandit17@bandit.labs.overthewire.org -p 2220 \
3. ls \
   <img width="369" height="93" alt="image" src="https://github.com/user-attachments/assets/dd65b0d0-fb51-4926-a6ab-c665cda1d668" /> \
4. Tool:diff ]
   diff passwords.new passwords.old \
      <img width="650" height="153" alt="image" src="https://github.com/user-attachments/assets/63bbed7c-7ac7-4235-96e7-afa980fb123c" /> \
   Password for bandit 18 :pGozC8kOHLkBMOaL0ICPvLV1IjQ5F1VA

