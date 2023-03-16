# Amazon Route 53

Route 53 is a [[#DNS]] service that routes users to applications.
- Domain name registration
- Performs health checks on AWS resources
- Supports hybrid cloud architectures

# AWS Direct Connect

Direct Connect is a dedicated physical network connection from your on-premises data center to AWS.
- Dedicated physical network connection
- Connects your on-premises data center to AWS
- Data travels over a private network
- Supports a hybrid environment

## Direct Connect in the Real World

1. Large datasets
	- Transfer large datasets to AWS
2. Business-critical data
	- Transfer internal data directly to AWS, bypassing your internet service provider
3. Hybrid model
	- Build hybrid environments

# AWS VPN

Site-to-Site VPN creates a secure connection between your internal networks and your AWS VPCs.
- Similar to [[Direct Connect]], but data travels over the public internet
- Data is automatically encrypted
- Supports a hybrid environment
- Connects your on-premises data center to AWSConnects your on-premises data center to AWS

## Site-to-Site VPN in the Real World

- A Site-to-Site VPN makes moving applications to the cloud easier.
- a secure connection between your internal networks and AWS

# API Gateway

API Gateway allows you to build and manage APIs.
- Share data between systems
- Integrate with services like [[Lambda]]

# Terms

##### DNS

> DNS stands for Domain Name System and directs internet traffic by connecting domain names with web servers.