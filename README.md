- We used AWS to execute the challenge to demonstrate our flexibility in performing DevOps tasks and our skills. First, we created an EC2 instance running Ubuntu t2.micro.

- 
 ![1](https://github.com/user-attachments/assets/91b1c92e-d8a5-4393-a960-75b9f1ccd19c)

![2](https://github.com/user-attachments/assets/1f940974-4530-4f12-9a8a-b956a2dab4d8)

We installed everything related to running Docker and Docker Compose.


![3](https://github.com/user-attachments/assets/410df23f-9394-4237-964c-e1149c7f5f7a)

![5](https://github.com/user-attachments/assets/332589e6-16ae-4bb9-93ca-e79385010bec)

![4](https://github.com/user-attachments/assets/0af53371-683a-447e-9c2b-508a6544d482)


We created the Dockerfile for the API file, The modifications were added to the GitHub file.
We create our project on folder called challenge, and get the file from github on my ec2.


![6](https://github.com/user-attachments/assets/6c1fb4e9-6007-4fdd-951a-3b924e0230cb)

Dockerfile for client file.


![7](https://github.com/user-attachments/assets/2e76740d-6110-4c82-a369-efc616727b2d)

create docker-compose.yml file


![8](https://github.com/user-attachments/assets/9ab458af-d3c9-40fe-b299-12ec151a0f97)

![9](https://github.com/user-attachments/assets/d9a3dfb3-1ae9-42df-beb0-4ea3c9606001)

This command is used to generate a self-signed SSL certificate using OpenSSL. It creates a new private key (nginx-selfsigned.key) and a certificate (nginx-selfsigned.crt) valid for 365 days, using RSA with a key size of 2048 bits. This is a bonus point!


![10](https://github.com/user-attachments/assets/8635cfac-8ff5-4ddb-8742-8d2b8ef90519)

![11](https://github.com/user-attachments/assets/b79cf978-58a3-406b-adcf-b13b220f1678)

We modified the `/etc/nginx/nginx.conf` file to complete the rest of the task, as shown in the image.


![image](https://github.com/user-attachments/assets/bab1baa5-3907-4f75-87f1-bea48cc41d96)


In the end, we started running Docker Compose, and many issues appeared due to the PHP version, but we resolved them. We also replaced all the missing files. Finally, we activated the images and then the containers.


![Screenshot (296)](https://github.com/user-attachments/assets/93d1aa90-941b-476a-ba96-f90a12f6702c)

![Screenshot (295)](https://github.com/user-attachments/assets/27a85991-4047-4252-87a2-be9a7ade1480)

![Screenshot (297)](https://github.com/user-attachments/assets/32c14be5-c3f8-4a3f-8afd-cb47c9da511f)![Screenshot (298)](https://github.com/user-attachments/assets/da774918-97eb-4cbc-b2b7-f4a7c73d7c4d)

![Screenshot (299)](https://github.com/user-attachments/assets/4c9637af-4f62-4800-a379-2a745a279e7a)


In the end, executing the task on an EC2 t2.micro wasn't the best choice due to its limited resources. However, we did this to demonstrate our cloud expertise on any platform. We used the t2.micro instance and didn't upgrade the resources because it's part of the free tier.
