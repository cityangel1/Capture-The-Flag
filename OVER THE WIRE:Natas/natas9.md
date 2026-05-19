# CHALLENGE 
Username: natas9 \
Password : ZE1ck82lmdGIoErlhQgWND6j2Wzz6b6t \
URL:      http://natas9.natas.labs.overthewire.org
# SOLUTION
1.Login. \
<img width="968" height="373" alt="image" src="https://github.com/user-attachments/assets/3f56ec35-af89-40f4-abaa-ced2071f6050" /> \
2.View source code. \
<img width="960" height="699" alt="image" src="https://github.com/user-attachments/assets/7b65ff64-8361-4477-8cea-6dbdb019bcd1" /> \
INTERPRETATION:
  - 
  -<img width="964" height="998" alt="image" src="https://github.com/user-attachments/assets/54de50f6-f84a-4975-9ff9-b80da282f234" /> \
  -There is a dictionary file. \
  -Most importantly,the command takes an input and executes the command.Lets think out of the world,we can inject a command
  to get the password of the next level.since we know it might be at /etc/natas_webpass/natas10.
3.Command injection. \
 Command = natas ; cat /etc/natas_webpass/natas10 \
 <img width="968" height="664" alt="image" src="https://github.com/user-attachments/assets/456c6562-5858-43da-b8d3-59b72ef1b78c" />
# FLAG : t7I5VHvpa14sJTUGV0cbEsbYfFP2dmOu



