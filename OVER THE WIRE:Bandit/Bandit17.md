# Level Goal
The credentials for the next level can be retrieved by submitting the password of the current level to a port on localhost in the range 31000 to 32000. First find out which of these ports have a server listening on them. Then find out which of those speak SSL/TLS and which don’t. \
There is only 1 server that will give the next credentials, the others will simply send back to you whatever you send to it.
# Solution
1.Discover open ports: use nmap \
<img width="930" height="316" alt="image" src="https://github.com/user-attachments/assets/99c3dd29-81ad-420f-9c69-6b7fbf3ca4b1" /> \
2.Know the services running: use nmap \
<img width="954" height="750" alt="image" src="https://github.com/user-attachments/assets/4e852a9c-93c4-454a-8062-2c56a49f596c" /> \
CONCLUSION: ITS either 31518 or 31790. \
3.NOW USE openssh to connect. \
Commands: openssl s_client -quiet -connect localhost:31518  \
          <img width="833" height="251" alt="image" src="https://github.com/user-attachments/assets/a395f7fd-270f-4134-85c9-173a705fc4ff" /> \
           openssl s_client -quiet -connect localhost:31790 \
           <img width="932" height="942" alt="image" src="https://github.com/user-attachments/assets/cea832a7-7ac2-45bc-adf2-1398d8580a17" /> \
Final: COPY THE RSA KEY TO LOCAL MACHINE. \
CTRL+SHIFT+C - nano bandit17_key.private(local machine) - paste code - save - CLAP FOR YOURSELF, YOU DID IT.

