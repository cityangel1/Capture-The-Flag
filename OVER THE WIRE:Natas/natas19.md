# CHALLENGE
GET NEXT PASSWORD. \
GIVEN: \
Password: tnwER7PdfWkxsG4FNWUtoAZ9VyZTJqJr \
Username: natas19 \
URL:      http://natas19.natas.labs.overthewire.org
# HOW TO SOLVE IT
1.Login \
<img width="965" height="436" alt="image" src="https://github.com/user-attachments/assets/40191763-8d23-41fa-9ffb-21f7e3b79be0" /> \
2.TRIAL AND ERROR \
 - Try the previous script only change the credentials for login
 - <img width="669" height="224" alt="image" src="https://github.com/user-attachments/assets/1050cef9-094b-4951-82b0-5669e6032d4a" />
 - What a miss
 - LETS TRY ANOTHER WAY

3.TRy to login \
 - Use admin:previous password level
 - <img width="962" height="287" alt="image" src="https://github.com/user-attachments/assets/804f1488-40ac-4806-aa15-44c046d262ad" />
 - WEv still need to change the session id
4.Get PhpSessionId Format \
 - After login.inspect,and view the cookie
 - Copy sessionID and decode it,it is a hex from the look.
 - <img width="778" height="357" alt="image" src="https://github.com/user-attachments/assets/8c7e71a3-d902-45be-bf0d-70eebffd1efe" />
 - now we know the format,admin-sessionID

5.Craft an automated script to brute force using the known ID format \
<img width="618" height="610" alt="image" src="https://github.com/user-attachments/assets/b6563532-65e0-4899-bfe6-74e1a575151b" /> \
<img width="944" height="950" alt="image" src="https://github.com/user-attachments/assets/a2e98124-fd25-4927-881f-8a2acf762b5e" /> 
# Flag: p5mCvP7GS2K6Bmt3gqhM2Fc1A5T8MVyw






