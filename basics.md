
different types of cloud computing models that are available:
---------------------------------------------------------------
 Infrastructure as a service (IAAS):  So if we want to launch a Linux server and, we want to manage that Linux server ourselves, that is how we would do that as infrastructure as a service and we would do that using the Elastic Compute cloud or EC2 service. 

Platform as a service or (PaaS):  that's where AWS will take a little bit more control over the underlying infrastructure. AWS manages their underlying infrastructure and the hardware and operating system normally and, a good example of that would be the relational database service and, in that service AWS they provision all the operating system, the server and everything to run that but, you still need to do the high-level administration of that database

Software as a service(SaaS):  that is a complete product that normally runs in a browser and it mostly refers to end-user applications. A good example that would be Office 365 or salesforce.com, 

serverless computing: That allows you to build and run applications without having to think about servers. You don't need to provision the server yourself AWS will do that for you. It's also referred to as function as a service or abstract services. Examples of that are the simple storage service .

Cloud computing models provided by AWS:
----------------------------------------------
 1. Infrastructure as a service (IAAS) --> Example: VPC, EC2, EBS
 2. Platform as a service (PAAS) --> Example: RDS, EMR, Elastic Search
 3. Software as a service (SAAS) --> Example: Web-based email, Office 365, Salesforce. com
 4. Function as a service (FAAS)/Abstracted services --> Server less computing --> AWS allows you to build and run application and services without thinking about servers. 
	|--> Example: S3, AWS Lambda, AWS DynamoDB, AWS SNS (Amazon simple notification service they can send out notifications to your users.)

storage services that are available on AWS:
--------------------------------------------- 
Amazon simple storage service or (S3) for short:   It's designed to store and access any type of data over the Internet. It's a serverless service and as such we don't need to worry about what is behind it. There's obviously a file server an operating system a hard drive but we don't need to be concerned about that at all. We just simply need to create this thing called a bucket and then we upload objects to that bucket, the bucket grows as we add objects to it and the size of that bucket is theoretically unlimited. AWS just looks after everything for us.

Amazon Glacier : 	 is the cheapest storage option on AWS and it's used for long-term archiving of data. It's a serverless service just like Amazon s3 but it is not as readily accessible as s3 so it should only be used for content that 
is to be archived. You can also set up a lifecycle rule that will automatically migrate old data in Amazon s3 automatically over to Glacier for long-term archiving. 

Amazon elastic block store or EBS for short:  	 is a highly available, low latency block storage and it's specifically for attaching to servers that are launched with the Amazon ec2 service and it's similar to attaching a hard drive to 
your computer at home, works in the same manner. 

Amazon Elastic file system or EFS for short:  	 is network attached storage and it's specifically for Amazon EC2 servers. Because it is network attached store, this allows multiple servers to access one data source in a similar way to NAS on your network at home can be accessed by multiple computers on that network. 

The AWS Storage Gateway:  	 enables hybrid storage between on-premise environments(onsite datacenter of a company ex: icici banck/etc) and the AWS cloud. It provides a low latency performance by caching frequently used data on-premises while storing the less frequently data in Amazon Cloud storage services. 

A Snowball device:  is a portable, petabyte scale, data storage device that can be used to migrate data and large amount of data from on-premise environments over to the AWS cloud. You simply download your data to the Snowball device, then you send it off to AWS who will then upload that data to an AWS storage service for you. 

AWS- Storage Services:
-------------------------
1. Simple storage service (S3) ? ( long time access
2. Glacier ( for content archiving ) ?
3. EBS( Elastic Block Store ) ? used in EC2 instance
4. Elastic File System (EFS) ? ( network attached storage
5. AWS Storage Gateway ? ( act as a bridge between AWS --> Onsite Datacenter ) 
6. Snowball ?

Storage Example:
-----
![image](https://user-images.githubusercontent.com/33980623/116887458-f3ed4200-ac47-11eb-9657-32aad2c6fbbc.png)

AWS 
  |--> Created VPC
    |--> Launched 2 Servers
	    |--> Attached to Amazon EBS storage
	      |--> to share the data among server created need EFS(Elastic File System) Mount Target ---->DataSource EFS Share(NAS)

VPC: Virtual Private Cloud is our own Virtual private space with in AWS Cloud. Its highly secure space where no one is allowed until the VPC owner give permission to external world. 

endpoint --> S3 Bucket --> Glacier

![image](https://user-images.githubusercontent.com/33980623/116903487-19834700-ac5a-11eb-9726-ae89ba95cfea.png)



