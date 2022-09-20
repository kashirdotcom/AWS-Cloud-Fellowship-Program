# AWS Migration Stratagies
https://aws.amazon.com/blogs/enterprise-strategy/6-strategies-for-migrating-applications-to-the-cloud/
## 6 Different Strategies The 6's R
1. Rehosting - **lift-and-shift.**
2. Replatforming  - **lift-tinker-and-shift**
3. Repurchasing  -  **Moving to a different product.**
4. Refactoring / Re-architecting - **Re-imagining how the application is architected and developed, typically using cloud-native features.**
5. Retire - **Get rid of**
6. Retain - **revisit or do nothing (for now**

### Rehosting
- Its means that the migration is done through tools like  [CloudEndure Migration, AWS VM Import/Export] while migration also done via Manual.

- Applications are easier to optimize/re-architect once they’re already running in the cloud. Partly because your organization will have developed better skills to do so, and partly because the hard part — migrating the application, data, and traffic — has already been done.

## Replatforming 
Migrating your application to a fully managed platform like Amazon Elastic Beanstalk.

##  Repurchasing
move to a SaaS platform like already Build Platforms and you can use it
For Example
- CRM to Salesforce.com
- HR system to Workday
# Refactoring / Re-architecting
- This is typically driven by a strong business need to add features, scale, or performance that would otherwise be difficult to achieve in the application’s existing environment.
- Migration of the application from monolithic architecture to Serverless Enviorment.
- Most expensive pattern, but, if you have a good product-market fit, it can also be the most beneficial.

## Retire
Closing the Infrastructure the System

## Retain
Didnot migrated the Updgraded System,or not inclined to migrate some applications


#  AWS Snow Family
https://aws.amazon.com/snow/

## Defination
Its the collection of physical devices that help migrate large amounts of data into and out of the cloud without depending on networks. This helps you apply the wide variety of AWS services for analytics, file systems, and archives to your data.

## Features of AWS Snow Family
- **Simple management and monitoring** - 
AWS OpsHub is a complimentary graphical user interface (GUI) available to makes it easy to setup and manage Snow devices
- **NFS endpoint** - 
Easily use Snow devices with your existing on-premises servers and file-based applications.
- **On-board computing** - 
Snow Family devices have computing resources to collect and process data at the edge support for the AWS IOT
- **Encryption** 
1. Encrypted with 256-bit encryption keys 
2. Managed by the AWS Key Management Service (KMS).
3. Keys are Never stored on the device.
- **Anti-tamper & Tamper-evident**  
1. Trusted Platform Module (TPM) that provides a hardware root of trust.
2.  Each device is inspected after each use to ensure the integrity of the device and helps preserve the confidentiality of your data.
- **End-to-end tracking**   
Each device uses an E-Ink shipping label for easy tracking and automatic label updates for return shipping using 
1. Amazon Simple Notification Service (SNS)
2. Text messages
3. AWS Console.
- **Secure erasure** -
Once the data migration job is complete and verified, AWS performs a software erasure of the device that follows the National Institute of Standards and Technology (NIST) guidelines for media sanitization.

## AWS Snow Family service models
Three type of Service Models
- AWS Snowcone
1. most compact and portable device
2. Its ruggedized, secure, and purpose-built for use outside of a traditional data center.
- AWS Snowball
1. Availble as a Compute Optimized device or a Storage Optimized device.
2. All devices are suited for extreme conditions, tamper proof, and highly secure.
- AWS Snowmobile
1. Its an Exabyte-scale data migration device used to move extremely large amounts of data to AWS.
2. Migrate up to 100PB in a 45-foot long ruggedized shipping container, pulled by a semi-trailer truck.


## Features Comparision
![image](https://user-images.githubusercontent.com/43639867/191267553-93f8a21d-fe46-4701-a68e-69fd114d560a.png)


