# CHALLENGE
ACCESS NBEXT LEVEL'S PASSWORD \
gIVEN \
Paassword:MeuqmfJ8DDKuTr5pcvzFKSwlxedZYEWd \
Username: natas24 \
URL:      http://natas24.natas.labs.overthewire.org
# SOLUTION
1.Login \
<img width="955" height="368" alt="image" src="https://github.com/user-attachments/assets/bb3689dd-3198-448f-842b-3202bc5f40e5" /> \
2.View source code \
<img width="959" height="590" alt="image" src="https://github.com/user-attachments/assets/6834371c-de5c-4f14-b16b-0de1f1337305" /> \
3.Inteprete
 - THis is another PHP type confusion challenge, this time abusing how PHP handles arrays in string functions.
 - The vulnerable code is effectively:
  - if (strcmp($_REQUEST["passwd"], $password) == 0)
 - The issue:
  - strcmp() expects strings.
 - If you send an array instead:
  - passwd[]
  - PHP emits a warning and returns NULL.
  - Then:
   - NULL == 0
   - evaluates to true in weak comparison.

4.WE ARE GOOD TO GO,LETS USE CURL TO SEND THE ARRAY!!
 - Syntax: curl -u natas24:<PASSWORD> "http://natas24.natas.labs.overthewire.org/?passwd[]="
 - <img width="964" height="963" alt="image" src="https://github.com/user-attachments/assets/cd20b45d-2ee1-4042-beb3-e2d33bb292cf" />

# Flag: ckELKUWZUfpOv6uxS6M7lXBpBssJZ4Ws
