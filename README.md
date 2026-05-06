
🧠 What is Lift & Shift?
Lift & Shift (Rehosting) is a migration strategy where an application is moved from on-premises infrastructure to the cloud with minimal architectural or code modifications. 
This project demonstrates how legacy applications can be modernized gradually after migration to AWS.

🎯 Project Objectives

Host a traditional Java application on AWS


Improve scalability and availability


Eliminate infrastructure maintenance overhead


Use cloud-native networking and load balancing


Prepare the application for future modernization



AWS Services Used


* Amazon EC2


* Application Load Balancer (ALB)


* Auto Scaling Groups


* Route53


* AWS Certificate Manager (ACM)


* Amazon S3


* Security Groups


* IAM Roles & Policies


🏗️ Infrastructure Components

🌐 Frontend Layer

* Route53 manages DNS


* HTTPS enabled via ACM


* ALB distributes traffic across application servers


⚙️ Application Layer

* Apache Tomcat deployed on EC2


* Auto Scaling Group manages scaling


* Security Groups restrict access to port 8080


🗄️ Backend Layer
Separate EC2 instances host:

* MySQL Database


* RabbitMQ Message Broker


* Memcached Cache Server


* Private Route53 DNS is used for internal communication between services.

🔁 Deployment Flow

* Create AWS infrastructure


* Configure Security Groups


* Launch backend EC2 instances


* Launch Tomcat application servers


* Build application using Maven


* Upload artifact to S3


* Deploy WAR file to Tomcat


* Configure Load Balancer


* Enable HTTPS using ACM


Configure Route53 DNS


* Validate deployment



📁 Project Structure
.├── ansible/              # Configuration management├── src/                  # Application source code├── userdata/             # EC2 bootstrap scripts├── pom.xml               # Maven configuration├── Jenkinsfile           # CI/CD pipeline└── README.md

🛠️ Prerequisites


AWS Account


AWS CLI configured


Java 17+


Maven


Git


🌐 Access the Application
After deployment:
http://https://vprofileapp.tcapp.xyz/

🔐 Security Architecture


Backend services run in private subnets


Only ALB can communicate with Tomcat instances


Security Groups enforce least privilege access


HTTPS enabled using ACM certificates



⚠️ Common Issues
404 from Load Balancer


Verify Target Group health checks


Ensure application is deployed as ROOT.war


Confirm Tomcat is listening on port 8080



ECS / Tomcat Not Reachable


Verify Security Group rules


Check ALB listener configuration


Confirm instances are healthy



Backend Connection Failures


Verify private Route53 DNS entries


Confirm backend EC2 security groups allow traffic



🔮 Future Improvements


Terraform Infrastructure as Code


ECS / EKS migration


CI/CD automation with Jenkins


Docker containerization


Monitoring with CloudWatch


Blue/Green deployments



🎯 Skills Demonstrated


AWS Infrastructure Deployment


Lift & Shift Cloud Migration


EC2 & Networking


Load Balancing & Auto Scaling


Multi-tier Architecture


DevOps Fundamentals


Linux Administration



📚 Key Takeaways
This project demonstrates how traditional applications can successfully migrate to AWS using a Lift & Shift strategy while improving:


Scalability


Availability


Reliability


Security


Operational efficiency



🙌 Author
Tina Collins

⭐ Portfolio Value
This project showcases:


Cloud migration experience


AWS architecture knowledge


Infrastructure deployment skills


Real-world DevOps workflows

