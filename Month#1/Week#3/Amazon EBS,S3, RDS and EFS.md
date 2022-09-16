# Amazon S3
Amazon Simple Storage Service (Amazon S3) is the Object storage service that has the data encryption, scalability, security and performance.
Amazon S3 provides management features so that you can optimize, organize, and configure access to your data to meet your specific business, organizational, and compliance requirements.

Storage upto 5 TB.

## Features of Amazon S3
### Storage Management
1. Manage Cost
2. Reduce Latency
3. Save Multiple Distinct Copies of the data

1. **S3 Lifecycle**-Create Policy for the Object and Store in the cost effective way over the lifecycle. If the Object expiration is reach to the end of the lifecycle its moved to the other S3 class.
2. **S3 Object Lock**- Send Warning/Prevent us if we delete or owerrite the Object for a fixed amount of time or the indefinite time.
Its help us to meet the requirements for (WORM) which means its readonly for many times after writting 1 time. (Additional Layer for prevention.)
3. **S3 Replication**- Saving Object Data and its meta Data on the one or more AWS Regions for the latency and security purpose
4. **S3 Batch Operations**- Perform operations such as Copy, Invoke AWS Lambda function, and Restore on millions or billions of objects.Manage the Objects with the Single Click.

### Access Management
Provides features for auditing and managing access to buckets and objects. For Accessing the other buckets and Objects we need permission for that AWS Reources.
1. **S3 Block Public Access** – Block public access to S3 buckets and objects. By default, Block Public Access settings are turned on at the account and bucket level.
2.  **AWS Identity and Access Management (IAM)** uage to configure resource-based permissions for your S3 buckets and the objects in them.
3.  **Amazon S3 access points**  – Configure named network endpoints with dedicated access policies to manage data access at scale for shared datasets in Amazon S3.



### Data Processing:
Transform data and trigger workflows to automate a variety of other processing activities at scale.

1. **S3 Object Lambda** – Add own code to S3 GET requests to modify and process data as it is returned to an application. Filter rows, dynamically resize images, redact confidential data, and much more.
2. **Event notifications** – Trigger workflows that use Amazon Simple Notification Service (Amazon SNS), Amazon Simple Queue Service (Amazon SQS), and AWS Lambda when a change is made to S3 resources.



### Storage logging and monitoring
Provides logging and monitoring tools that you can use to monitor and control how your Amazon S3 resources are being used. 
1. **Amazon CloudWatch** (track operational health of S3 resources and configure billing alerts) 
2. **AWS CloudTrail** (provide you with detailed API tracking for S3 bucket-level and object-level operations) 
These are  the 2 Automated monitoring tools while Server access logging (detailed records for the requests made to a bucket) and AWS Trusted Advisor (evaluate account to optimize AWS infrastructure, improve security and performance, reduce costs, and monitor service) are the 2 Manual monitoring tools.

### Analytics and insights
Helps gain visibility into storage usage, which empowers to better understand, analyze, and optimize storage at scale.

### Strong consistency
Provides strong read-after-write consistency for PUT and DELETE requests of objects in S3 bucket.


# Amazon EFS
- Amazon Elastic File System popularly known as AWS EFS is a simple and serverless elastic file system built to scale on demand without disruptions and with automatic shrinking due to files. 
- No provison or management of capacity for growth and simple interface to create files quickly. 
- It manages all the file storage infrastructure for you abd you only pay for storage used by your files with no minimum fee or setup cost. Amazon EFS offers a range of storage classes designed for different use cases. These include:

 1. **Standard storage classes** – EFS Standard and EFS Standard–Infrequent Access (Standard–IA), which offer multi-AZ resilience and the highest levels of durability and availability.
 2. **One Zone storage classes** – EFS One Zone and EFS One Zone–Infrequent Access (EFS One Zone–IA), which offer customers the choice of additional savings by choosing to save their data in a single Availability Zone. Features of EFS are as following:

    - Automatic scalability.
    It can be used with multiple EC2 instances and across availability zones.
    - High throughput supports heavy workloads.
    It is a complete managed service.
    
   # EBS vs. EFS vs. S3
   ![S3-vs-EBS-vs-EFS-2048x1293](https://user-images.githubusercontent.com/43639867/190598106-76ac570b-72eb-4c42-a8c8-956b5c03fc4c.png)
# Amazon RDS
- RDS is used for storing traditional relation data. The RDS support a large number of database engines. 
- The data is well structured, Simple to Operate, Scale and Maintain

## Features and Benifits of Amazon RDS

  - SQL type of database.
  - Can be used to perform complex queries and joins.
  - Easy to set up, highly available, fault-tolerant and scalable.
  - Used when data is clearly defined.
  - Used for Online Stores and Banks.
  - Well Structured Data

## Amazon RDS Databases List

    - SQL Server.
    - Oracle.
    - MySQL Server.
    - PostgreSQL.
    - Aurora.
    - MariaDB.
    
 ## Amazon RDS Service
 AWS Provides some special services to RDS instances. This forces people to use the AWS RDS service instead of installing the database into EC2 instances. The RDS service includes the following:

    1. Security and patching of the DB instances.
    2. Automated backup for the DB instances.
    3. Software updates for the DB engine.
    4. Easy scaling for storage and compute.
    5. Multi-AZ option with synchronous replication.
    6. Automatic failover for Multi-AZ option.
    7. Read replicas option for read-heavy workloads.
    
   ## Working of Amazon RDS
   ![how_read_replicas_work-f](https://user-images.githubusercontent.com/43639867/190599698-e3beec85-fcb4-4e12-afd8-b26dbf918bbd.png)



    







