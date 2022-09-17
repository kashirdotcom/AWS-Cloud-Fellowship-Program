## Resources
1. Amazon DynamoDB https://www.dynamodbguide.com/what-is-dynamo-db/
2. Amazon DynamoDB vs RDS https://dynobase.dev/dynamodb-vs-amazon-rds/
3. Amazon RedShift https://www.tutorialspoint.com/amazon_web_services/amazon_web_services_redshift.htm
4. Amazon DMS https://www.amazonaws.cn/en/dms/

# Amazon DynamoDB
1. Uses NoSql Database
2. It is swift, reliable, and scalable, which makes working with NoSQL data much easier to handle.
3. How its Work!
![image](https://user-images.githubusercontent.com/43639867/190842397-73b63aa0-871f-411e-9511-0d2a540a8595.png)

## Key Features of Amazon DynamoDB
- It Helps you to Offload the Burden of Administrative Side, means manage it byself.
- Scale as its own
- Provides Data Encrytion
- Provides on Demand Backup Capacity, along with the backup of the large tables.
- DynamoDB allows you to delete expired items from tables automatically to help you reduce storage usage and the cost of storing data that is no longer relevant
- DynamoDB automatically spreads the data and traffic for your tables over a sufficient number of servers to handle your throughput and storage requirements, while maintaining consistent and fast performance.
- Automatically moves your data over Regions and Availbility Zones for the durability and the high Availbility. 

## Core Component of Amazon DynamoDB
1. Tables
2. Items 
3. Attributes
   - **Primary Key**
   Used for Uniquely Identifies for the Items in the Table.
      - **Partition key** -
       Its the simple primary key, composed of one attribute known as the partition key.
       DynamoDB uses the partition key's value as input to an internal hash function. The output from the hash function determines the partition (physical storage internal to DynamoDB) in which the item will be stored. 
      - **Sort key** -
        All items with the same partition key value are stored together, in sorted order by sort key value.
        
   - **Secondary indexes**
   secondary index lets you query the data in the table using an alternate key, in addition to queries against the primary key.
      - **Global secondary index** - An index with a partition key and sort key that can be different from those on the table.
      - **Local secondary index** – An index that has the same partition key as the table, but a different sort key.
      
      
      > __Note__
      Each table in DynamoDB has a quota of 20 global secondary indexes (default quota) and 5 local secondary indexes.
    - DynamoDB Streams
      - The data about these events appear in the stream in near-real time, and in the order that the events occurred.
      - Each event is represented by a stream record. If you enable a stream on a table, DynamoDB Streams writes a stream record whenever one of the following events occurs:
      - A new item is added to the table: The stream captures an image of the entire item, including all of its attributes.
      - An item is updated: The stream captures the "before" and "after" image of any attributes that were modified in the item.
      - An item is deleted from the table: The stream captures an image of the entire item before it was deleted.
      - Each stream record also contains the name of the table, the event timestamp, and other metadata. Stream records have a lifetime of 24 hours; after that, they are automatically removed from the stream.
     
     
         - **How its Work** -
         You can use DynamoDB Streams together with AWS Lambda to create a trigger—code that runs automatically whenever an event of interest appears in a stream. For example, consider a Customers table that contains customer information for a company. Suppose that you want to send a "welcome" email to each new customer. You could enable a stream on that table, and then associate the stream with a Lambda function. The Lambda function would run whenever a new stream record appears, but only process new items added to the Customers table. For any item that has an EmailAddress attribute, the Lambda function would invoke Amazon Simple Email Service (Amazon SES) to send an email to that address.

# Amazon DynamoDB vs RDS
| Amazon DynamoDB  |  RDS |
|---|---|
| DynamoDB is a database service for NoSQL data fully managed by Amazon Web Services  | mostly use it for structured and relational data (SQL).Its contains Aurora engine,MySQL, MariaDB, Oracle, PostgreSQL engines,SQL Server engine  |
| Fully Managed by the AWS  | Fully Managed by the AWS  |
|  Table consist of Any Size |  Aurora engine: 128 TB,MySQL, MariaDB, Oracle, PostgreSQL engines: 64 TB,SQL Server engine: 16 TB  |
| high-performance as it can cope with more than 10 trillion requests within a single day with peaks greater than 20 million requests per second.| A high-performance choice for OLTP applications and another cost-effective solution for general-purpose use.|
|less latency and response time when reading and writing data because of the high IO performance of SSDs| erformance that delivers at 3 IOPS per provisioned GB that can scale up to 3000 IOPS. The high-performance option can deliver up to 40000 IOPS per database instance.|
|Latency of DynamoDB is minimum, and it maintains within milliseconds. So, the performance of this database engine is considerably high, if you use the indexes and partitioning properly.| His high-performance IOPS rate is maintained throughout the lifetime of the database instance.|
|the data is replicated across three availability zones automatically. However, users do not have a choice to choose availability zones, they can only choose a region| Amazon RDS uses Multi-AZ deployments to enhance the availability of its databases. So, in case of any hardware failure, the requested data will be made available by replacing the compute instance powering the database instance with a functional one.|
| Uses AWS IAM, KMS(WS KMS (Key Management Service) encryption keys ensure DynamoDB security. The KMS allows creating, storing, and managing the encryption keys. There are three options for the users to encrypt the tables with DynamoDB.) for Securtity | Uses AWS KMS (The users can also use SSL to enhance the security of data.)| 


