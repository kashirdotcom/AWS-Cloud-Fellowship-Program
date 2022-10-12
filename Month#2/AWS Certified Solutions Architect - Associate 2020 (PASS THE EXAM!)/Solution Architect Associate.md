# Solution Architect Associate
## What we consider
- Architecture Daigram
- Pricing (Cost Optimization)
- Constant Learning (Docs/ other Stuffs)
- Security/ Networking
## S3 Object
- It contains key, value, version ID and metadata.
- Its has the transfer rate of 5 TB.
## S3 Buckets
- S3 bucket hold objects.
- Its a universal namespace so their name must be unique.
## Storage Classes
- Fast Availabilty (99.99%), durability and replicated across various zones.
- Intelligent Tiering. (storing for 30 days)
- Standard Infrequently Accessed. (storing for 30 days)
- One Zone IA (storing for 30 days)
- S3 Glacier - long term cheap storage. (storing for 90 days to 180 Days)
## S3 Security
Access control list can be configured by using bucket policies.
## Encryption
- Server side encryption - encrypt object data.
- SSE-AES, SSE-KMS, SSE-C.
- S3 managed keys.
- Client side encryption - we encrypt our files before uploading to S3.
## Data Consistency
- Read After Write Consistency.
- Eventual consistency.
## Cross Region Replication CRR
- When enabled --- replicates an object to another region
- Durablitiy -- Disaster recovery.
## MFA Delete
- Ensures that users cannot delete MFA unless they provide their MFA code.
- Bucket S3 versioning must be turned on.
- AWS cli must be used to turn on MFA.
## Snowball
- Generally it costs thousands of dollars to transfer 100TB over high speed internet.
- Snowball reduces this cost by 1/5th.
- Reduce transfer time by less than a week.

## Virtual Private Cloud (VPC)
- Region Specific.
- Can create 5 VPC per region.
- 200 VPC subnets per VPC.
- IP4 Cidr Block.
- DNS hostnames.

## VPC Features
- AWS has default VPC with default settings.
- Default DHCP
- Default Security group.
- Default network access control list.
- VPC size /16 IPv4 CIDR Block.
- Contains route table.
- Default subnet /20 in each zone.

## VPC Peering
- Allows us to connect to another VPC over a irect network route using a private network address.
## Route Tables
- It determines where our traffic is directed.
- Each subnet should be associated with it.
## IGW Internet Gateway
- Allows VPC to connect to the internet.
- NAT translation.
- Target VPC route tables to connect to internet routeable traffic.
## Bastions
- They are EC2 instances in a private subnet and security hardened. They give access to EC2 instances via SSH/RCP.

## Direct Connect
- Its a very fast network. its an AWS solution for building dedicated netowrk from on-premises locations.
## VPC Endpoints
- It allows us to connect to different AWS services privately.
- Highly scaled.
- Redundant.
- High availability.
- Interface Endpoints
     - Elastic network interfaces with private IP addresses.
- Gateway Endpoints
     - It targets a specific route in the route table.
## Flow Logs
- It captures traffic information in and out of network interfaces with in VPC.
- It can be created for
     - Subnets
     - VPC.
     -  Network interface.
  ## NACL
Network Access control list contains set of rules which allows or deny network traffic into or out of a subnet.

## Security Groups
Security Groups contains set of rules that controls inbound and outbound traffic of EC2 Instances. It has no deny rules. Acts as a virtual firewall at instance level.

## NAT
Network address translation remaps the Private IP addresses in a private network to gain the outbound access to the internet.

## Identity Access Management (IAM)
I am allows management of access of users and resources which includes;

- User
- Roles
- Groups
- Policies
- MFA
- Permissions
## Amazon Cognito
- Decentralized Managed Authentication. Signup Sign in integration with our apps. Providers - Google -Facebook.

     - Cognito User Profiles
     - Cognito Identity Pools
     - Cognito Sync.
- Web Identity Federation

      - Identity Security information exchange between identity providers. Identity providers (IDP) could be; Google, facebook, github, linkedIn etc.

