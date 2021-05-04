
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

endpoint --> S3 Bucket --> Glacier

VPC: Virtual Private Cloud is our own Virtual private space with in AWS Cloud. Its highly secure space where no one is allowed until the VPC owner give permission to external world. 

Hybrid Storage Example:
------------------------

S3 bucket with Objects --> AWS Storage Gateway -->  corporate data center (onsite storage)


![image](https://user-images.githubusercontent.com/33980623/116903487-19834700-ac5a-11eb-9726-ae89ba95cfea.png)


different options that are available for running databases on AWS:
------------------------------------------------------------------

The relational database service or RDS for short:    is a fully managed database service that makes it easy to launch database servers in the AWS cloud and scale them when required. The RDS service can launch servers for mySQL including variations of the mySQL database engine with MariaDB and Amazon's own enterprise version of mySQL Amazon Aurora. Standard Postgre SQL is also available and also available as Amazon's Enterprise Aurora Postgre SQL. Microsoft SQL server and Oracle are also available. 

Amazon DynamoDB is : AWS's NoSQL database as a service. It's a serverless service like Amazon S3 and as such you don't need to worry about the underlying infrastructure behind it. AWS takes care of everything for you and it provides high speed extremely low latency performance. 

Amazon Redshift is:  a fast fully managed petabyte scale data warehouse that is based upon the postgre SQL database engine. If you're looking for a big data storage solution Redshift is perfect for this. 

Amazon ElastiCache is: an in-memory data store or cache in the cloud. It allows you to retrieve information from fast fully managed in-memory caches instead of relying on slower disk based databases. 

The AWS database migration service or DMS orchestrates a migration of databases over to AWS easily and securely. It can also migrate data from one database engine type to another totally different database engine type, for example you can use it to migrate from Oracle over to Amazon Aurora. 

Amazon Neptune is:  a fast reliable fully managed graph database service it has a purpose-built high performance graph database engine optimized for storing billions of relationships and clearing the graph with millisecond latency. 

![image](https://user-images.githubusercontent.com/33980623/117020865-717e8400-ad14-11eb-9218-4b3a2a203712.png)

real-life example: 
------------------
we've got our corporate data center and inside of our corporate data center we've got an on-site Oracle database. Now let's just say that Oracle database, it's old, it's worn out, it's outgrown its capacity and it needs to be replaced. Now you've done a total cost of ownership analysis on the situation and you've identified that it is far more cost effective to host that database on the aws cloud. 

So the first thing that you are going to want to do is to launch an RDS database instance. Now let's say you want to further reduce your cost by not having to pay for the Oracle licensing fee and what you can do is that you can launch an Amazon Aurora database instance and that will be running either the Mysql or the Postgresql open source database engines and by doing that you're not going to be paying for a licensing fee. The disadvantage of that is that some of the fields of data that are located in that Oracle database may not be compatible with the Amazon Aurora Mysql or Postgresql fields. what you're going to need to do is that when you take that data out of your Oracle database, you're going to have to change it and manipulate it to suit the amazon aurora database, and that is where the aws database migration service comes in.

You can define a database migration workflow by specifying the source database, the target database and any operations on that data that need to occur during that migration of that data. Once you've done that you can then run the database migration job and that will look after everything for you. It will migrate that data from that on-site oracle database to your amazon aurora database and at the same time it will be giving you feedback through the aws management console, as a dashboard, on the performance of how that job is actually going, because that job could take hours, it could take days, it could take weeks, depending on how big your oracle database is and how fast your connection to the aws cloud is, and it will also give you feedback of any errors and alert you to any problems that may occur. 

Once our RDS instance is up and running and the data has been migrated over, then we can look at launching a web server that can receive traffic and requests from the outside world over the internet and then get that data that is required from the RDS database and then return that back to the requester. 

Now let's just say we're getting a lot of requests from the outside world and a lot of that is for the same data. What we can look at doing is getting all of our regularly accessed content and putting it into an Elasticache node and, because the Elasticache node is serving those requests from its memory, not from a solid-state drive, as is the case of the rds service, it will be returning that very quickly and it will be at a lower cost. Now we need to take into consideration that the costs of storing data in memory is more expensive than storing that data on a solid state drive and so we need to make sure that Elasticache node only contains regularly accessed data. So the way that we would do that is that requests would come in from the outside world to the web server, the web server could then check to see whether that data is in the Elasticache node. If it is or if it is in the Elasticache node it will simply grab that data and then forward it back to that requester. 

Let's just say a request comes in and that data is not in the Elasticache node. So then the web server will go to the RDS database instance, it will get that data if it's there and after it has got that data, it will then write that data into the Elasticache node, and at the same time it will define a time to live or a ttl for that specific data, and once that ttl has expired, if there are no further requests for that data within that ttl, then that data will be removed automatically by the Elasticache service from the Elasticache node, and by doing that, all of that data that's in the Elasticache node will be regularly accessed data that has been accessed within that time to live period. Now let's just say a request comes into that web server for either writing to or deleting from that RDS database. So the way that would work is that the request would come into the web server the web server would then either delete or write to the RDS database. If it is deleting from the database then it would also delete from the Elasticache node as well. If it's writing to the database then it would also write to the Elasticache node and again it would define a time to live period, so that if that data is not requested within that time to live period then it will automatically be removed from the Elasticache node by the Elasticache service.



networking and content & delivery services:
----------------------------------------------

Amazon CloudFront: 
is a global content delivery network or cdn for short that securely delivers your frequently requested content to over 100 edge locations across the globe and by doing this it achieves low latency and high transfer speeds for your end users. It also provides protection against DDOS attacks. 

Amazon virtual private cloud or VPC:
lets you provision a logically isolated section of the AWS cloud and you can launch AWS resources in that virtual network that you yourself define and this is your own personal private space within the AWS cloud and no one can enter it unless you allow them to enter it. 

AWS direct connect:
is a high-speed dedicated network connection to AWS. Enterprises can use it to establish a private connection to the AWS cloud in situations where a standard internet connection won't be adequate. 

AWS elastic load balancing or ELB: ELB is automatically distributes incoming traffic for your application across multiple EC2 instances and also in multiple availability zones. So if one availability zone goes down, the traffic will still go to the other availability zone and your application will continue to deliver responses to requests. It also allows you to achieve high availability and fault tolerance by distributing traffic evenly amongst those instances and it can also bypass unhealthy instances. 

Amazon Route 53: 
is a highly available and scalable domain name system or DNS for short and it can handle direct traffic for your domain name and direct that traffic to your back-end web server. 

Amazon API gateway: 
is a fully managed service that makes it easy for developers to create and deploy secure application programming interfaces or API at any scale. It handles all of the tasks involved in accepting and processing up to hundreds of thousands of concurrent API calls. It's a serverless service and as such you don't need to worry about the underlying infrastructure AWS looks after everything for you. 

![image](https://user-images.githubusercontent.com/33980623/117042447-9cbf9e00-ad29-11eb-90e4-e9e1357a1104.png)

real-life example: 
------------------
how we can use these networking services of AWS. So here we've got the architecture that we looked at before in the compute section but one thing we didn't mention was availability zones. So let's just say that we've launched that architecture in a single availability zone. What happens if that availability zone goes down? What happens to our traffic? Our traffic has nowhere to go and our application stops delivering responses to requests. 

That is why it's always desirable to have our architecture distributed across multiple availability zones. That way if one availability zone goes down the other one will continue to operate and the infrastructure within that other availability zone will continue to respond to requests. We can launch EC2 instances in multiple availability zones and our elastic low balancing service can distribute that traffic across multiple availability zones as well. So if one availability zone goes down the elastic load balancer will continue to distribute traffic to the availability zone that is still healthy and to those instances in that availability zone that are still healthy as well. 

So let's just say our application running on these EC2 instances is a wordpress web server and that contains lots of images and lots of video that is static content, it's not really changing that much and it's not efficient for us to continue to keep delivering that from our EC2 instances. We would like somewhere to put that where it can be delivered with high speed and low latency and to take the load off our EC2 instances. That is where the CloudFront content delivery network or CDN comes in. 

So we can get these large images and large videos that are not really changing that often and we can put that in a CloudFront distribution and CloudFront will cache that and distribute that across hundreds of edge locations across the globe. So when your end user requests that video or those images, it will be delivered to them with really high speed and low latency and at the same time it's going to take the load off your EC2 instances and is going to significantly reduce your costs at the same time.

Dynamic content that is changing regularly, CloudFront can forward those requests over to the elastic load balancer which will then forward them to an EC2 instance. So that way you have the best of both worlds. You have dynamic content delivered as a dynamic content and at the same time you have these large videos and images that aren't really changing that often delivered very rapidly. Now that CloudFront service or that CloudFront distribution will have its own DNS name that we can put into a browser and we can directly access that. 

The problem with that is that that DNS name for that CloudFront distribution will be something very complicated and just won't mean anything to our end user at all. So we would prefer to have our end user type in a domain name and have the request for that domain name forwarded to that CloudFront service. That is where route 53 domain name service can come in. 

So route 53 will grab those requests for your domain example.com and it will forward those requests over to the CloudFront service and the CloudFront service will handle it from then on. So let's just say we work for a large enterprise that has its own corporate data center and the reason it's got its own corporate data center is because that is located where the employees work and we don't want our employees to be slowed down by a network. We want them to be able to work efficiently but at the same time we have resources on the AWS cloud that those employees also need to access. So we need some way of having a high speed connection between our corporate data center and the AWS cloud and that is where the AWS direct connect service comes in

So route 53 will grab those requests for your domain example.com and it will forward those requests over to the CloudFront service and the CloudFront service will handle it from then on. So let's just say we work for a large enterprise that has its own corporate data center and the reason it's got its own corporate data center is because that is located where the employees work and we don't want our employees to be slowed down by a network. We want them to be able to work efficiently but at the same time we have resources on the AWS cloud that those employees also need to access. 

So we need some way of having a high speed connection between our corporate data center and the AWS cloud and that is where the AWS direct connect service comes in and that can provide a very high speed fibre optic network between our corporate data center and the AWS cloud and that is completely private. Okay, so that's a very complicated architecture. As an associate level certification that 
