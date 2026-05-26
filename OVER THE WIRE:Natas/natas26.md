# CHALLENGE
ACCESS NEXT LEVEL'S PASSWORD \
GIVEN: \
Password:cVXXwxMS3Y26n5UZU89QgpGmWCelaQlE \
Username: natas26 \
URL:      http://natas26.natas.labs.overthewire.org
# SOLUTION
1.Login \
<img width="958" height="337" alt="image" src="https://github.com/user-attachments/assets/cdf62e29-b2dd-4bf3-9968-8f8dc23f3a88" /> \
2.View source code \
<img width="959" height="926" alt="image" src="https://github.com/user-attachments/assets/a07a937b-60e2-4879-9520-20fc8030aafb" /> \
3.Interprete
  - This is a PHP object injection / unsafe deserialization challenge.
  - The vulnerability is:
   - unserialize(base64_decode($_COOKIE['drawing']))
   - The application unserializes user-controlled data from a cookie.
  - A class contains a dangerous destructor like:
   - function __destruct() {
   - file_put_contents($this->filename, $this->img);
   - }
  - This lets you:
   - create arbitrary files
   - write PHP code into the web directory
   - execute commands through a webshell

4.Solve
 - WE WILL USE A PYTHON SCRIPT TO DO OUR DIRTY WORK
    - The script creates a malicious serialized PHP Logger object that abuses unsafe unserialize() behavior in OverTheWire Natas Natas26.
    - It sets:
     - logFile → where the shell gets written (img/pwn.php)
     - initMsg + exitMsg → pieces of PHP code that become a working webshell.
    - The payload is Base64-encoded because the application expects the drawing cookie in serialized Base64 format.
Using Python requests, the script sends the malicious cookie to trigger PHP object deserialization and file creation automatically.
    - Finally, it accesses the generated shell with:
     - ?cmd=cat /etc/natas_webpass/natas27
     - to execute a command and retrieve the next password.
 - <img width="946" height="864" alt="image" src="https://github.com/user-attachments/assets/a69627e2-c204-4505-b372-baaa8b4d4b2f" />
 - <img width="500" height="378" alt="image" src="https://github.com/user-attachments/assets/7acd5920-5a72-4871-a587-68759b8f4fc4" />

# Flag : u3RRffXjysjgwFU6b9xa23i6prmUsYne






