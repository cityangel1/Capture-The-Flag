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
4
