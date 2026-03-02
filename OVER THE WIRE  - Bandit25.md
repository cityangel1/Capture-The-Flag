# Level Goal
A daemon is listening on port 30002 and will give you the password for bandit25 if given the password for bandit24 and a secret numeric 4-digit pincode. There is no way to retrieve the pincode except by going through all of the 10000 combinations, called brute-forcing.
You do not need to create new connections each time.
# Solution
1.Login to session. \
2.nc localhost 30002 : Get to know what happens. \
3.TRy a combination: echo "gb8KRRCsshuZXI0tUuR6ypOFjiZbf3G8 0000" | nc localhost 30002 : ERror \
<img width="941" height="137" alt="image" src="https://github.com/user-attachments/assets/f41e7769-6b5f-4ec3-a97b-113a7ab2fc36" /> \
4. Create a script that brute forces all combinations untill the correct one is found. \
 - mkdir /tmp/brute_force
 - nano brute_python.sh
 - <img width="928" height="902" alt="image" src="https://github.com/user-attachments/assets/299d9324-99b8-432f-87db-1e5370ad4244" /> \
 - Make it executable: chmod +x brute_python.sh
 - <img width="850" height="242" alt="image" src="https://github.com/user-attachments/assets/11631cc5-2acb-4411-970b-14ec3d471937" />
 - PASSWORD FOR BANDIT 25:iCi86ttT4KSNe1armKiwbQNmB3YJP3q4
   # Computer Intimacy
[brute_python.sh](https://github.com/user-attachments/files/25683786/brute_python.sh)


