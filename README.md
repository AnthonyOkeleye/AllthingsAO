Welcome to Anthony O's Landing Page

Set by set guide on server provisioning, web server setup and deploying a simple HTML page.   

*STEP 1: LUNCH EC2 INSTANCE* 
* Log into your AWS Console, Navigage to EC2 & click 'lunch Instance'
* Choose a suitable name for your Instance, advisable to select free tier eligible options under - AMI & instance type
* Create a key pair - choose a suitable name for your kep pair, download and sucurely store the .pem file.
* ![image](https://github.com/user-attachments/assets/f1476753-d569-4dfa-90dc-6d531e3482dc)

Ensure your instance has the right security group configuration as per below. - SSH (Port 22) only from your IP. 
![image](https://github.com/user-attachments/assets/1808535a-b8ec-466a-94ef-99007ea549b3)

*STEP 2 - SERVER CONFIGURATION - CONNECT TO THE INSTANCE AND INSTALL NGINX*
User your kep pair details and your public IPv4 address to SSH into your EC2 instance. 
ssh -i YOUR KEY PAIR NAME.pem ubuntu@YOUR-EC2-PUBLIC-IP
![image](https://github.com/user-attachments/assets/2b9b54d4-5bac-4972-8851-1bcd8db67c35)
Once you succesfully SSh into your instance, run the follow commands
sudo -i to change to root
sudo apt update
sudo apt upgrade
*OPTIONAL* - Rename your hostname using - vi /etc/hostname
Save and exit vim, exit the root & ubuntu.
Now SSH into ubuntu and your new hostname will appear. 
![image](https://github.com/user-attachments/assets/074a1298-7a2e-4cfe-b655-c27460270f66)

Run the below commands to install, start and enable nginx. 
sudo apt install nginx -y
sudo systemctl start nginx
sudo systemctl enable nginx

WEBSITE DEPLOYMENT - Follow command lines in the screenshots below. 
