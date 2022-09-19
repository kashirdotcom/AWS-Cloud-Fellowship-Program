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




# 3. Amazon KMS, WAF, Guard Duty
