# Compute in the Cloud
## Amazon Elastic Compute Cloud (EC2)
Those servers are virtual and the servers you use to gain access to virtual servers is called EC2
Using EC2 for compute is 
- highly flexible, 
- cost-effective
- quick  
** We compare it to running your own servers on premises in a data center that you own.
![image](https://user-images.githubusercontent.com/43639867/193493709-cc12f21a-4eb6-45d4-920b-c60c252d05de.png)

- Launch:
When you lanch any Server you will add the template like you need storage optamized server, on demand server etc.Then we will configure the EC2 Server,
These configurations include the operating system, application server, or applications. You also select the instance type, which is the specific hardware configuration of your instance. 
- Connect:
We can conncet through
  - SSH
  - RDP
 
 - Use:
 You can access that machine anywhere as its running on the server 24/7
 ## Amazon EC2 instance types
 - General purpose instances : provide a balance of compute, memory, and networking resources
 - Compute optimized instances : ideal for compute-bound applications that benefit from high-performance processors
 - Memory optimized instances : designed to deliver fast performance for workloads that process large datasets in memory
 - Accelerated computing instances :  use hardware accelerators, or coprocessors, to perform some functions more efficiently than is possible in software running on CPUs
 - Storage optimized instances : designed for workloads that require high, sequential read and write access to large datasets on local storage
 

## Amazon EC2 Pricing
On-Demand: short-term, irregular workloads that cannot be interrupted
Amazon EC2 Savings Plans : providing reduce price for 1 to 3 year terms
Reserved Instances : billing discount applied to the use of On-Demand Instances in your account.
Spot Instances : ideal for workloads with flexible start and end times, or that can withstand interruptions
Dedicated Hosts : physical servers with Amazon EC2 instance capacity that is fully dedicated to your use. 

## Scaling Amazon EC2
### Scalability
Scalability involves beginning with only the resources you need and designing your architecture to automatically respond to changing demand by scaling out or in. 
Within Amazon EC2 Auto Scaling, you can use two approaches: dynamic scaling and predictive scaling.

Dynamic scaling responds to changing demand. 

Predictive scaling automatically schedules the right number of Amazon EC2 instances based on predicted demand.

# Elastic Load Balancer
Automatically distributes incoming application traffic across multiple resources, such as Amazon EC2 instances.  if you have multiple Amazon EC2 instances, Elastic Load Balancing distributes the workload across the multiple instances so that no single instance has to carry the bulk of it. 

## Low-demand period
This means that the customer comes to the website, the less EC2 are used.

## High-demand period
More Users more EC2 like the date of result the more customers are comming the more EC2 are used.

# Monolithic Applications and Microservices
## Monolithic Applications
Tightly coupled Components Working Together are called Monotlithic application such as a website which request from database through api and take outputs from the Devices and each application is connected to each other.
## Microservices Applications
The Microservices applications are loosly coupled like the modules are connected but if one module is fail, but the system always working such as in metro if the card system fail the coins are working and the system works.

# Amazon Simple Notification Service (Amazon SNS)
- publish/subscribe service
- Will recieve notification.

# Serverless Computing
Its means that the maintaine of the servers  will done it by self, you need to upload the code to the servers.
flexibility to scale serverless applications automatically. Serverless computing can adjust the applications' capacity by modifying the units of consumptions, such as throughput and memory. 

## AWS Lambda
- Its an service used for serverless computing
-  run code without needing to provision or manage servers.
-  Charges apply only when your code is running.
![image](https://user-images.githubusercontent.com/43639867/193845388-da96a833-df53-4e99-b50c-cf139d606d7e.png)

- You upload your code to Lambda. 

- You set your code to trigger from an event source, such as AWS services, mobile applications, or HTTP endpoints.

- Lambda runs your code only when triggered.

- You pay only for the compute time that you use. In the previous example of resizing images, you would pay only for the compute time that you use when uploading new images. Uploading the images triggers Lambda to run code for the image resizing function.

## Containers
 standard way to package your application's code and dependencies into a single object. 
 ## Amazon Elastic Container Service (Amazon ECS)
 is a highly scalable, high-performance container management system that enables you to run and scale containerized applications on AWS. 
Amazon ECS supports Docker containers. **Docker** is a software platform that enables you to build, test, and deploy applications quickly. AWS supports the use of open-source Docker Community Edition and subscription-based Docker Enterprise Edition. With Amazon ECS, you can use API calls to launch and stop Docker-enabled applications.

 
