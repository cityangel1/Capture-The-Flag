# CHALLENGE
Password:yZdkjAYZRd3R7tq7T5kXMjMJlOIkzDeB \
Username: natas12 \
URL:      http://natas12.natas.labs.overthewire.org
# SOLUTION
1.Login. \
<img width="961" height="412" alt="image" src="https://github.com/user-attachments/assets/0b202af9-bef6-43af-850e-d0770fb2a842" /> \
2.View Source code. \
<img width="963" height="933" alt="image" src="https://github.com/user-attachments/assets/f2decc51-0a17-4941-bb15-26a57b04e565" /> \
3.The Vulnerability Explained. \
 - This level exploits a client-side control failure. While the webpage has an upload form that visually restricts you to JPEG files, the actual security check is not happening on the server.
 - Looking at the backend source code available in the challenge, you can see the upload logic. It uses a hidden HTML input field named MAX_FILE_SIZE and relies on the file extension in the filename to determine where to save the upload. By manipulating this filename, you can force the server to save your PHP file with the correct .php extension, allowing it to be executed \
   
4.Exploitation Guide
 - Step 1: Create a PHP Web Shell
   First, create a simple PHP script that the server will execute to read the password for the next level. Save the following code as shell.php:
   php
   <?php echo shell_exec("cat /etc/natas_webpass/natas13"); ?>
 - Step 2: Open Developer Tools
 - Step 3: Find and Edit the Hidden Field
   <input type="hidden" name="filename" value="some_random_string.jpg">
   <img width="974" height="543" alt="image" src="https://github.com/user-attachments/assets/909d2e21-4398-4493-a9d8- d7706109477c" />
   This hidden field controls the name under which the server will save your uploaded file.
   Double-click the value attribute and change the extension from .jpg to .php. The name itself doesn't matter, only     the extension does. It should look like this:
   html
   <img width="291" height="88" alt="image" src="https://github.com/user-attachments/assets/c86c6d52-0cf6-403a-a053-10d3e80f2f10" />
 - Step 4: Upload the PHP File
   Now, use the "Browse" button to select your shell.php file and click the Upload File button. The server will save     your file on the disk using the name you specified in the hidden field (e.g., random_name.php).
 - Step 5: Access the Uploaded File
   After a successful upload, the page will provide a link to your uploaded file, like http://natas12.natas.labs.overthewire.org/upload/random_name.php. Click this link.
 <img width="608" height="116" alt="image" src="https://github.com/user-attachments/assets/01b67fa4-c325-4ac2-a94b-73c53fb39ebd" /> \

# Flag: trbs5pCjCrkuSknBBKHhaBxq6Wm1j3LC
