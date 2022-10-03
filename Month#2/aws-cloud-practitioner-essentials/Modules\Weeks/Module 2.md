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

 
 
