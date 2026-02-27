# Level Goal
The password for the next level is stored in a file somewhere under the inhere directory and has all of the following properties: \
human-readable \
1033 bytes in size \
not executable \
# Solution
Hint:That means we should show the file properties to know which is which. \
Terminal : \
1.cd inhere \
2.ls -la \
<img width="706" height="606" alt="image" src="https://github.com/user-attachments/assets/849e56ea-b3dc-4923-a36d-a9c7b77c6573" /> \
Analyze : No hint \
3. Find file by refining search. \
Command: find . -size 1033c ! -executable \
. - find in that directory. \
-size 1033c - specify the file size.c for bytes. \
! -executable - a file thats not execytable. \
<img width="727" height="88" alt="image" src="https://github.com/user-attachments/assets/11f65f4e-5259-4da0-8d18-fd5f9894f4b2" /> \
4. Open the file. \
cat ./maybehere07/.file2 \
<img width="1238" h eight="327" alt="image" src="https://github.com/user-attachments/assets/928b008c-b2b7-4b49-baac-abbd490ec45f" /> \
5.ssh bandit6@bandit.labs.overthewire.org -p 2220 \
Password: HWasnPhtq9AVKe0dmk45nxy20cvUa6EG \
SUCCESS.FELT THRILLED. \
<img width="504" height="196" alt="image" src="https://github.com/user-attachments/assets/032f25c7-80fa-45ef-972c-8e57a5d284c1" /> \
