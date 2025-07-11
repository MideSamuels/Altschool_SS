# AltSchool Africa Tinyuka Cloud Engineering Second Semester Exam

###Building and Hosting a Web Prototype on an Ubuntu EC2 Instance

<img width="1155" height="813" alt="image" src="https://github.com/user-attachments/assets/02fc6f66-af33-4a51-b3c2-79225b8b26e0" />
<img width="1531" height="666" alt="image" src="https://github.com/user-attachments/assets/97ccfe55-a5aa-48c6-bc23-94b5fe455960" />
<img width="1795" height="746" alt="image" src="https://github.com/user-attachments/assets/09c46e5e-9a55-4212-862a-7e796d5105ae" />

 1. Provisioning the EC2 Instance
I logged into my AWS account and launched a new EC2 instance with the following configuration:
Operating system: Ubuntu Server 24.04 LTS
Instance Type: t2.micro (Free Tier eligible)
Key Pair: Created a new  .pem key for secure SSH access
Security Group Settings:
•	Inbound: Allowed traffic on ports 22 (SSH), 80 (HTTP), and 443 (HTTPS)
•	Outbound: All traffic allowed
After launching, I copied the public IPv4 address of the instance.
2. Connecting via SSH
Using the terminal on my local machine, I connected to the instance with:
ssh -i "Alt_School_SS.pem" ubuntu@ec2-3-252-139-233.compute-1.amazonaws.com
3. Installing Nginx
Once logged in, I updated the package index and installed Nginx:
•	sudo apt update
•	sudo apt install nginx -y
4.  Creating Website Files on the Server
Instead of uploading files from my local computer, I created them directly on the server using nano:
Created a new index.html:  sudo nano /var/www/html/index.html (I pasted in my personalized HTML landing page.)
Created a style.css file: sudo nano /var/www/html/style.css (Added custom styling for the landing page.)
5. Pushing My Website to GitHub
To back up my work and share it, I pushed the files to a GitHub repository:
Initialize Git:          git init
Link to remote repository:             git remote add origin https://github.com/username/portfolio.git
stage and commit the changes:               git add .
git commit -m "Initial commit"
Rename branch and push
git branch -M main
git push -u origin main

<img width="1871" height="877" alt="image" src="https://github.com/user-attachments/assets/8974dbe3-3008-4e17-960d-a6645c516f83" />
<img width="1881" height="884" alt="image" src="https://github.com/user-attachments/assets/85121b5c-f4a8-4a25-bc37-85d36f19d083" />

Public IP: http://3.252.139.233/
