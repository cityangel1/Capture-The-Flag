# Level Goal
A program is running automatically at regular intervals from cron, the time-based job scheduler. Look in /etc/cron.d/ for the configuration and see what command is being executed.
# Solution
1.look at the specified dir. \
 cd /etc/cron.d \
 ls \
 Since its bandit23 : must be cronjob_bandit23 \
2.cat cronjob_bandit23 \
<img width="763" height="109" alt="image" src="https://github.com/user-attachments/assets/1d914d05-b283-4083-a6ad-a081c9c76b1a" /> \
3. cat /usr/bin/cronjob_bandit23.sh \
<img width="864" height="269" alt="image" src="https://github.com/user-attachments/assets/b2e9b297-fdc0-4f65-817c-4b7e46f0c27a" /> \
4.UNDERSTAND THE CODE: \
now what it does: myname is bandit23 - from whoami command result. \
                : mytarget is the md5 hash of (I am user bandit23).\
5.Hash with md5. \
6.view file. \
<img width="882" height="117" alt="image" src="https://github.com/user-attachments/assets/b30c9056-28b5-423a-960b-d0826cedeadb" /> \
Password for bandit 23:0Zf11ioIjMVN551jX3CmStKLYqjk54Ga \




 
