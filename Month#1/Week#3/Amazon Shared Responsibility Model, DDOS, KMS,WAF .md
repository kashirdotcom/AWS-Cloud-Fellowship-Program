# 1. Amazon Shared Responsibility Model
https://aws.amazon.com/compliance/shared-responsibility-model/
- Its the model used for both cutomer and Amazon are resposnible on the factor of Security.
- Security and Compliance is a shared responsibility between AWS and the customer. 
-  This shared model can help relieve customer’s operational burdens as AWS operates, manages and controls the components from the host operating system and virtualization layer down to the physical security of the facilities in which the service operates.
-  The customer assumes responsibility and management of the guest operating system including updates and security patches, other associated application software as well as the configuration of the AWS provided security group firewall.
## AWS responsibility “Security of the Cloud”
- AWS is responsible for protecting the infrastructure that runs all of the services offered in the AWS Cloud.
- This infrastructure is composed of the hardware, software, networking, and facilities that run AWS Cloud services.
## Customer responsibility “Security in the Cloud”
- Protecting the EC2 Passwords, SSH Keys, Manages the IAM Roles and his data.
- Protect also the Passwords used, Operating System,IPS (public, private or the elastic).
## Amazon Shared Controls
### Inherited Controls
Controls that a customer fully inherits from AWS. > Physical and Environmental controls.

### Shared Controls
Controls that apply to both the infrastructure layer and customer layers, but in completely separate contexts or perspectives. In the AWS shared security model, a shared control, AWS provides the requirements for the infrastructure and the customer must provide their own control implementation within their use of AWS services. . In shared responsibility model, AWS is responsible for the:

### Patch Management
AWS is responsible for patching and fixing flaws within the infrastructure, but customers are responsible for patching their guest OS and applications.
Configuration Management: AWS maintains the configuration of its infrastructure devices, but a customer is responsible for configuring their own guest operating systems, databases, and applications.
### Awareness & Training
AWS trains AWS employees, but a customer must train their own employees.
### Customer Specific
Controls are solely the responsibility of the customer based on the application they are deploying within AWS services. Examples of customer-specific controls include:
Service and Communications Protection or Zone Security may require a customer to route or zone data within specific security environments.
# 2. Denial Of Service Attacks and Protection in Amazon
https://aws.amazon.com/shield/ddos-attack-protection/
- A Denial of Service (DoS) attack is a malicious attempt to affect the availability of a targeted system, such as a website or application, to legitimate end users.
- Creates ulimited Request to the server for the downtime
- Handles the Attack **Each Level of OSI**
   - For Example
     - Uses the SSL on OSI Layer 6
     - Uses the HTTPS on OSI Layer 7
 ## Types of Layer Attacks
 ### 1. Infrastructure Layer Attacks
 - Attacks at **Layer 3 and 4**, are typically categorized as Infrastructure layer attacks.
 - These are also the **most common type of DDoS attack** and include vectors like **synchronized (SYN) floods** and other reflection attacks like **User Datagram Packet (UDP) floods**. 
 - These attacks are usually **large in volume** and **aim to overload the capacity of the network or the application servers**.
 -  But fortunately, these are also the type of attacks that have **clear signatures and are easier to detect**.
 ### 2. Application Layer Attacks
- These are **Layer 6 and 7 attacks**.
-  **Less common**, **more sophisticated**, **small in volume and aimed to target particular expensive parts of the application**.
-   Example of these attacks are flood of **HTTP requests to a login page**, **an expensive search API**.
## Protection Techniques:
### 1. Reduce Attack Surface Area
- **Most common ways of protection against DDOS attacks** is by minimizing the attack surface area so a **limited or no area is left unprotected**.
- This can be done by **moving computational resources behind Content Distribution Networks (CDNs)** or **Load Balancers** and **restricting direct traffic**, **firewalls or Access Control Lists (ACLs)** can also be used to control the traffic.
### 2. Plan for Scale:
#### Bandwidth (or transit) capacity
Plan for ample redundant internet connectivity while architecting the application, allowing to handle large amount of internet traffic. Employing Content Distribution Networks (CDNs) and smart DNS resolution services, provide web applications with an additional layer of network infrastructure for serving content and resolving DNS queries.

