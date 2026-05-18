# Level Goal
There is a setuid binary in the homedirectory that does the following: it makes a connection to localhost on the port you specify as a commandline argument. It then reads a line of text from the connection and compares it to the password in the previous level (bandit20). 
If the password is correct, it will transmit the password for the next level (bandit21).
# Solution
1.Login:Similar prottocol follows. \
2.Pretend you are a fool(Ofcourse you are not) and run the binary without any arguments. \
./suconnect \
<img width="939" height="148" alt="image" src="https://github.com/user-attachments/assets/c4b1b28f-fb48-478f-88df-6b4a569eaca5" /> \
3.Now we need to set a listener so that our setuid can connect to. \
So we use netcat to do it. \
echo "0qXahG8ZjOVMN9Ghs7iOWsCfZyXOUbYO" | nc -l -p 12345 & \
-l - listen mode \
-p 12345 - the port to connect,you can use any but avoid well known ports. \
& - allows us to use the same terminal for listening and connecting.well unless you want to use another terminal there wont be any need for this. \
4.Connect to localhost: \
./suconnect 12345 \
<img width="954" height="177" alt="image" src="https://github.com/user-attachments/assets/b55d020e-399f-4dfe-8c7d-a5178760e791" /> \
Password for bandit21 :EeoULMCra2q0dSkYj561DX7s1CpBuOBt

