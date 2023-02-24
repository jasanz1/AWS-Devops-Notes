
# The Bigger Picture
single [[4 - Leveraging the AWS Global Infrastructure#Regions|region]] contains multiple [[4 - Leveraging the AWS Global Infrastructure#Availability Zones or AZ|AZs]] contains multiple Data Centers Contains multiple [[Exploring Compute Services_EC2#Servers|Servers]] and a single server can contain multiple virtual servers[[Exploring Compute Services_EC2#EC2 instances|EC2 instances]]
(EC2 Instances are not considered serverless)

# Closer Look
EC2 is a foundational service used for managing your virtual instances.
1. You're able to provision an EC2 instance at the click of a button.
2. You can use a preconfigured template called an Amazon Machine Image(AMI) to launch your instance.
3. You can deploy your applications directly to EC2 instances.
4. You receive  750 compute hours per month on the [[Free Tier|free tier]] plan.

# EC2 in the real world
Let's discuss when you would use EC2 n the real world.
1. Deploy a database
	- Deploying a database to EC2 gives you full control over the database.
2. Deploy a web application
	- Deploy to multiple AZs to make the web application highly available.
# Methods to access an EC2 instance
1. AWS Management Console

	- You're able to configure and manage your instances via a web browser.

2. Secure Shell (SSH)
	- SSH allows you to establish a secure connection to your instance from your local laptop.
	-  the most common
		1. Generate a key pair
		2. Connect via SSH

3. EC2 Instance Connect (EIC)
	- EIC allows you to use IAM policies to control SSH access to your instances, removing the need to manage SSH keys.
	
4. AWS Systems Manager
	- Systems Manager allows you to manage your EC2 instances via a web browser or the AWS CLI.
# Ec2 Pricing Options
There are several pricing options to choose from for your EC2 instances.
## On Demand
- A fixed price in which you are billed down to the second based on instance type
	- there is not contract , and you pay only for what you use
- use On-Demand instances when:
	1. you care about low cost without any upfront payment or long0term commitment
	2. your application have unpredictable workloads that can't be interrupted
	3. your application are under development
	4. your workloads will not run longer then a year
> fun facts: you can reserve capacity using on-demand capacity reservations the EC2 capacity is held for you whether or not you run the instance
## Spot
- spot instances let you take advantage of unused EC2 capacity. your request is fulfilled only if capacity is available
- use Spot instances when:
	1. you are not concerned about the start or stop time of your application
	2. your workload can be interrupted
	3. your app is only feasible at very low compute prices
- fun facts:
	1. you can save up to 90% off on-demand prices
	2. you pay the spot price that's in effect at the beginning of each hour 
## Reserved instances (RIs)
- RIs allow you to commit to a specific instance type in a  particular [[4 - Leveraging the AWS Global Infrastructure#Regions|region]] for 1 or 3 years
- use RIs when
	1. you app has a steady state usage, and you can commit to 1 or 3 years
	2. you can pay money upfront in order to receive a discount on on-demand prices
	3. your app requires capacity reservation 
- fun facts
	 1. you can save up to 75% off on-demands proves
	 2. you care required to sign a contract
	 3. you can reserve capacity in an [[4 - Leveraging the AWS Global Infrastructure#Availability Zones or AZ|AZ]] for any duration
	 4. you can pay all upfront, partial upfront or no upfront. all upfront tfor the max term is the highest discount
	 5. provides convertible types at 54% discount
## Dedicated Hosts
- Dedicated hosts allow you to pay for a physical server that is fully dedicated to running your instances.
- use Dedicated hosts when:
	1. you want to bring your own server-bound software license from venders like Microsoft or oracle
	2. you have regulatory or corporate compliance requirements around tenancy model
- fun facts
	1. you can save up to 70% off on-demand prices.
	2. you bring your existing per-socket, per-core, or per-VM software licenses.
	3. there is no multi-tenancy, meaning the server is not shared with other customers
	4. a Dedicated host is a physical server whereas a Dedicated instance runs on the host
## Savings Plan
- Savings Plan allows you to commit to compute usage (measured per hour) for 1 or 3 years
- use Savings Plan when:
	1. you want to lower your bill across multiple compute services.
	you want the flexibility to change compute services, instance types, operating systems, or [[4 - Leveraging the AWS Global Infrastructure#Regions|regions]]
- fun facts:
	1. you can save up to 72% off on-demand prices
	2. you are not making a commitment to a dedicated host, just compute usage.
	3. savings can be shared across various compute services like [[EC2]], [[Fargate]], and [[Lambda]].
	4. this does not province a capacity reservation 
# Features
EC2 instances offer load balancing and Auto Scaling.
## [[0 - Key Terms#Elastic Load Balancing or ELB |Elastic Load Balancing]]
automatically distributes your incoming application traffic across multiple EC2 instances.
## EC2 [[0 - Key Terms#**Auto scaling** |Auto Scaling]]
adds or replaces EC2 instances automatically across AZs, based on need and changing demand
> [!note] HORIZONTAL SCALING OR SCALING OUT
> Auto Scaling reduces the impact of system failures and improves the availability of your applications.
> Do not confuse horizontal scaling with vertical scaling (or scaling up), which upgrades an EC2 instance by adding more power (CPU, RAM) to an existing server.
# Terms
###### Servers
> are the physical compute hardware running in a data center.
###### EC2 instances
> are the virtual servers running on these physical servers.