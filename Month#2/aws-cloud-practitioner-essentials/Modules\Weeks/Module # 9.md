# Migration and Innovation
## AWS Cloud Adoption Framework (AWS CAF)
- Business Perspective => IT aligns with business needs and that IT investments link to key business results.
- People Perspective => upports development of an organization-wide change management strategy for successful cloud adoption.
- Governance Perspective =>  focuses on the skills and processes to align IT strategy with business strategy. This ensures that you maximize the business value and minimize risks.
- Platform Perspective =>  includes principles and patterns for implementing new solutions on the cloud, and migrating on-premises workloads to the cloud.
- Security Perspective => ensures that the organization meets security objectives for visibility, auditability, control, and agility. 
- Operations Perspective => helps you to enable, run, use, operate, and recover IT workloads to the level agreed upon with your business stakeholders.

## Migration Strategies
- **Rehosting**
involves moving applications without changes. 
- **Replatforming**
 involves making a few cloud optimizations to realize a tangible benefit. Optimization is achieved without changing the core architecture of the application.
- **Refactoring/re-architecting**
involves reimagining how an application is architected and developed by using cloud-native features. Refactoring is driven by a strong business need to add features, scale, or performance that would otherwise be difficult to achieve in the application’s existing environment.
- **Repurchasing**
involves moving from a traditional license to a software-as-a-service model. 
- **Retaining**
consists of keeping applications that are critical for the business in the source environment. This might include applications that require major refactoring before they can be migrated, or, work that can be postponed until a later time.
- **Retiring**
process of removing applications that are no longer needed.

## AWS Snow Family
The AWS Snow Family is a collection of physical devices that help to physically transport up to exabytes of data into and out of AWS. 
AWS Snowcone is a small, rugged, and secure edge computing and data transfer device. 

### Snowball Edge Storage Optimized
devices are well suited for large-scale data migrations and recurring transfer workflows, in addition to local computing with higher capacity needs. Snowball Edge Storage Optimized provides 80 TB of HDD capacity for block volumes and Amazon S3-compatible object storage, and 1 TB of SATA SSD for block volumes.

### Snowball Edge Compute Optimized
provides powerful computing resources for use cases such as machine learning, full motion video analysis, analytics, and local computing stacks. 

## AWS Snowmobile
AWS Snowmobile is an exabyte-scale data transfer service used to move large amounts of data to AWS. 

You can transfer up to 100 petabytes of data per Snowmobile, a 45-foot long ruggedized shipping container, pulled by a semi trailer truck.