Types of Providers

- SAML Security assertion markup language. (Single Sign on)

- User Pools

User directories to manage the actions for web and mobile apps. like

- Signin
- Sign up
- Confirmation
- Recovery
## AWS CLI
- AWS CLI let us iteract with AWS services from anywhere through command line interface.

For Example we can;

- Launch, start, stop, terminate EC2 Instance
- Create, list buckets, upload data.
- Update security groups, create/update subnets.
- Setting up VPS, create and terminate.
## AWS SDK
AWS Software Development kit is used for controlling AWS services through different programming languages. It is a set of API libraries that let us integrate AWS Services to our application. Installed via python script. Programatic access must be enabled per user via IAM to access CLI or SDK.

## AWS Cloud9
AWS Cloud9 allows us to write and debug a code with just a browser.

## Domain Name System DNS
It is a service which handles converting a domain name into a routable IP address.

- IPV4 (192.168.150.15)
- IPV6 (2001:db8:3333:4444:5555:6666:7777:8888)
Top Level domains. example.com Second level domains. example.com.uk

Record DNS: It converts domain names with IP addresses. CNAME Records: It converts a domain name into another domain name.

TTL: The time in which DNS record will be cached.

## Route53
It is a cloud based highly scaleable and available DNS. It allows us to register, manage domains and create routing rules.

- Route Traffic to our web app.
- Route traffic to an instance.
- Route traffic to an API Gateway.
- Route traffic to a cloudfront.
- Route traffic to an elastic IP.
Alias Record

Record Set

## Routing Policies
- Simple Routing

- Weighted Routing --- Split up traffic based on different weight defined

- Latency Based Routing ---directs based on lowest network latency possible for our end user (bassed on region).

- Failover Routing --- allows us to create a primary site in one location and a secondary recovery site on another location.

- Geolocation Routing --- Directs traffic based on geo-graphical location where the request generated.

- Geo Proximity Routing --- select customs region and set custom co ordinates.

- Multi Value Answer Routing

- Traffic Flow ---- Visual Editor to create routing configurations for resources using existing routing types.

- Health Checks --- A health check can initial a failover if the status is unhealthy. Monitor endpoints.

## Amazon EC2
Amazon EC2 or Elastic compute cloud allows user to rent virtual computer on which they can run their own applications. EC2 provides scalable deployment of an application through a service (Auto scaling); in which a user can boot a Amazon machine image to configure a virtual machine. A user can create as many virtual machines as he needs and paying by a second of active servers.
### Features of EC2
- Virtual computing environment.
- Configuration of CPU, memory, storage, and networking capacity for our instances, known as instance types, with diverse configuration options.
- Elastic IP addresses.
- Multiple physical locations for our resources, with different availability timezones and regions.
- Security; such as firewalls and managing IP addresses ranges, ports and protocols through security groups. Secure login information, with private and public key.
- Creating our own private network, through virtual private cloud service.
- Persistant storage options i.e Elastic block storage.
# Instances Types
Amazon provides variety of Instances types which are optimized for difference use cases. Instances types contains diverse combinations and types of CPU, memory , network capacity with flexibility that gives us mixture of different resources to run our application.

- General Purpose
- Compute Optimized
- Memory Optimized
- Storage Optimized
- Accelerated Computing
## Placement Groups
Placement Groups let us choose the logical placement of our instances to optimize for communication, performance and durability. Properties based on:

- Cluster
- Partition
- Spread
## EC2 Pricing Model
- On Demand
- Reserve
- Spot
- Dedicated
## Dedicated Host Instances
- Multi Tenant --- virtual isolation
- Single Tenant --- Physical isolation
# AWS AMI
Amazon Machine Image provides an information required to launch an instance. It contains;
- Volumes, EBS snapshot.
- Operating System, servers information.
- Some are region specific, variation across regions.
- Architecture (32,64).
## Amazon EC2 Autoscaling Groups
Amazon EC2 Auto Scaling helps us ensure that we have the correct number of Amazon EC2 instances available to handle the load for our application. You create collections of EC2 instances, called Auto Scaling groups. We can specify the minimum number of instances in each Auto Scaling group, and Amazon EC2 Auto Scaling ensures that our group never goes below this size. We can specify the maximum number of instances in each Auto Scaling group, and Amazon EC2 Auto Scaling ensures that our group never goes above this size.

