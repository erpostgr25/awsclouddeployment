# AWS Cloud Deployment
## 1. Backend Configuration:
Step By Step Procedure:  
Clone the application on EC2.  
<img width="1137" height="400" alt="1" src="https://github.com/user-attachments/assets/c5b1bcb4-f4ac-4992-bee0-a9772431eeea" />  
Set up a reverse proxy using nginx  
<img width="801" height="306" alt="nginx1" src="https://github.com/user-attachments/assets/21676c29-850f-487c-bef0-fe65ad6e38e2" />  
Updated the .env and started the backend.  
<img width="573" height="56" alt="image" src="https://github.com/user-attachments/assets/434f8819-9048-4a60-abd8-730f39889e22" />  
## 2. Frontend and Backend Connection:  
Configured url.js on frontend  
<img width="1086" height="78" alt="image" src="https://github.com/user-attachments/assets/62793322-65f2-4ac1-af47-ec697407b4d9" />  
Successfully able to access fronend using nginx rev proxy server and updated many travel experiences  
<img width="1072" height="1028" alt="nginx2" src="https://github.com/user-attachments/assets/15cd5a9d-0d69-4a34-b808-b1bb5d1fec2c" />  
Same have been updated in mongo DB, reference below:  
<img width="948" height="602" alt="5" src="https://github.com/user-attachments/assets/c205af03-8289-4879-9d34-cd0d8a9c998a" />  

## 3. Scaling the Application:  
Created multiple EC2 instances to test ALB functionality  
<img width="522" height="221" alt="image" src="https://github.com/user-attachments/assets/5023dd79-9528-4cd7-b740-e19df8abf98f" />  
Created two target group, details below  
<img width="1242" height="355" alt="tg1" src="https://github.com/user-attachments/assets/29d024e2-de93-4d12-a4f6-f61f41c9302f" />  
<img width="1387" height="832" alt="tg2" src="https://github.com/user-attachments/assets/64ee6b23-d9a5-4690-8795-030befc7fef5" />  
 
<img width="1396" height="786" alt="tg3" src="https://github.com/user-attachments/assets/7e2a204a-3fb2-4a45-a900-75bc77694fb7" />  

ALB created and both target group has been added, shown below:  
<img width="1402" height="210" alt="alb1" src="https://github.com/user-attachments/assets/9ffe8c8a-705a-460f-a577-19a8feba7e57" />  
## For backend target group role been created so that the ALB distribution can be verified  
<img width="1477" height="847" alt="alb2" src="https://github.com/user-attachments/assets/1e4d8c5d-be7e-4db1-8351-ca1be5705a2a" />  
Testing TravelMonitor app using load balancer endpoint, as below  
<img width="1120" height="1016" alt="ft1" src="https://github.com/user-attachments/assets/df39e559-db7f-4896-a63a-00a23ac63c6e" />  
Verifying the load balancing first attempt hits backend 1 server  
<img width="858" height="195" alt="bk1" src="https://github.com/user-attachments/assets/92d8509a-c3d3-41d4-ad2a-0ad53c1091f3" />  

Verifying the load balancing again for second attempt hits backend 2 server  
<img width="862" height="196" alt="bk2" src="https://github.com/user-attachments/assets/96600a41-c42e-4c5e-a98e-40eb22949aa1" />  

## 4. Domain Setup with Cloudflare:  
Created custom domain on Cloudflare  
<img width="1500" height="386" alt="cf1" src="https://github.com/user-attachments/assets/10e71b76-97ce-4cb3-a232-280608de10aa" />  
A record to EC2 instance public IP and CNAME record to ALB endpoint respectively  
<img width="1820" height="602" alt="CNAME" src="https://github.com/user-attachments/assets/7a8809bc-ad0a-4c17-9945-9b6215e9fb46" />  
## Test Rsult  
<img width="1117" height="1022" alt="cf2" src="https://github.com/user-attachments/assets/2760736e-e678-41c7-8b4f-27d4a39e12f4" />  
<img width="630" height="152" alt="cf3" src="https://github.com/user-attachments/assets/08f8087d-e6df-4c86-abec-be972fd06d8b" />  
<img width="602" height="167" alt="cf4" src="https://github.com/user-attachments/assets/f2fa7692-62f7-4e97-ad53-5a821f851268" />  
