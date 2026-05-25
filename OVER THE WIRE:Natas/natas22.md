# CHALLENGE
ACCESS NEXT LEVEL'S PASSWORD \
GIVEN: \
Password: d8rwGBl0Xslg3b76uh3fEbSlnOUBlozz \
Username: natas22 \
URL:      http://natas22.natas.labs.overthewire.org
# SOLUTION
1.Login \
<img width="962" height="255" alt="image" src="https://github.com/user-attachments/assets/6eac1e6c-55bc-47bc-bf60-cde1c49e3f93" /> \
2.View source code \
<img width="960" height="629" alt="image" src="https://github.com/user-attachments/assets/de9f4ed3-55db-463c-a872-ee6ace8dbef5" /> \
3.Interpretation 
 - The page uses:
   - header("Location: /");
 - but still processes the protected content afterward unless execution is stopped with exit();.
 - The solution is simply to prevent your client from following redirects.

4.Explot \
Command syntax:
 - curl -u natas22:<PASSWORD> -i http://natas22.natas.labs.overthewire.org/?revelio=1
<img width="959" height="982" alt="image" src="https://github.com/user-attachments/assets/e7ace0eb-004b-4336-a7b2-32a8867c2d9a" /> \
# Flag: dIUQcI3uSus1JEOSSWRAEXBG8KbR8tRs
