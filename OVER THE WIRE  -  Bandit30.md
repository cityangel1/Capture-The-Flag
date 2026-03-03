# Level Goal
There is a git repository at ssh://bandit29-git@bandit.labs.overthewire.org/home/bandit29-git/repo via the port 2220. The password for the user bandit29-git is the same as for the user bandit29.
From your local machine (not the OverTheWire machine!), clone the repository and find the password for the next level.
This needs git installed locally on your machine.
# Solution
1.CLONE REPO:
  - mkdir bandit29
  - cd bandit29
  - git clone ssh://bandit29-git@bandit.labs.overthewire.org:2220/home/bandit29-git/repo
  - Enter Password
  - cd repo
  - ls
  - cat README.md
  - <img width="937" height="925" alt="image" src="https://github.com/user-attachments/assets/03ef1949-abe0-45ef-bed6-cdb9a959e5cc" />
2.GET PASSWORD FROM THE CORRECT BRANCH
  - git branch -a
  - git checkout dev
  - cat README.md
  - <img width="822" height="437" alt="image" src="https://github.com/user-attachments/assets/470c231b-16f3-409a-97c4-b844e35382ee" />
  - PASSWORD:qp30ex3VLz5MDG1n91YowTv4Q8l7CDZL
