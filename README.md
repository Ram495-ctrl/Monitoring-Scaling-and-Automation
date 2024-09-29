# Monitoring-Scaling-and-Automation
Monitoring, Scaling and Automation git hub repo - https://github.com/Ram495-ctrl/Monitoring-Scaling-and-Automation.git

Develop a system that automatically manages the lifecycle of a web application hosted on EC2 instances, monitors its health, and reacts to changes in traffic by scaling resources.  Furthermore, administrators receive notifications regarding the infrastructure's health and scaling events. 

Detailed Breakdown: 

1. Web Application Deployment: 
 - Use `boto3` to: 
 - Create an S3 bucket to store your web application's static files. 
 - Launch an EC2 instance and configure it as a web server (e.g., Apache, Nginx).  - Deploy the web application onto the EC2 instance. 
2. Load Balancing with ELB: 
 - Deploy an Application Load Balancer (ALB) using `boto3`. 
 - Register the EC2 instance(s) with the ALB. 
3. Auto Scaling Group (ASG) Configuration: 
 - Using `boto3`, create an ASG with the deployed EC2 instance as a template. 
 - Configure scaling policies to scale in/out based on metrics like CPU utilization or network traffic. 
4. SNS Notifications: 
 - Set up different SNS topics for different alerts (e.g., health issues, scaling events, high traffic). 
 - Integrate SNS with Lambda so that administrators receive SMS or email notifications. 
5. Infrastructure Automation: 
 - Create a single script using `boto3` that: 
 - Deploys the entire infrastructure. 
 - Updates any component as required. 
 - Tears down everything when the application is no longer needed. 
6. Optional Enhancement – Dynamic Content Handling: 
 - Store user-generated content or uploads on S3. 
 - When a user uploads content to the web application, it gets temporarily stored on the  EC2 instance. A background process (or another Lambda function) can move this to the S3  bucket and update the application's database to point to the content's new location on S3. 

execution: Create boto3 code and execute


  ![image](https://github.com/user-attachments/assets/20fbc73a-4ad6-4862-8613-b19eefb3f673)
  
1.  EC2 created- Ram_webserver1

  ![image](https://github.com/user-attachments/assets/5fcad376-3628-484c-9027-78827810b34e)

  Index file create in /var/www/html/
  
  ![image](https://github.com/user-attachments/assets/437a13c4-2328-42a0-b2fa-577fb8e97e16)


2. Load balancer-Ramwebapp-lb1
   
![image](https://github.com/user-attachments/assets/3c4a7d64-f92b-40c6-9656-5cacaf2e61b3)

3. ASG created – Ram_ASG

![image](https://github.com/user-attachments/assets/11f40bfa-deef-4df1-9011-f5961770cba0)

4. SNS Notifications:

 ![image](https://github.com/user-attachments/assets/6c547212-e301-43d0-9b64-0e626aae9474)

 ![image](https://github.com/user-attachments/assets/fea8c00b-ad02-4b58-aa95-7f650352ed4d)

 5. Infrastructure Automation:

Tears down everything when the application is no longer needed. Run the delete.py to delete the application

![image](https://github.com/user-attachments/assets/d1c2b199-f088-4d39-b326-4fc1e72176a5)

<h1> Rama Srinivas </h1>

Check the detailed test results and instructions in the (Monitoring, Scaling and Automation_Doc) Documentation which is loacated in Monitoring-Scaling-and-Automation repo




 



   
  


