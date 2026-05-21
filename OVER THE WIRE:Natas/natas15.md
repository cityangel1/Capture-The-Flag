# CHALLENGE
Password:SdqIqBsFcz3yotlNYErZSZwblkm0lrvx \
Username: natas15 \
URL:      http://natas15.natas.labs.overthewire.org
# SOLUTION
1.Login \
<img width="960" height="339" alt="image" src="https://github.com/user-attachments/assets/bd8e2799-95f9-423c-877f-67b7d3cfc00e" /> \
2.View source code. \
<img width="962" height="862" alt="image" src="https://github.com/user-attachments/assets/2abb266c-05c7-43a6-bbca-cc6b7edf05c3" /> \
3.Interpretation.
 - The server checks if a user exists.
 - But it doesn't sanitize,big mistake
 - THIS IS BLIND SQL INJECTION.THE NOTORIUS TYPE OF SQLI.
 - Looking at the source code it says there is a users table and has two columns,username and password.Though its commented
 - THe way to do this is to guess every character of the password.we are talking  of thousands of combinations.we even have to check the length of the password first

4.Inject. \
First check a valid username. \
<img width="449" height="212" alt="image" src="https://github.com/user-attachments/assets/5458ab3a-9d9e-4d5f-9e80-8a6cb1b82ab4" /> \
<img width="609" height="188" alt="image" src="https://github.com/user-attachments/assets/75472925-1ca4-4f9c-aae2-17fe610adc20" /> \
Tried some ,,but natas16 is the one i found. \
Second,Inject. \
 - <img width="802" height="294" alt="image" src="https://github.com/user-attachments/assets/f9dca912-c31f-44f4-99fc-984740a7b38f" />
 - CHANGE OF PLANS,LETS USE BASH.IT HAS THE BEST DEBUGGING UTILITIES.
 - <img width="613" height="796" alt="image" src="https://github.com/user-attachments/assets/a1808774-3209-445c-b5d7-e7c3dbd6245a" />
 - <img width="901" height="953" alt="image" src="https://github.com/user-attachments/assets/8ccf34d8-d894-495c-96be-9e64a18805e4" /> \

# Flag : hPkjKYviLQctEW33QmuXL6eDVfMW4sGo
 


