# CHALLENGE
ACCESS NEXT PASSWORD : \
gIVEN:: \
Password: dIUQcI3uSus1JEOSSWRAEXBG8KbR8tRs \
Username: natas23 \
URL:      http://natas23.natas.labs.overthewire.org
# SOLUTION
1.Login \
<img width="960" height="362" alt="image" src="https://github.com/user-attachments/assets/26c57668-7e65-49b6-861a-1fbd707ec0a6" /> \
2.View source code \
<img width="934" height="565" alt="image" src="https://github.com/user-attachments/assets/c8297dc1-eb8d-4db4-9d68-16697b81e62c" /> \
3.Interprete 
 - The vulnerable logic is essentially:
  - if ($passwd == "iloveyou") {
     ...
    }
 - combined with a numeric check like:
  - if (!is_numeric($passwd)) {
 - The trick:
  - PHP weak comparison (==) can treat strings beginning with numbers strangely.

4.Exploit \
 - syntax curl -u natas23:<PASSWORD> "http://natas23.natas.labs.overthewire.org/?passwd=11iloveyou"
 - <img width="944" height="852" alt="image" src="https://github.com/user-attachments/assets/ef49d27d-c9e5-4041-835a-77829f36207a" />
 - What happenned
   - PHP converts "11iloveyou" to integer 11
   - Weak comparisons and numeric coercion create unexpected truthy behavior
# Flag: MeuqmfJ8DDKuTr5pcvzFKSwlxedZYEWd
