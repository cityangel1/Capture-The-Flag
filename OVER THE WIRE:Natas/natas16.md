# CHALLENGE
Password: \
Username: natas16 \
URL:      http://natas16.natas.labs.overthewire.org 
# SOLUTION
1.Login \
<img width="956" height="393" alt="image" src="https://github.com/user-attachments/assets/c57d7b12-1f86-4c1e-93f9-b6b70cd11ba4" /> \
2.View Source code \
<img width="909" height="685" alt="image" src="https://github.com/user-attachments/assets/5a1c42c8-1cd1-4b77-af77-945180473a8e" /> \
3.Interpretation
 - an advanced blind injection vulnerability
 - The server sanitizes some special characters.
 - so we cannot use our previous script to brute force the password
 - now since it a blind injection,we cant display the password in the website.
 - so we craft a script that escapes the sanited special characters
 - the script should search a name from the dictionary and add an injection that greps the password for natas17
 - we can then check whether what character belongs to the password for each index untill we get the whole password.
 - Thats why we need an automated script because manual work is tiresome,come on this is 2026,not the time when manual work was important in building the pyramids in egypt.
 - lets use the script.

4.THE SCRIPT \
<img width="523" height="662" alt="image" src="https://github.com/user-attachments/assets/6f88da44-072f-4642-b4bc-f7ee51c64e74" /> \
PLEASE TAKE YOUR TIME TO TRY AND UNDERSTAND THE CODE. \
<img width="914" height="981" alt="image" src="https://github.com/user-attachments/assets/242f53c9-f53f-438c-a389-d29a9a89eb5b" />
# Flag: EqjHJbo7LFNb8vwhHb9s75hokh5TF0OC





