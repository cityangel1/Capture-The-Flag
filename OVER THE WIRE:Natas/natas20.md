# TASK
Find natas21 password. \
Given Login Credentials: \
Password: p5mCvP7GS2K6Bmt3gqhM2Fc1A5T8MVyw \
Username: natas20 \
URL:      http://natas20.natas.labs.overthewire.org
# sOLUTION
1.Login \
<img width="960" height="405" alt="image" src="https://github.com/user-attachments/assets/32d09946-7ef7-4359-8eeb-054ff6f6f8e4" /> \
2.View source code. \
<img width="959" height="886" alt="image" src="https://github.com/user-attachments/assets/8d548a04-1b65-41de-8cb6-80397717111b" /> 
3.Understanding
 - This level uses PHP Session Serialization.
 - When you enter a name, it saves your name + a flag (admin=0) into the session file.
 - The goal is to trick the server so that when it reads the session, admin=1.
 - Vulnerability: You can inject a newline (%0A) into the "name" field to break the session format and inject admin 1. 

4.EXploit. \
I will use a scipt.I will attach it,Appreciate programming. \
<img width="483" height="668" alt="image" src="https://github.com/user-attachments/assets/8876efa1-fbcd-4989-80c1-18dda7a6708d" /> \
<img width="664" height="275" alt="image" src="https://github.com/user-attachments/assets/d909adea-e80a-47cf-bfd8-0ee4cbe17470" /> 
# Flag: BPhv63cKE1lkQl04cE5CuFTzXe15NfiH



