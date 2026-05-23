# CHALLENGE
ACCESS NEXT FLAG FOR NEXT NEXT LEVEL PASSWORD: \
GIVEN: \
Password:6OG1PbKdVjyBlpxgD4DDbRG6ZLlCGgCJ \
Username: natas18 \
URL:      http://natas18.natas.labs.overthewire.org 
# SOLUTION
1.lOGIN \
<img width="961" height="360" alt="image" src="https://github.com/user-attachments/assets/66ea0ce8-d53c-4e78-a5eb-f9e9f4a20416" /> \
2.View source code \
<img width="832" height="877" alt="image" src="https://github.com/user-attachments/assets/28d38af3-4245-4051-b9fb-5c8827e247a4" /> \
3.UNDERSTAND THE VULNERABILITY
 - This is a session hijacking vulnerability
 - The code says that only the admin can view the password
 - Now when you login,you will just be a normal user,so we need to switch our user role to admin
 - Now,they have made it easy for us,because we only need to know the session id of the admin to access the flag
 - session ids range from 1-641.
 - so we need to brute force the IDs.Now you can use manual brute force where you input an id and refresh the page each tiome,well good luck with that because by the time you finish Jesus would have returned to take his saints
 - Or you can do it my way,automated python script.

4.Brute forcethe admin session Id \
<img width="944" height="697" alt="image" src="https://github.com/user-attachments/assets/b9030c43-4f44-4527-9c3b-e90aff7da84b" /> \
<img width="956" height="330" alt="image" src="https://github.com/user-attachments/assets/287159be-23e5-48fb-80f9-add83ebb7c8e" />
# Flag: tnwER7PdfWkxsG4FNWUtoAZ9VyZTJqJr





