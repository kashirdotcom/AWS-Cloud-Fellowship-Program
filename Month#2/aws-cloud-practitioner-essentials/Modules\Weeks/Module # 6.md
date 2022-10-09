# Security

## Shared Responsibility Model
- AWS is responsible for some parts of your environment and you (the customer) are responsible for other parts. This concept is known as the shared responsibility model.
- Customer responsibilities ( security in the cloud)
   - maintain complete control over your content. 
   - You are responsible for managing security requirements for your content, including which content you choose to store on AWS
   - Services which you are using
- AWS responsibilities(security of the cloud)
  - protecting the global infrastructure that runs all of the services offered in the AWS Cloud
  - Specifically the physical infrastructure that hosts your resources
 ![image](https://user-images.githubusercontent.com/43639867/194740784-f0fec746-f123-407c-be9f-ebbcb19cdd7e.png)
 
 ## User Permission and Access
 ### 1. AWS Identity and Access Management (IAM)
 - manage access to AWS services and resources securely. 
     - IAM users, groups, and roles
     - IAM policies
     - Multi-factor authentication
 ### 2. AWS Account Root User
 It has complete access to all the AWS services and resources in the account.
 **Do not use the root user for everyday tasks. **
 
 
 ### 3. IAM users
 - IAM Users represents the person or application that interacts with AWS services and resources. It consists of a name and credentials.

### 4. IAM policies
document that allows or denies permissions to AWS services and resources.
![image](https://user-images.githubusercontent.com/43639867/194741085-7cd181e4-72e7-460b-8c27-d7cb2263aaf9.png)

### 5. IAM Groups
collection of IAM users
assign an IAM policy to a group, all users in the group are granted permissions specified by the policy.


### 6. IAM Roles
An IAM role is an identity that you can assume to gain temporary access to permissions.  
IAM roles are ideal for situations in which access to services or resources needs to be granted temporarily, instead of long-term.  

### 7. Multi-factor Authentication
You can enable MFA for the root user and IAM users. As a best practice, enable MFA for the root user and all IAM users in your account. By doing this, you can keep your AWS account safe from unauthorized access.


## AWS Organizations
When you create an organization, AWS Organizations automatically creates a root, which is the parent container for all the accounts in your organization. 

In AWS Organizations, you can centrally control permissions for the accounts in your organization by using **service control policies (SCPs)**. SCPs enable you to place restrictions on the AWS services, resources, and individual API actions that users and roles in each account can access.

### Organizational Units
Converting whole organizations into the Sub Parts or units for managing them indivisual.


## Compliance
### 1. AWS Artifact
- An audit or inspection will ensure that the company has met those standards.
- provides on-demand access to AWS security and compliance reports and select online agreements. AWS Artifact consists of two main sections: 
   - AWS Artifact Agreements
   review, accept, and manage agreements for an individual account and for all your accounts in AWS Organizations

   - AWS Artifact Reports
           - AWS Artifact Reports provide compliance reports from third-party auditors.
           -  These auditors have tested and verified that AWS is compliant with a variety of global, regional, and industry-specific security standards and regulations. 
           -  AWS Artifact Reports remains up to date with the latest reports released. 
## Denial-of-Service Attacks
- A denial-of-service (DoS) attack is a deliberate attempt to make a website or application unavailable to users.

### AWS Shield
AWS Shield is a service that protects applications against DDoS attacks. AWS Shield provides two levels of protection: Standard and Advanced.

1. **AWS Shield Standard**
- AWS Shield Standard automatically protects all AWS customers at no cost. It protects your AWS resources from the most common, frequently occurring types of DDoS attack. 
- AWS Shield Standard uses a variety of analysis techniques to detect malicious traffic in real time and automatically mitigates it. 
2. **AWS Shield Advanced**
- AWS Shield Advanced is a paid service that provides detailed attack diagnostics and the ability to detect and mitigate sophisticated DDoS attacks. 
- It also integrates with other services such as Amazon CloudFront, Amazon Route 53, and Elastic Load Balancing. Additionally, you can integrate AWS Shield with AWS WAF by writing custom rules to mitigate complex DDoS attacks.

## Additional Security Services
- **AWS Key Management Service (AWS KMS)**
AWS Key Management Service (AWS KMS) enables you to perform encryption operations through the use of cryptographic keys. 
- **AWS WAF**
   - AWS WAF is a web application firewall that lets you monitor network requests that come into your web applications. 
   - AWS WAF works together with Amazon CloudFront and an Application Load Balancer.
   
- **Amazon Inspector**
Amazon Inspector helps to improve the security and compliance of applications by running automated security assessments. It checks applications for security vulnerabilities and deviations from security best practices, such as open access to Amazon EC2 instances and installations of vulnerable software versions. 
- **Amazon GuardDuty**
Amazon GuardDuty is a service that provides intelligent threat detection for your AWS infrastructure and resources. It identifies threats by continuously monitoring the network activity and account behavior within your AWS environment.
If GuardDuty detects any threats, you can review detailed findings about them from the AWS Management Console. 


 
 
