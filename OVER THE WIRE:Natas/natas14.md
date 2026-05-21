# CHALLENGE
Access next level's password \
Password: z3UYcr4v4uBpeX8f7EZbMHlzK4UR2XtQ \
Username: natas14 \
URL:      http://natas14.natas.labs.overthewire.org
# SOLUTION
1.Login \
<img width="964" height="383" alt="image" src="https://github.com/user-attachments/assets/3c6fc2f7-92b6-451b-a614-d607036e12b7" /> \
2.View source code. \
<img width="960" height="681" alt="image" src="https://github.com/user-attachments/assets/3d305341-7ac6-495e-9c8d-6211bbd648ee" /> \
3.Interpretation. \
 - The server takes in a username and password and queries the database.
 - It does not sanitize inputs,so we can inject an sql.
 - we will use the vintage sql injection,' OR 1=1 -- 

4.Do it. \
<img width="961" height="381" alt="image" src="https://github.com/user-attachments/assets/4d3fd78d-2cfb-4362-88fe-0e1ad48a86dd" /> \
<img width="959" height="337" alt="image" src="https://github.com/user-attachments/assets/63e421cb-f619-41f9-b6ab-ac431f4ea3c5" /> \
Lets try first supplying a username then the injection. \
<img width="958" height="435" alt="image" src="https://github.com/user-attachments/assets/ccb31630-d5ef-42bb-a008-517cc1f4fdf9" /> \
<img width="960" height="390" alt="image" src="https://github.com/user-attachments/assets/170e7890-f065-4536-9f27-874fd9146d8e" />
# Flag: SdqIqBsFcz3yotlNYErZSZwblkm0lrvx






