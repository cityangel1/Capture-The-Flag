# Level Goal
After all this git stuff, it’s time for another escape. Good luck!
# Solution
1.When I first saw this I was confused as an oasis in a desert.A glimse of hope. \
2.LOGIN:  
  - ssh bandit32@bandit.labs.overthewire.org -p 2220 \
  - Enter password
3.GET PASSWORD:
  - ls
  - cat /etc/bandit_pass/bandit33
  - <img width="459" height="159" alt="image" src="https://github.com/user-attachments/assets/4473c954-b37d-4241-b0a7-66f6781898fe" />  - Something is happening:ITS CONVERTING EVERYTHING TO UPPERCASE(JOKE:EVEN THIS LINE OF TEXT)
  - So we need to escape that : $0
      - $0  -- RESEARCH :$0 in a shell script (or interactive shell) expands to the name/path of the currently executing program/shell.
                        -Here:
                        -Your current shell is /home/bandit32/uppershell (a setuid binary owned by bandit33 with SUID bit set: -rwsr-x--- 1 bandit33 bandit32).
                        -Typing $0 tells the shell to re-execute itself (i.e., run /home/bandit32/uppershell again), but because of how the shell spawning works, it actually gives you a new normal shell (likely /bin/sh) as the effective user bandit33 (thanks to the SUID).
  - cat /etc/bandit_pass/bandit33
  - <img width="472" height="124" alt="image" src="https://github.com/user-attachments/assets/0c42c591-55fe-4118-80db-8d261335a8fe" />
  - PASSWORD:tQdtbs5D5i2vJwkO8mEyYEyTL8izoeJ0
