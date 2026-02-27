# Level Goal
The password for the next level is stored in the file data.txt, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions \
# Solution
My Thoughts : This is crazy,I think its Ceasar ciphertext. \
Guess what: it is. 
Hint: Tool: tr
Command: cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m' \
<img width="766" height="176" alt="image" src="https://github.com/user-attachments/assets/158bd990-95b8-4061-bb17-e57b3dcb05df" /> \
The password is 7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4 \
Login: ssh bandit12@bandit.labs.overthewire.org -p 2220 \
<img width="305" height="96" alt="image" src="https://github.com/user-attachments/assets/bb5fcb04-3b1b-4ac5-b0be-9a8320f26742" /> \
# CALL ME GENIUS
