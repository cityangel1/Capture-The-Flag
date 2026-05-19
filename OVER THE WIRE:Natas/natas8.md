# CHALLENGE
Username: natas8 \
Password: xcoXLmzMkoIP9D7hlgPlh9XD7OgLAe5Q  \
URL:      http://natas8.natas.labs.overthewire.org \
# SOLUTION
1.Login \
<img width="965" height="369" alt="image" src="https://github.com/user-attachments/assets/8a466cd3-c71e-447f-9de9-f2b14262ef58" /> \
<img width="959" height="448" alt="image" src="https://github.com/user-attachments/assets/c28c7235-bff3-45db-97a2-c03f46f3bb8b" /> \
SOMETHING IS DENYING US ACCESS. \
Lets TRy curl \
<img width="942" height="783" alt="image" src="https://github.com/user-attachments/assets/539f10be-50a8-48ba-ae75-a0d05d55ec43" /> \
THen try login again. \
<img width="961" height="375" alt="image" src="https://github.com/user-attachments/assets/37494e4c-6aca-4efc-ab4a-852117a5b3b8" /> \
IT WORKED,IS IT MAGIC OR COINCEDENCE. \
2.View source code. \
<img width="959" height="668" alt="image" src="https://github.com/user-attachments/assets/9c1ad778-9e73-4d0b-915b-1936cc93e3f9" /> \
INTEPRETATION: \
  - ITS AN ENCODING TRICK.YOU ARE GIVEN AN ENCODED VALUE AND YOU JOB IS TO DECODE THE ORIGINAL VALUE AND FEED IT TO THE INPUT FILED WHICH WILL INTURN GIVE THE PASSWORD. \
4.DECODE. \
 -Bin2hex DECODE,ONLINE TOOLS.OUTPUT = "==QcCtmMml1ViV3b" \
 -<img width="963" height="562" alt="image" src="https://github.com/user-attachments/assets/2a521a4d-b3e9-452d-9a90-4715c343c93e" /> \
 -String reverse,online.Output= "b3ViV1lmMmtCcQ=="
 -Base64 Decode,online tool.Output = "oubWYf2kBq"
 -<img width="958" height="872" alt="image" src="https://github.com/user-attachments/assets/95ead74f-2967-4d5a-a9d7-3e2cf30cfc61" /> \
5.Give the secret. \
<img width="962" height="370" alt="image" src="https://github.com/user-attachments/assets/c0fc1093-a4d7-440a-97a4-a5d880750c6e" />
# FLAG : ZE1ck82lmdGIoErlhQgWND6j2Wzz6b6t
 




