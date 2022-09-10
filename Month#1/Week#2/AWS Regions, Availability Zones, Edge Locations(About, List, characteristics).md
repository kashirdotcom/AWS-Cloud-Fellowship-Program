# AWS Regions, Availability Zones, Edge Locations(About, List, characteristics)

## Resources
https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-regions-availability-zones.html

## AWS Regions
### Defination
Different locations have the company data center and there names in the EC2 are called Regions
More Regions means that its covers the maximum area of the world.

### Key Points

1. Each Region is seperated
2. No Communication between two Regions
3. More Regions means more flexibility, scalability and stability.

## Availability Zones
1. Each Region has multiple, isolated locations known as Availability Zones. 
2. For example, us-east-1a.
3. An availability zone is a logical data center in a region available for use by any AWS customer. Each zone in a region has redundant and separate power, networking and connectivity to reduce the likelihood of two zones failing simultaneously.

## Local Zones
1. Local Zones have their own connections to the internet and support AWS Direct Connect, so that resources created in a Local Zone can serve local users with low-latency communications.
2. AWS Local Zones are a type of infrastructure deployment that places compute, storage, database, and other select AWS services close to large population and industry centers.
3. For example, us-west-2-lax-1.


## Wavelength Zones
1. AWS Wavelength enables developers to build applications that deliver ultra-low latencies to mobile devices and end users. 
2. Wavelength deploys standard AWS compute and storage services to the edge of telecommunication carriers' 5G networks
3. Wavelength brings the power of AWS to the network edge to enable latency sensitive use cases requiring near real-time responses. Processing at the network edge can help avoid transmitting large volumes of data over the network provider's infrastructure, and offload processing from mobile device hardware.
4. The code for a Wavelength Zone is its Region code followed by an identifier that indicates the physical location. For example, us-east-1-wl1-bos-wlz-1 in Boston.

## AWS Outposts
1. AWS Outposts is a fully managed service that extends AWS infrastructure, services, APIs, and tools to customer premises
2. An Outpost is a pool of AWS compute and storage capacity deployed at a customer site. AWS operates, monitors, and manages this capacity as part of an AWS Region. 
