# Networking
## Amazon Virtual Private Cloud (Amazon VPC)
Amazon VPC enables you to provision an isolated section of the AWS Cloud.
A networking service that you can use to establish boundaries around your AWS resources is Amazon Virtual Private Cloud (Amazon VPC).
Amazon VPC enables you to provision an isolated section of the AWS Cloud. In this isolated section, you can launch resources in a virtual network that you define. Within a virtual private cloud (VPC), you can organize your resources into subnets. A subnet is a section of a VPC that can contain resources such as Amazon EC2 instances.
## Internet gateway
An internet gateway is a connection between a VPC and the internet. You can think of an internet gateway as being similar to a doorway that customers use to enter the coffee shop. Without an internet gateway, no one can access the resources within your VPC.
### Virtual Private Gateway
- The virtual private gateway is the component that allows protected internet traffic to enter into the VPC.
- A virtual private gateway enables you to establish a virtual private network (VPN) connection between your VPC and a private network, such as an on-premises data center or internal corporate network.
-  A virtual private gateway allows traffic into the VPC only if it is coming from an approved network.
## AWS Direct Connect

- Establish a dedicated private connection between your data center and a VPC.  
- The private connection that AWS Direct Connect provides helps you to reduce network costs and increase the amount of bandwidth that can travel through your network.

# Subnets
A subnet is a section of a VPC in which you can group resources based on security or operational needs. Subnets can be public or private. 
## Public subnets 
It contain resources that need to be accessible by the public, such as an online store’s website.

## Private subnets 
It contain resources that should be accessible only through your private network, such as a database that contains customers’ personal information and order histories. 

# Network Traffic in a VPC
A packet is a unit of data sent over the internet or a network. 
It enters into a VPC through an internet gateway. Before a packet can enter into a subnet or exit from a subnet, it checks for permissions. These permissions indicate who sent the packet and how the packet is trying to communicate with the resources in a subnet.
## network access control list (ACL)
A network access control list (ACL) is a virtual firewall that controls inbound and outbound traffic at the subnet level.
Each AWS account includes a default network ACL. When configuring your VPC, you can use your account’s default network ACL or create custom network ACLs. 

# Security Group
The VPC component that checks packet permissions for an Amazon EC2 instance is a security group.
a security group denies all inbound traffic and allows all outbound traffic. You can add custom rules to configure which traffic to allow or deny.

# Global Networking
## Domain Name Server
![image](https://user-images.githubusercontent.com/43639867/193867066-ea46baab-10cd-4674-ad06-9b4203970789.png)
- When you enter the domain name into your browser, this request is sent to a DNS server. 

- The DNS server asks the web server for the IP address that corresponds to AnyCompany’s website.

- The web server responds by providing the IP address for AnyCompany’s website, 192.0.2.0.
## Amazon Route 53
- Amazon Route 53 is a DNS web service. It gives developers and businesses a reliable way to route end users to internet applications hosted in AWS. 

- Amazon Route 53 connects user requests to infrastructure running in AWS (such as Amazon EC2 instances and load balancers). It can route users to infrastructure outside of AWS.
-  ability to manage the DNS records for domain names. You can register new domain names directly in Route 53. You can also transfer DNS records for existing domain names managed by other domain registrars. This enables you to manage all of your domain names within a single location.
