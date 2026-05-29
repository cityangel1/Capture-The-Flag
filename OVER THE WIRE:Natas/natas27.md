# CHALLENGE
ACCESS NEXT PASSWORD \
given \
Password:u3RRffXjysjgwFU6b9xa23i6prmUsYne \
Username: natas27 \
URL:      http://natas27.natas.labs.overthewire.org
# SOLUTION
1.Login \
<img width="960" height="374" alt="image" src="https://github.com/user-attachments/assets/26fbfdbc-9e62-4ad6-809a-8e47e2e61401" /> \
2.View source code \
<img width="895" height="923" alt="image" src="https://github.com/user-attachments/assets/dee09126-33eb-403a-b138-de5dd4c735e8" /> \
3.Understanding
  - The application limits usernames to a fixed length in the database (typically 64 characters). MySQL silently truncates longer values when storing them.
  - Suppose there is already a user:
     - natas28
     - You can register a new username such as:
     - natas28 <Alot of spaces>                                                       
     - where enough trailing spaces are added to exceed the column length
  - Because of truncation and how the application handles authentication, the stored username may collide with the existing account while retaining your chosen password.

4.How to solve 
  - The username column in the database is limited to 64 characters (VARCHAR(64)).
  - We create a fake user: "natas28" + 57 spaces + "x" → MySQL truncates it to "natas28" + 57 spaces.
  - This truncated username is identical (after trimming) to the real natas28 account.
  - When we login using the padded username (natas28 + 57 spaces), the system thinks it's the real user.
  - The page then leaks the real password of natas28.
  - <img width="769" height="295" alt="image" src="https://github.com/user-attachments/assets/59c9b012-0eae-4f5c-b5ce-37e4f5b15d54" />
  - WILL ATTACH CODE.

# Flag: 1JNwQM1Oi6J6j1k49Xyw7ZN6pXMQInVj
