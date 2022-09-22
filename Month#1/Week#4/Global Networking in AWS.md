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
### Network ACL rules
You can add or remove rules from the default network ACL, or create additional network ACLs for your VPC
1. Rule number - 1 to 32766 
2. Type - For Example, SSH
3. Protocol - such as IPv4, TCP or IP
4. Port range - for example HTTP for 80
5. Source - The source of the traffic (CIDR range) in InBound Rules
6. Destination - The destination for the traffic (CIDR range) in Outbound Rules
7. Allow/Deny - Whether to allow or deny the specified traffic.

### Default network ACL
- The default network ACL is configured to allow all traffic to flow in and out of the subnets with which it is associated
- This rule ensures that if a packet doesn't match any of the other numbered rules, it's denied. You can't modify or remove this rule.
### Custom network ACL
- It includes rules that allow HTTP and HTTPS traffic in (inbound rules 100 and 110).
- There's a corresponding outbound rule that enables responses to that inbound traffic (outbound rule 140, which covers ephemeral ports 32768-65535).

### Ephemeral ports
ephemeral ports may also be used for continuation of communications with a client that initially connected to one of the services listening with a well-known port.
- Many Linux kernels (including the Amazon Linux kernel) use ports 32768-61000.

- Requests originating from Elastic Load Balancing use ports 1024-65535.

- Windows operating systems through Windows Server 2003 use ports 1025-5000.

- Windows Server 2008 and later versions use ports 49152-65535.

- A NAT gateway uses ports 1024-65535.

- AWS Lambda functions use ports 1024-65535.