#### Server Capacity
Most DDoS attacks are volumetric attacks so add a provision for scaling up and down resources according to traffic. Load Balancers can also be used for monitoring and shifting loads between resources to prevent overloading any one resource




# 3. Amazon KMS
- AWS Key Management Services (KMS) is used to encrypt data across AWS workloads, digitally sign data, encrypt within applications using AWS Encryption SDK, and generate and verify message authentication codes (MACs).
- AWS Key Management Service (AWS KMS) lets you create, manage, and control cryptographic keys across your applications and more than 100 AWS services.
## KMS Features:
- Managed service that enables you to easily create and control the keys used for cryptographic operations.
- Keys are kept as multiple copies in a single region to make sure its durability and reliability.
- A shared key management infrastructure with FIPS 140–2 Level 2 compliance
- Currently supports 50+ AWS services.
- Highly Available (HA) is present.
-  It integrates fully with IAM and CloudTrail for Permission Management and Auditing respectively.
-  Supports both symmetric and asymmetric key encryption. Until 2019, it only supported symmetric but now it supports both key encryption aspects [3]. With the support of asymmetric key encryption, it widened the aspect of interoperability by being able to connect to many other Key Management Infrastructures in the market
### How KMS Works

![image](https://user-images.githubusercontent.com/43639867/190986698-cfa4f87f-ac66-4884-9e4f-5a23fe895466.png)

## KMS supported keys:
1. Customer Master Keys (CMK)
2. Data Encryption Keys.
> **_NOTE:_** By default, CMK can encrypt data up to 4KB. If data to be encrypted is more than 4KB, you have to use (CMK + Data Encryption Key) combination, which is known as the KMS Two Tier Architecture.

### CMK Keys:
There are three types of CMK.

#### Customer Managed CMK 
Keys used by AWS on a shared basis across many AWS accounts. You normally do not interact with this CMK.
#### AWS Managed CMK 
Used as the default CMK within most of the AWS services and named under the AWS service name (aws/). You are not able to manage or change its configurations (Key Policies, Rotation)
### AWS owned CMK 
You are able to create your own CMK. You are allowed to rotate keys, key policies can be defined and can be enabled / disabled. Customer Managed CMKs are regional specific and if you want to use in another region you need to use a different CMK in the target region.

# AWS Web Application Firewall (WAF)
- AWS Web Application Firewall also popularly know as AWS WAF is a web application firewall that helps protect your web applications or APIs against common web exploits and bots.
- You have the authority to create security rules to control the traffic flow reacing your web application.
- You can deploy AWS WAF on Amazon CloudFront as part of your CDN solution, the Application Load Balancer that fronts your web servers or origin servers running on EC2, Amazon API Gateway for your REST APIs, or AWS AppSync for your GraphQL APIs.
## Benefits
- Ease of deployment & maintenance
- Easily monitor, block, or rate-limit bots
- Save time with managed rules
- Improved web traffic visibility
- Agile protection against web attacks
- Security integrated with how you develop applications

## Working of Amazon WAF
![image](https://user-images.githubusercontent.com/43639867/190987865-38876af4-c253-407b-8d58-9d3dee8941a9.png)

# AWS Guard Duty
- Threat detection service that continuously monitors your AWS accounts and workloads for malicious activity and delivers detailed security findings for visibility and remediation.
- It Continuously monitor your AWS accounts, instances, container workloads, users, and storage for potential threats.
-  It expose threats quickly using anomaly detection, machine learning, behavioral modeling, and threat intelligence feeds from AWS and leading third-parties, and mitigate threats early by initiating automated responses.

## Working of AWS Guard Duty
![image](https://user-images.githubusercontent.com/43639867/190988422-2080bc74-ab49-4b26-ac3a-8c55820744de.png)

