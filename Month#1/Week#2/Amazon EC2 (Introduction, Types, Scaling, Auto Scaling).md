# Amazon EC2

## Introduction
Its an AWS Elastic Cloud Compute which contains the cloud virtual machines acting like a server.
We can increase or decrease the resources easily.
### For Configuring the EC2 Instance
1. Select the Operating System
2. Select the Memory and Harddisk and the CPU
3. Configure the Network and create the SSH or Password for login **(SSH recommended)**
4. Connect via Public IP.

## Types of EC2 Instances
### General Purpose
1. Balenced Resources
2. Example for the General Purpose are 
 - Hosting of Web Services
 - Sharing Codes Repo like Github
 - Value for Small Company
 
 
### Compute Optimized
1. Its used for those servers which contains high load
**For Example**
Result Website at the date of Results Announced and many people view their results at the same time.
### Memory Optamized
1. These Server contains the Large Amount of Data Set and mainly used for train the Machine Learning Algorithms and the Big Data.
2. This server will process the data and then send to the Computer Program.
### Accelerated Computing
1. This type use hardware accelerators for boosting the data processing. 
2. Thses are best for graphics applications and streaming like Gaming Streaming or BroadCasting.
### Storage Optamized
1. This type is best when you have large datasets (Big Data) on local storage.
2. These are designed to deliver many inputs as fast as possible. Like every sec transactions done from 1 bank to another those banks need the large amount of storage for saving the transaction log,data. 


## Scaling
Scaling means that adding/removing resources when its required
Now the AWS allow to pay per minutes means that if resources are added when thier is load on the server its add bill to the account and when server is free its automatically go to gerneral configuration (in terms of resources) that we have used when creating EC2.

## Auto Scaling
AWS EC2 Auto Scaling allows you to add or remove EC2 instances automatically.
Used for handling large amount of Requests and Server Timeouts.
### Dynamic Scaling
When demand increases resources increases, when demand decreases resources decreases.

### Predictive scaling
schedules the number of instances based on a predicted demand

- These approaches are used at the same time for scaling faster.
