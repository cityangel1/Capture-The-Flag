# CHALLENGE
GET NEXT LEVELS PASSWORD,GIVEN: \
Password: EqjHJbo7LFNb8vwhHb9s75hokh5TF0OC \
Username: natas17 \
URL:      http://natas17.natas.labs.overthewire.org
# SOLUTION
1.Login \
<img width="962" height="367" alt="image" src="https://github.com/user-attachments/assets/a4fad9a3-ee58-4856-b0d4-87df549fd09a" /> \
2.View source code \
<img width="783" height="495" alt="image" src="https://github.com/user-attachments/assets/818db66f-a27e-4577-8536-6239f1abba7e" /> \
3.The Vulnerability \
 - When you enter a username, the application runs this query :
  - SELECT username FROM users WHERE username = '[your input]';
 - If the username exists, it shows "This user exists".
 - If it doesn't exist, it shows "This user doesn't exist".
 - However, in Natas17, the developers removed the output messages — the page always looks the same. So you get zero feedback about whether your injection worked or not.
 - This forces you to use time-based techniques.
 - The Key Technique: Time-Based Blind SQLi
 - You can inject a condition that makes the database SLEEP() for a few seconds if true.
 - Example payload:
   - natas17" AND IF(1=1, SLEEP(5), 0) --
   - natas17" AND IF((SELECT SUBSTRING(password,1,1) FROM users WHERE username='natas18')='a', SLEEP(5), 0) --
  - If the first character of natas18's password is 'a', the page will take ~5 seconds to load.
  - If not, it loads instantly.
  - By measuring response time, you can infer true/false answers.

4.Solve \
AGAIN WE USE AN AUTOMATED SCRIPT. \
<img width="885" height="307" alt="image" src="https://github.com/user-attachments/assets/1aa54f2e-1803-4237-af82-776325b613a8" /> \
You will wait like a century for it to finish. \
<img width="726" height="289" alt="image" src="https://github.com/user-attachments/assets/bed9c215-a6d4-41d4-857a-0f0a2183d2ce" /> \
# Flag : 6OG1PbKdVjyBlpxgD4DDbRG6ZLlCGgCJ



 
 

