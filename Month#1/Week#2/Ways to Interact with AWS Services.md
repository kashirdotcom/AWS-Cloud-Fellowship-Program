# Ways to Interact with AWS Services

## Following are the ways to Interact with AWS Services

1. AWS Console (GUI Based)   **Basic Level**
2. AWS CLI (Command Line)
3. AWS SDK's
4. Cloudformation

## AWS Console
A web based GUI, providing the ability to interact with the AWS services. We could use the console to launch, view, modify and remove any instance. As we login to the AWS portal we are provided with a simple and user friendly GUI from which we can search and use any service that we like. 

### Feature of AWS Console:

   - Easy to use and user friendly
   - Displays recently used services
   - Can easily pin most used services
   - Easy selection of AWS region
   - Account information can be viewed easily
   - Easy approach to AWS documentation via accessible links

#### Diagram of AWS Console
![console](https://user-images.githubusercontent.com/43639867/189488968-45b29393-a606-48d6-8818-66fd4d09c19b.png)


## AWS CLI
CLI alows us to manage the AWS environment using a terminal rather than a graphical interface, which is more quicker and easier. We can also create a script that contains all the commands to interact with different sercvices, So a single script can perform multiple actions. All AWS CLI commands start with aws keyword 

### For Example
- aws EC2
aws ec2 create-volume \
    --volume-type gp2 \
    --size 80 \
    --availability-zone us-east-1a
    
## AWS SDK's

AWS provides a number of Software Development Kits (SDKs) that allows interaction with the platform via code. SDKs are available for all the major programming languages, including:

    - Java
    - Python
    - Node.JS/ React.Js
    - Go.
    - Php
    
 ## Cloudformation
1. Uses for the IaaS (Infrasturucture as the Service)
2. Cloudformation is the way to go if we want to define the desired infrastructure within AWS, quickly and in a repeatable manner.

### Advantages
- Extremely flexible and powerful
- Infrastructure defined as code




