# AWS-Projects
Hey there
I will not start by my introduction because that's not important right now but i am a B.com graduate having keen interest in Cloud, I had deployed the Virtual server in which i faced some problem while connecting it through W-powershell. 

So let's get started with the steps How to Launch your server. 
i) Firstly we have to login in console through User not the Root
ii) Then go to EC2(Elastic Compute) 

<img width="883" height="544" alt="Image" src="https://github.com/user-attachments/assets/786dec98-0757-4619-9abc-acc06dc2e208" />
iii) Give name to your Instance and select AMI(Amazon Machine Image)

iv) In my first try i didn't create VPC I used the default one

<img width="897" height="460" alt="Image" src="https://github.com/user-attachments/assets/7fde31ea-5b47-4543-becc-c940801ef3e5" />
v) Don't forget to Allow SSH(Secure Shell) port 22. 

<img width="818" height="250" alt="Image" src="https://github.com/user-attachments/assets/f0725086-2ccf-4105-b484-51ccae91ab7a" />
 vi) When the instance was in Running State, i launched it through Connect(Amazon EC2 Instance Connect provides a simple and secure way to connect to your instances using Secure Shell (SSH).)

<img width="1361" height="626" alt="Image" src="https://github.com/user-attachments/assets/ede47e08-78d6-42a7-88a2-49f890b78bfb" />

vii) After that i tried to launched it through W-Powershell: - ssh -i .\mykey.pem ec2@publicip
    >But it was not connecting to the server Error 
      "Warning: Identity file .\mykey.pem not accessible: No such file or directory. ec2-user@34.239.128.198: Permission denied      (publickey,gssapi-keyex,gssapi-with-mic).

<img width="1362" height="258" alt="Image" src="https://github.com/user-attachments/assets/0fde42e1-2a76-4ea5-8f11-552c76b7e291" />

viii) Then i tried to solve this error, for that i had to enter the full path where the key was stored. 
     > ssh -i "C:\Users\YourName\Downloads\mykey.pem" ec2-user@34.239.128.198

<img width="1362" height="602" alt="Image" src="https://github.com/user-attachments/assets/d026a56c-3fed-460b-8ecf-d6ddb2bb3798" />

So i did launch my First Virtual server through EC2 , it was time consuming but worth it, in the same way you can launch the other AMI also. I tried to explain the whole process through this i know it's not that much impressive but this is my first...
