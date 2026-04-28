**Full Stack Auto Scaling Web Application on AWS**
 Project Overview

This project demonstrates how to deploy a highly available and scalable full-stack web application using Amazon Web Services.
The system automatically adjusts computing resources based on user demand using Auto Scaling, ensuring performance and cost optimization.

The architecture combines EC2-based frontend hosting with scalable backend services, enabling the application to handle varying traffic loads efficiently.

 **Key Features**
Automatic scaling of servers based on traffic
High availability across multiple instances
Load balancing for efficient traffic distribution
Cost optimization using dynamic resource allocation
Fault-tolerant infrastructure
Seamless user experience under heavy load

 **Architecture**
 
🔹 Components
1. Compute Layer
Amazon EC2
Hosts frontend and backend application
Instances are dynamically created and terminated
2. Auto Scaling
AWS Auto Scaling
Automatically adjusts the number of EC2 instances
Maintains desired capacity
3. Load Balancer
Elastic Load Balancing
Distributes incoming traffic evenly across instances
Ensures no single server is overloaded
4. Launch Template
Defines configuration for EC2 instances
Includes AMI, instance type, security groups
5. Monitoring
Amazon CloudWatch
Monitors CPU usage, traffic, and system health
Triggers scaling actions
6. Database Layer
Amazon RDS or DynamoDB
Stores application data securely

 **Application Workflow**
User accesses the application via public URL
Request is sent to Load Balancer
Load Balancer forwards request to available EC2 instances
Instances process request and interact with database
CloudWatch monitors system performance
Auto Scaling adjusts number of instances:
High load → Adds instances
Low load → Removes instances
Response is sent back to the user
 **Setup Instructions**
 
1️⃣ Launch EC2 Instance
Install application and dependencies
Configure web server (Nginx/Apache)

2️⃣ Create AMI
Create image from configured EC2 instance

3️⃣ Create Launch Template
Select AMI
Configure instance type and security groups

4️⃣ Create Load Balancer
Choose Application Load Balancer
Configure target group

5️⃣ Create Auto Scaling Group
Attach Launch Template
Set:
Minimum instances: 2
Maximum instances: 5
Desired capacity: 2

6️⃣ Configure Scaling Policy
Example:
CPU > 70% → Scale Out
CPU < 30% → Scale In

** Frontend**
Hosted on EC2 instances
Built using HTML, CSS, JavaScript
Accessible via Load Balancer DNS

** Backend**
Runs on EC2 or serverless services
Handles business logic and API requests
🛠️ Technologies Used
HTML, CSS, JavaScript
Python / Node.js
AWS EC2
AWS Auto Scaling
Elastic Load Balancing
CloudWatch
RDS / DynamoDB
**Advantages**
✔ High Availability
✔ Scalability
✔ Cost Efficiency
✔ Fault Tolerance
✔ Improved Performance
🏁 Conclusion

