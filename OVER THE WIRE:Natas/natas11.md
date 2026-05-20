# CHALLENGE
Access next password. \
GIven \
 - Password:UJdqkK1pTu6VLt9UHWAgRZz6sVUZ3lEk
 - Username: natas11
 - URL:      http://natas11.natas.labs.overthewire.org
# SOLUTION
1.Login. \
<img width="960" height="358" alt="image" src="https://github.com/user-attachments/assets/d2aa83c3-9e2b-48c2-a1ff-2c162220f562" /> \
2.View source Code. \
<img width="961" height="924" alt="image" src="https://github.com/user-attachments/assets/134907ab-306f-4f03-8434-4d5933e31b32" /> \
3.INterpretation. \
 - THe code encrypts the cookie using XOR in a Base64 encoding which inturn is encoded using json.
 - WE already know the datavalue that is being encrypted : $defaultdata = array( "showpassword"=>"no",  "bgcolor"=>"#ffffff");
 - Now inorder to pass this level we need to set the show password value to "yes" and then encode to Json,Base64 and finally through XOR
 - Lets express this mathematically
   - let a=$defaultdata = array( "showpassword"=>"no", "bgcolor"=>"#ffffff");
   - let encrypting key be X
   - let cookie be y.
   - NOw we know the cookie value and the data,we only dont know the XOR key,we work backwards to recover the key and then encrypt our data with the new key to get the password.
   - Lets do it. \

4.Get Key.\
NOw here we will use a php code to do the work for us.I have attached the php file so you can see what i used. \
Now all you need to input is the cookie value.to get cookie value,right click on web,go to inspect,then storage,then cookies,then copy the cookie value. \
<img width="964" height="855" alt="image" src="https://github.com/user-attachments/assets/520e511b-364c-4dca-ac7c-c47a713d2e1d" /> \
<img width="942" height="156" alt="image" src="https://github.com/user-attachments/assets/0b975a3b-20a3-43c5-ae03-c65edc9eb6e2" /> \
KEY:eDWo \
5.Encrypt the data with showpassword set to yes. \
I have also attached the file. \
<img width="953" height="819" alt="image" src="https://github.com/user-attachments/assets/d367dfb5-5a7d-4e69-9603-01daaf3309d3" /> \
6.replace the cookie in the web and refresh. \
<img width="960" height="822" alt="image" src="https://github.com/user-attachments/assets/2c1d1158-111a-4032-9495-f020fc0d23f0" /> \
<img width="960" height="282" alt="image" src="https://github.com/user-attachments/assets/5706ff5e-34af-44ca-b58f-bc318eb5c7ec" />
# Flag: yZdkjAYZRd3R7tq7T5kXMjMJlOIkzDeB






