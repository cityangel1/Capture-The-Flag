# Level Goal
There is a git repository at ssh://bandit28-git@bandit.labs.overthewire.org/home/bandit28-git/repo via the port 2220. The password for the user bandit28-git is the same as for the user bandit28.
From your local machine (not the OverTheWire machine!), clone the repository and find the password for the next level. This needs git installed locally on your machine.
# Solution
1.CLONE REPO:
  - git clone ssh://bandit28-git@bandit.labs.overthewire.org:2220/home/bandit28-git/repo
  - Enter Password solved from previous level
  - ls
  - cd repo
  - ls
  - cat README.md
  - <img width="645" height="253" alt="image" src="https://github.com/user-attachments/assets/15211663-8eb1-481b-9a7d-39d551227b06" />
2.WE NEED TO KNOW THE PASSWORD.SO WE LOOK AT PREVIOUS COMITS:
  - git log README.md
  - <img width="944" height="464" alt="image" src="https://github.com/user-attachments/assets/86c111c6-e8f7-43a1-8644-35dc4562e2ea" />
  - IM NOT A GENIUS BUT I CAN TELL "fix info leak" is it
  -Examine it
       - git show b5ed4b5a3499533c2611217c8780e8ead48609f6:README.
       -<img width="954" height="294" alt="image" src="https://github.com/user-attachments/assets/5d70f012-380a-444d-8cab-aa3d18cde3a5" />
       - username: bandit29
       - password: 4pT1t5DENaYuqnqvadYs1oE4QLCdjmJ7
