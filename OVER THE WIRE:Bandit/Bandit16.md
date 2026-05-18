# Level Goal
The password for the next level can be retrieved by submitting the password of the current level to port 30001  \
on localhost using SSL/TLS encryption. \
# Solution
ASSUMPTION: YOU ALREADY LOGGED IN TO BANDIT15 USING PASSWORD FROM PREVIOUS EXERCISE. \
HEAR THIS: nc and telnet are used where security is of no concern \
But when security comes in and encryption is to be used,thats where OPENSSL comes in. \
COMMAND: openssl s_client -quiet -connect localhost:30001 \
s_client - acts as a tls client initiating a handshake \
-connect localhost:30001 - where to connect \
<img width="942" height="340" alt="image" src="https://github.com/user-attachments/assets/dd8520e7-3e7c-41f0-bed0-4235f83a55bb" /> \
Password:kSkvUpMQ7lBYyCM4GBPvCvT1BfWRy0Dx \
