IAM: Identity Access management 
--------------------------------

Q. What is CloudComputing & Different CloudComputing platforms?
Q. What is AWS-Global-Infrastucture?
Q. What is Root & IAM user?
Q. What is IAM User, Group, Role, Policy ? 
Q. What is an IAM Role ? 
Q. Types of Policies ?
Q. What is AccessKeys?
Q. SSH key for CodeCommit?


VPC: Virtual Private cloud
--------------------------------
### Q. What is VPC?
Amazon Virtual Private Cloud (Amazon VPC) enables you to provision a logically isolated section of the AWS Cloud where you can launch AWS resources in a virtual network that you've defined.

### Q. What is Amazon VPC IP Address Manager?
Amazon VPC IP Address Manager (IPAM) automates your IP address management workflows. This includes assigning, tracking, troubleshooting, and auditing IP addresses across AWS Regions and accounts throughout your AWS Organization.

### Q. What is Subnets?
A subnet is a range of IP addresses in your VPC. After creating a VPC, you can add one or more subnets in each Availability Zone. You launch AWS resources, such as Amazon EC2 instances, into your subnets. You can connect a subnet to the internet, other VPCs, and your own data centers, and route traffic to and from your subnets using route tables.

### Q. What is Route tables?
A route table contains a set of rules, called routes, that are used to determine where network traffic from your subnet or gateway is directed.


### Q. What is Internet Gateway?
An internet gateway is highly available VPC component that enables communication between your VPC and the internet. To use an internet gateway, attach it to your VPC and specify it as a target in your subnet route table for internet-routable IPv4 or IPv6 traffic. An internet gateway performs network address translation (NAT) for instances that have been assigned public IPv4 addresses.

### Q. What is AWS Transit Gateway?
AWS Transit Gateway connects your VPCs and on-premises networks through a central hub.

### Q. What is AWS PrivateLink?
AWS PrivateLink establishes private connectivity between VPCs and services hosted on AWS or on-premises, without exposing ata to the internet.

### Q. What is DHCP?
### Q. What is Elastic-IP?
An Elastic IP address is a static IPv4 address designed for dynamic cloud computing. An Elastic IP address is allocated to your AWS account, and is yours until you release it. An Elastic IP address is a public IPv4 address, which is reachable from the internet. If your instance does not have a public IPv4 address, you can associate an Elastic IP address with your instance to enable communication with the internet.

### Q. What is NAT Gateway?
NAT gateway enable instances(EC2) in a private subnet connect to services outside your VPC. it also prevent such external services from initiating a connection with those instances. There are two types of NAT gateways: 

**public NAT Gateway:** A public NAT gateway enables instances in private subnets to connect to the internet, but prevents them from receiving unknown inbound connections from the internet. You should associate an **elastic IP address with a public NAT gateway** and attach an **internet gateway to the VPC** containing it.

**private NAT Gateway:** A private NAT gateway enables instances in private subnets to connect to other VPCs or your on-premises network but prevents any unknown inbound connections from outside your VPC. You can route traffic from the NAT gateway through a transit gateway or a virtual private gateway.

### Q. Difference between NAT Gateway and Internet Gateway?


### Q. What is Network ACL?
A network access control list (ACL) is an optional layer of security for your VPC that acts as a firewall for controlling traffic in and out of one or more subnets.

### Q. What is Security Group?
A security group acts as a virtual firewall that controls the traffic for one or more instances. When you launch an instance, you can specify one or more security groups. 

### Q. What is Endpoint & Endpoint Service?
A VPC endpoint enables connections between a virtual private cloud (VPC) and supported services, without requiring that you use an internet gateway, NAT device, VPN connection, or AWS Direct Connect connection. Therefore, your VPC is not exposed to the public internet.

### Q. What is VPC Endpoint?
A VPC endpoint enables you to privately connect your VPC to supported AWS services like Amazon S3. VPC endpoints enable you to create an isolated VPC that is closed from the public internet. In addition, there is no additional charge for using gateway endpoints.

### Q. What is Customer Gateway?

### Q. What is Vitual Private Gateway?

### Q. What is Site-to-Site VPN connection?

### Q. What is dual stack mode?
Your VPC can operate in dual-stack mode. This means that your resources can communicate over IPv4, IPv6, or both IPv4 and IPv6.



EC2: Elastic Compute cloud
-------------------------------
### Q. how do you access ec2 console?

Q. how do you check all region/zone instances running on aws cloud? 
ec2 Global view

Q. what is instace Events and Volume Events?
Instace Events: AWS can schedule events for your instances, such as a reboot, stop/start, or retirement. Depending on the event, you might be able to take action to control the timing of the event.

Volume Events: When Amazon EBS determines that a volume's data is potentially inconsistent, it disables I/O to the volume from any attached EC2 instances by default. This causes the volume status check to fail, and creates a volume status event that indicates the cause of the failure.

Q. Limits of AWS resource usage details?
we can see the details in the ec2 services where you can see "Limits" option, there we can see the details

Q.  In general what type of instace type is used for E-commerce application?

Q. How to launch and ec2 instance? 
Goto ec2 service --> launch instance --> select AMI types --> Instance types (C5/M5/R5) 

Q. what is CloudWatch ?
CloudWatch monitors metrics for one of your instances. CloudWatch will automatically send you a notification when the metric reaches a threshold that you specify. For each alarm, you must specify the thresholds to monitor and the actions to take when the alarm is triggered. You can also configure the alarm to send an email notification when it is triggered.
