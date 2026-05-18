# Level Goal
The password for the next level is stored in the file data.txt, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under /tmp in which you can work. \
Use mkdir with a hard to guess directory name. Or better, use the command “mktemp -d”. Then copy the datafile using cp, and rename it using mv (read the manpages!) \
# Solution
1.Make a directory: mktemp -d \
2.cd to directory: \
<img width="536" height="112" alt="image" src="https://github.com/user-attachments/assets/e4276e94-96bf-4274-94f7-75eb80d97e72" /> \
3.MY ADVICE : WORK SMART,NOBODY CARES OF THE EFFORT ,JUST THE RESULTS. \
Definetely there is going to be multiple compressions. \
You might be asking Yourself "So what are you suggesting?". \
Write a Script that does everything for you. \
<img width="827" height="366" alt="image" src="https://github.com/user-attachments/assets/0f6ba6ef-55ed-4fa6-bfcb-d0f35232510c" /> \
Make it executable. \
Command : chmod +x solve.sh \
Run it. \
Command: ./solve.sh \
<img width="959" height="413" alt="image" src="https://github.com/user-attachments/assets/c3c82de2-2dc3-4448-b114-5b09d5bb8254" /> \
4.LOGIN:
ssh bandit13@bandit.labs.overthewire.org -p 2220 \
Password:FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn \
Damn that was Good. \
Find Attached bash Script that does everything for you. \
[solve.sh](https://github.com/user-attachments/files/25607721/solve.sh)
