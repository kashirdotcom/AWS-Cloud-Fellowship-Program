# Global Networking in AWS
## Defination
A global network is a container for your network objects. When you create a global network, it's empty. After you create it, you can register your transit gateways and define your on-premises networks in the global network.

# Subnets and Network Access Control list in general and in context with AWS
## Network ACL
 - Network ACL allows or denies specific inbound or outbound traffic at the subnet level.
 - Combinations of Different Rules
 - An optional layer of security that acts as a firewall for controlling traffic in and out of a subnet.
 - Network ACL found in the firewall router or in a router connecting two internal networks.

### Network ACL Basics
- When we create VPC the Network ACL comes bydefult.
- each custom network ACL denies all inbound and outbound traffic until you add rules.
- One ACL connected to multiple subnets, But Subnet is connected to One ACL.
- Rules are from 1 to 32766.
- Network ACLs are stateless, which means that responses to allowed inbound traffic are subject to the rules for outbound traffic (and vice versa).


