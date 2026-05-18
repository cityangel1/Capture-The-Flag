# Level Goal
There is a git repository at ssh://bandit30-git@bandit.labs.overthewire.org/home/bandit30-git/repo via the port 2220. The password for the user bandit30-git is the same as for the user bandit30.
From your local machine (not the OverTheWire machine!), clone the repository and find the password for the next level. This needs git installed locally on your machine.
# Solution
1.Clone:
  - mkdir bandit30
  - cd bandit30
  - git clone ssh://bandit30-git@bandit.labs.overthewire.org:2220/home/bandit30-git/repo
  - ls
  - cd repo
  - ls
  - cat README.md
  - <img width="927" height="837" alt="image" src="https://github.com/user-attachments/assets/41e81e42-f5ff-4b41-a945-976b4c4827bf" />
2.GET PASSWORD:
  - Check Branches: git branch -a
  - <img width="549" height="126" alt="image" src="https://github.com/user-attachments/assets/b45125ab-0310-4246-8c29-3f7a837d863a" />
  - Just one branch
  - Check tags: git tag
  - Show Secret: git show secret
  - <img width="546" height="124" alt="image" src="https://github.com/user-attachments/assets/e185916f-3b10-4cd8-8996-b50c74a02eb3" />
  -PASSWORD:fb5S2xb7bRyFmAvQYQGEqsbhVyJqhnDy
