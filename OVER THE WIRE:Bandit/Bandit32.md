<img width="948" height="796" alt="image" src="https://github.com/user-attachments/assets/f9059587-166c-4946-b172-dcfc8600f78a" /># Level Goal
There is a git repository at ssh://bandit31-git@bandit.labs.overthewire.org/home/bandit31-git/repo via the port 2220. The password for the user bandit31-git is the same as for the user bandit31.
From your local machine (not the OverTheWire machine!), clone the repository and find the password for the next level. This needs git installed locally on your machine.
# Solution
1.CLONE:
  - mkdir bandit31
  - cd bandit31
  - git clone ssh://bandit31-git@bandit.labs.overthewire.org:2220/home/bandit31-git/repo
  - Enter password
  - ls
  - cd repo
  - ls
  - cat README.md
  - <img width="797" height="192" alt="image" src="https://github.com/user-attachments/assets/2e757a61-7445-440c-a425-ee0d69cd1ddf" />
2.PUSH:
  - First check .gitignore : cat .gitignore
  - <img width="539" height="75" alt="image" src="https://github.com/user-attachments/assets/a99f4c36-0f09-4dae-a32e-2ff710e2a8d4" />
  - Means it ignores .txt files: WE have to override
  - CREATE THE FILE:
         -echo "May I come in?" > key.txt
         -git add -f key.txt                   - overrides .gitignore
         -git commit -m "Add key.txt"
  - Actual push : git push origin master
  - Enter password
  - <img width="948" height="796" alt="image" src="https://github.com/user-attachments/assets/f9059587-166c-4946-b172-dcfc8600f78a" />
  -PASSWORD:3O9RfhqyAlVBEZpVb6LYStshZoqoSx5
# Amazing
