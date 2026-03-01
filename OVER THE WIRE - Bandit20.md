# Level Goal
To gain access to the next level, you should use the setuid binary in the homedirectory. Execute it without arguments to find out how to use it.
The password for this level can be found in the usual place (/etc/bandit_pass), after you have used the setuid binary.
# Solution
1. LOgin using credentials obtained in previous session. \
2. know about setuid binary. \
   ls -l \
   <img width="816" height="221" alt="image" src="https://github.com/user-attachments/assets/14935c97-02cf-4ae8-a91e-0b60c4140257" /> \
   ./bandit20-do \
   <img width="449" height="114" alt="image" src="https://github.com/user-attachments/assets/63c3be25-f8ae-4d4d-829f-697f5cb42519" /> \
   <img width="509" height="95" alt="image" src="https://github.com/user-attachments/assets/e08b74e6-e71a-458a-8e9a-694ef073ca03" /> \
   THATS THE HINT:ITS BANDIT2O \
3.Open file using the file: ./bandit20-do cat /etc/bandit_pass/bandit20 \
Password for Bandit20:0qXahG8ZjOVMN9Ghs7iOWsCfZyXOUbYO \
<img width="750" height="85" alt="image" src="https://github.com/user-attachments/assets/f57bc730-4f5c-4cb4-bc86-31085f59d6be" /> \


