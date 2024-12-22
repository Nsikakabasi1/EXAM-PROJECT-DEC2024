STEP BY STEP DOCUMENTATION OF THE PROVISIONED AWS-APACHE SERVER
===============================================================
PUBLIC ADDRESS  OF PROJECT WEBSERVER - 174.129.170.113
===============================================================
STEP(1) An AWS account was created.
STEP(2) A AWS-VPC was created.
STEP(3) Ec2- Elastic Compute Cloud was created.
Compare instance types
Amazon EC2 provides a wide selection of instance types optimized to fit different use cases. Instances are virtual servers that can run applications. They have varying combinations of CPU, memory, storage, and networking capacity, and give you the flexibility to choose the appropriate mix of resources for your applications. Learn more about instance types and how they can meet your computing needs.

Launch an instance
  Info
Amazon EC2 allows you to create virtual machines, or instances, that run on the AWS Cloud. Quickly get started by following the simple steps below.

STEP(4)
Key pair (login) Info
======================
You can use a key pair to securely connect to your instance. Ensure that you have access to the selected key pair before you launch the instance.
Choose an Amazon Machine Image (AMI)
Cancel
An AMI is a template that contains the software configuration (operating system, application server, and applications) required to launch your instance. You can select an AMI provided by AWS, our user community, or the AWS Marketplace; or you can select one of your own AMIs.
=============================================
Summary
Number of instances Info
Software Image (AMI)
Ubuntu Server 24.04 LTS (HVM),...read more
ami-0e2c8caa4b6378d8c
Virtual server type (instance type)
t2.micro
Firewall (security group)
New security group
Storage (volumes)
1 volume(s) - 8 GiB

==============================================
STEP(5)
ec2 CONNECT TO UBUNTU 
#LINUX CODES THAT WAS USED TO INSTALL APACHE2 SERVER, ETC
sudo su -
sudo apt update
sudo apt list --upgradeable
sudo apt upgrade
sudo apt-get install lamp-server
OR
sudo apt-get install apache2 php mysql-server
sudo apt install php-cli
sudo apt install php-pdo
sudo apt install php-fpm
php -v
sudo systemctl reload apache2
sudo systemctl restart apache2

========================================================

STEP(6)
USE FILEZILLA AS FTP TOOL TO TRANSFER FILES TO SERVER.

STEP(7)
HTTP PORT 80 FOR IPV4 ADDRESS 174.129.170.113
															================

STEP(8)
CONFIG OF APPLICATION LOAD BALANCER.
AddListeners-  Editlistener- Listeners and rules
HTTP:80  - RedirectToURL  - https:443
HTTPS:443 - ForwardTotargetGroups - TargetGroup - selectedcertificate