It occurs via;

- Capacity.

- Health check replacements.

- Scaling policies.

## Elastic Load Balancer
Distribute network traffic to improve application scalability.

### ELB Types

- Application Load balancer
- Gateway Load balancer
- Network Load balancer

## Sticky Session
- Its an advanced load balancing method which allow us to bind a user session to a specific EC2 instance.

## Elastic File System
- Scalable, elastic, cloud native, NFS file system.

- Attach a single file system to multiple EC2 instances.
- Supports NFSv4 Version protocol
- easily shrink and pay per GB per month
## Elastic Block Store EBS
- Virtual Harddrive
- Backup via Snapshots
- Easy Encryption

- IOPS
    - Input/Output Per Secound
    - non-contigueous reads and writes

- Throughput
    - data transfer rate from the storage
   ## Types of EBS
   - General Purpose gp2-use for workloads-upto 16TB-16000 IPOS 
   - Provisioned IOPS io1 - use for large database-upt 16 TB - 64000  
   - Throughput Otimized HDD
   - Cold HDD
   - EBS Mangentic 
   
   ## EBS Moiving Values
    - take the snapshot of the volume
    - create an AMI from the snapshot
    - launch two EC2 Instance in desired AZ.
    
    ## EBS VS INstance Store Volumes
    1. EBS are durable, while Instance store is temporary
    2. EBS are created from EBS Snapshot while Instance Store is created from template stored in S3.
    
    
    ## Introduction to Cloud Front
    ### Contenet Delivery Network
    - distributed Network of servers which deliver web pages
    - used to deliver an entire website
    - request for content from nearest location for the best possible performance.
   ### Core Components of Cloud Front
   - Origin (where all the orignal files are located)
   - Edge Location (web content will be cached
   - Distribution (where cached content should behave)- replicates copies based on PriceClass

### Types of Distributions
- WEB (for website)
- RTMP (for streaming media)

## CloudFront - Lambda@Edge
- overrides the behaviour of request and responses
- Four Functions
   - Viewver Request - Cloudfront recieves a request from a viewer
   - Origin Request - cloudfront forwards a request to the origin
   - Origin Response - cloudfront recieves a response from the origin
   - Viewer Response -   cloudfront returns the response to the viewver.
## CloudFront - Protection
by default distribution allows everyone to have access.
### Orignal Identity 
Virtual User Identity that will be used to give your cloudfront distribution permsiion to fetch a private object.
In order to use Signal URLs  or signed cookies (passed along with the request to CloudFront.

## Data Warehouse
Data Warehouse is the online analytical Processing, store large amount quantities.
Example is AWS Redshift, petabyte scale solution
## Redshift
Redshift is the coloumnar storage database(optimizing analytical query performance, reduces the overall disk I/O requirements and reduce the amount of data.
### Redshift Single Node
size of 160 GB
### Redshift Multinode
- Leader Node (manages client connection)
- compute Node (stores data and performs)

## Types of Nodes
- Dense Compute (less storage with high performance)
- Dense Storage (clusters of data)

## Masively Parallel Processing
Automatic Distributes Data and query across all nodes.
Maintaing Fast Query Performance

## Redshift Backups
enabled by default with a 1 day retention period
upto 35 days modification

maintain 3 copies of the data
- orignal copy
- replica on the compute nodes
- backup copy in S3

## Compute Node Hours
1 unit per node, per hour
not charged for leader node hours,
billed for only tranfers within a VPN, not outside it

## Redshift Security
Encrypted using SSL (AES-256)
Redshift is the Single AZ

## DynamoDB
- Key Value and Document Database(NOSQL)
- consistant read and writes
- 








    
   
   
    
