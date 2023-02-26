# The Bigger Picture
Networking connects computers together and allows for the sharing of data and applications, around the globe, in a secure manner using virtual routers, firewalls, and network management services.
# Amazon Virtual Private Cloud (VPC)
VPC is a foundational service that allows you to create a secure private network in the AWS cloud where you launch your resources.
- Private virtual network
- Launch resources like [[EC2]] instances inside the VPC
- Isolate and protect resources
- A VPC spans [[4 - Leveraging the AWS Global Infrastructure#Availability Zones or AZ|AZ]] in a [[4 - Leveraging the AWS Global Infrastructure#Regions|Region]]
##### VPC peering allows you to connect 2 VPCs together.
- Peering facilitates the transfer of data in a secure manner.

# Terms
##### Subnet
> A subnet allows you to split the network inside the VPC this is where you launch resources like [[EC2]] instances
##### Network Access control list Or ACL
> A firewall/security layer on the subnet level to ensure the proper traffic is allowed into the subnet
##### Router and route table
> Defines where network traffic is routed
##### Internet gateway
> allows public traffic to the internet from a VPC