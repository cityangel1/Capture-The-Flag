# CHALLENGE
Access next level's password,Given: \
Username: natas4 \
URL:      http://natas4.natas.labs.overthewire.org \
Password: QryZXc2e0zahULdHrtHxzyYkj59kUxLQ
# SOLUTION
1.Login \
<img width="961" height="411" alt="image" src="https://github.com/user-attachments/assets/251310b6-3b8c-4541-9b5e-4cd4c4d3b0a3" /> \
2.VIew page source. \
<img width="955" height="331" alt="image" src="https://github.com/user-attachments/assets/58cc843b-fefd-4633-9409-513b3b0a05bb" /> \
3.Something is off.But it says "authorised users are allowed from natas5".THats a hint.THat means that the referer should be : \
http://natas5.natas.labs.overthewire.org/ \
4.Open terminal: \
    - WE need to change the referer using the following curl command. \
    -THe syntax is : curl -u "username:password" -H "Referer:Referer_name" <target> \
    - curl -u natas4:QryZXc2e0zahULdHrtHxzyYkj59kUxLQ \
     -H "Referer: http://natas5.natas.labs.overthewire.org/" \
     http://natas4.natas.labs.overthewire.org/
<img width="1002" height="789" alt="image" src="https://github.com/user-attachments/assets/b1242475-8b7a-451a-a85d-eccff5cd50fc" />
# Flag : 0n35PkggAPm2zbEpOU802c0x0Msn1ToK



