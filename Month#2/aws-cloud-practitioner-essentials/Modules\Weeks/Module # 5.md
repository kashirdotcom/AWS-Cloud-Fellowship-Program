# Storage and Databases

## Instance Stores and Amazon Elastic Block Store (Amazon EBS)

### 1. **Instance Store**
- Temporary block-level storage for EC2
- physically attached to the host computer
- EC2 Terminated, Data Terminated
- No Extra Fees

### 2. **Amazon Elastic Block Storage (Amazon EBS)**
- Seperate Block for storing Data, Linking to AWS EC2.
- EC2 Terminated, Data Stored
- Pay Extra for this

### 3. **Amazon EBS Snapshots**
- Backup the Data, and Make Backup for more than 1 copies and hence recent backup will be stored in it.
- Supports **Full Backup(Recent Backup)** and **Incremental Backup(supports copies/Versions)**.
- ![image](https://user-images.githubusercontent.com/43639867/194739144-fd2d427c-48b4-4cda-97c9-172af5a8f5c0.png)

### 4. **Amazon Simple Storage Service (Amazon S3)**
- Provides Object Storage (consists of data, metadata, and a key)
- Data Stored in  buckets.
- set permissions to control visibility and access to it
- ** Storage Classes**
    - Amazon S3 Standard => (frequently accessed data, Stored Data in Minimum 3 AZ)
    - Amazon S3 Standard-Infrequent Access (S3 Standard-IA)=> (infrequently accessed data,lower storage price and higher retrieval price)
    - Amazon S3 One Zone-Infrequent Access (S3 One Zone-IA)=> (Stores Data in single Availability Zone)
    - Amazon S3 Intelligent-Tiering => (data with unknown or changing access patterns,small monthly monitoring and automation fee per object)
    - Amazon S3 Glacier Instant Retrieval=> archived data that requires immediate access
    - Amazon S3 Glacier Flexible Retrieval=> Low-cost storage designed for data archiving, retrieve objects within a few minutes
    - Amazon S3 Glacier Deep Archive => Lowest-cost object storage class ideal for archiving, Retrieve Objects in 12 Hour
    - Amazon S3 Outposts =>  delivers object storage to your on-premises AWS Outposts environment
  
  

### 5. **Comparing Amazon EBS and Amazon S3**
- EBS Supports 15 TB,SSD By Default, HDD also Availble)
- S3 (Unlimited Storage, Indivisual Object upto 5 TBs, write once read many, 99.99% durablity, Web Enabled, Regional Ditributed, Serverless)
- Object Storage take anything as complete, but Block storage devides the componenets in objects.
### 6. **Amazon Elastic File System (Amazon EFS)**
- File Shared Server
- Access through Paths
- Many Resources are used at the same time, is applicable in EFS.
- scalable file system used with AWS Cloud services and on-premises resources (shrinks automatically)
- scale on demand without disturbing Applications

### 7. **Comparing Amazon EBS and Amazon EFS**
- EBS Stored in single Availability Zone.Connecting EC2 and EBS both are in same Availability Zone.
- EFS regional service. It stores data in and across multiple Availability Zones. Connecting Through Instance is AWS Direct Connect for AWS EC2 and EBS.

### 8. **Amazon Relational Database Service (Amazon RDS)**
- use structured query language (SQL) to store and query data
- easily understandable, consistent, and scalable way
- automates tasks such as hardware provisioning, database setup, patching, and backups

### 9. **Amazon RDS database Engines**
- Amazon Aurora => 
     - (Enterprise-class relational database,compatible with MySQL and PostgreSQL relational databases, 5x Faster MYSQL, 3x PostgreSQL)
     - reduce your database costs by reducing unnecessary input/output (I/O) operations while resoucres remain availble and reliable).
     - workloads require high availability, its replicates copies of the data across 3 AZ and Continueos Backup data to S3).

- PostgreSQL 

- MySQL 

- MariaDB 

- Oracle Database

- Microsoft SQL Server

### 10. **Amazon DynamoDB**
- Nonrelational Databases
- key-value database service. It delivers single-digit millisecond performance at any scale.
- serverless, which means that you do not have to provision, patch, or manage servers. 
- require high performance while scaling.

### 11. **Amazon Redshift**
- data warehousing service that you can use for big data analytics
- ability to collect data from many sources 
-  helps you to understand relationships and trends across your data.

### 12. **AWS Database Migration Service (AWS DMS)**
- migrate relational databases, nonrelational databases, and other types of data stores.
- Development and test database migrations
- Database consolidation
- Continuous replication


### 13. **Amazon DocumentDB**
  - supports MongoDB workloads. (MongoDB is a document database program.)
### 14. **Amazon Neptune**
   - build and run applications that work with highly connected datasets, such as recommendation engines, fraud detection, and knowledge graphs.
### 15. **Amazon Quantum Ledger Database (Amazon QLDB)** 
   - ledger database service
   - review a complete history of all the changes that have been made to your application data.
   
### 16. **Amazon Managed Blockchain**
 - service that you can use to create and manage blockchain networks with open-source frameworks. 
 - Blockchain is a distributed ledger system that lets multiple parties run transactions and share data without a central authority.
### 17. **Amazon ElastiCache**
 - service that adds caching layers on top of your databases to help improve the read times of common requests. 

- It supports two types of data stores: Redis and Memcached.
### 18. **Amazon DynamoDB Accelerator**
- in-memory cache for DynamoDB. 

- It helps improve response times from single-digit milliseconds to microseconds.


