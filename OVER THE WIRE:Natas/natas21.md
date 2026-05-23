# TASK
Access next password \
Given the login credentials: \
Password: "BPhv63cKE1lkQl04cE5CuFTzXe15NfiH" \
Username: natas21 \
URL:      http://natas21.natas.labs.overthewire.org
# SOLUTION
1.Login \
<img width="959" height="414" alt="image" src="https://github.com/user-attachments/assets/a1e72e97-88a5-489b-bb7b-dc7c40987c37" /> \
2.View Source Code \
<img width="919" height="646" alt="image" src="https://github.com/user-attachments/assets/03caa4e3-4102-4274-8b8a-ae0ab6682580" /> \
3.Go to the colocater website. \
<img width="964" height="569" alt="image" src="https://github.com/user-attachments/assets/260ddbe2-8ebb-4738-8007-99daba6e8064" /> \
View its source code \
<img width="960" height="870" alt="image" src="https://github.com/user-attachments/assets/5f6f7bc4-c2a8-491b-8489-1b3290097456" /> \
4.INterpretation 
 - is a privilege escalation challenge involving session poisoning between two applications:
  - main site
  - experimenter subdomain
 - The vulnerable experimenter app lets you inject arbitrary session variables like:
  - admin=1,which is what we want so we can gain priviledges as admin.

5.SOLVE \
I used a python script.I will attach it as natas21.py \
<img width="940" height="931" alt="image" src="https://github.com/user-attachments/assets/6fe0cf07-0331-4e38-ab6a-c3db0e45dc97" /> 
 - What the script does
    - The script first connects to the experimenter site and obtains a valid PHPSESSID.
    - It sends admin=1, which poisons the shared PHP session storage on the server.
    - The script manually reuses the same session ID on the main natas21 site.
    - Because both applications trust the same backend session data, the main app treats you as an admin.

# Flag: d8rwGBl0Xslg3b76uh3fEbSlnOUBlozz
