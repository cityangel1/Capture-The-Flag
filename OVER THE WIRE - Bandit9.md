# Level Goal
The password for the next level is stored in the file data.txt and is the only line of text that occurs only once
# Solution
Hint: Use uniq tool - used to identify unique lines. \
    : use sort tool - used to like "group" common items together. \
    :Pipe the two. \
THerefore: \
Command: sort data.txt | uniq -u \
<img width="520" height="139" alt="image" src="https://github.com/user-attachments/assets/e291f881-01cb-468f-a9bb-3299dcd6e3e8" /> \
Final step: Login \
ssh bandit9@bandit.labs.overthewire.org -p 2220 \
Password:4CKMh1JI91bUIZZPXDqGanal4xvAg0JM \
<img width="523" height="177" alt="image" src="https://github.com/user-attachments/assets/eda02f75-94bf-4ae6-bf47-20cef1b77ffe" /> \

