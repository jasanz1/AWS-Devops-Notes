# The Bigger Picture

Companies today need to collect, store, and analyze the data they've accumulated over the years on a massive scale. Storage services in the cloud provide a place for companies to store data.

S3 is an object storage service for the cloud that is highly available.
- Objects (or files) are stored in buckets (or directories).
- Objects can be public or private.
- Essentially unlimited storage that can hold millions of objects per bucket.
- You can upload objects via the console, the CLI, or programmatically from within code using SDKs.

# Let's Take a Closer Look

- You can set security at the bucket level or individual object level using access control lists (ACLs), bucket policies, or access point policies.
- You can enable versioning to create multiple versions of your file in order to protect against accidental deletion and to use a previous version.
- You can use S3 access logs to track the access to your buckets and objects.
- S3 is a regional service, but bucket names must be globally unique

# Data Accessibility

Durability and availability are 2 very different aspects of data accessibility
1. Durability
	- Durability is important so you objects are never lost or compromised

	> [!note] Amazon S3 Standard is designed for 99.999999999% (11 9’s) of durability.

2. availability
	- Availability is important so you can access your data quickly when you need it.

	> [!note] Amazon S3 Standard is designed for 99.99% availability.

# S3 Storage Classes

Amazon S3 offers several storage classes designed for different use cases.
 1. S3 Standard
	- General-Purpose
	- Data sorted across multiple [[4 - Leveraging the AWS Global Infrastructure#Availability Zones or AZ|AZ]]
	- Low latency and high throughput

	> [!Recommended for]
	> Frequently accessed data

	> Durability of 99.999999999%
	> Availability of 99.99%

 2. S3 intelligent-Tiering
	- Automatically move your data to the most cost effective storage class
	- Automatic cost saving
	- No retrieval fees
	- Data stored across multiple [[4 - Leveraging the AWS Global Infrastructure#Availability Zones or AZ|AZ]]

	> [!Recommended for]
	> Data with unknown or changing access pattern

	> Durability of 99.999999999%
	> Availability of 99.9%

 3. S3 Standard Infrequent Access (IA)
	- data accessed less frequently but requrs rapid access
	- data stored across multiple [[4 - Leveraging the AWS Global Infrastructure#Availability Zones or AZ|AZ]]
	- cheaper than S3 standard

 	> [!Recommended for]
 	> Long-Lived data
 	> Infrequently accessed
 	> millisecond access when needed

	> Durability of 99.999999999%
	> Availability of 99.9%

 4. S3 One Zone- infrequent Access (IA)
	- Like S3 Standard-IA but data stored in single [[4 - Leveraging the AWS Global Infrastructure#Availability Zones or AZ|AZ]]
	- Cost 20% less than S3 standard-IA
	- Data sotred in this storage class can be lost

	> [!Recommended for]
	> Re-creatable data
	> infrequently accessed with millisecond access
	> availability and durability are not essential

	> Durability of 99.999999999%
	> Availability of 99.95%

 5. S3 Glacier (now S3 Glacier Flexible retrieval)
	- Long-term data storage and archival lower costs
	- data retrieval takes longer
	- 3 retrieval options:
		- 1-5 mins
		- 3-5 hours
		- 5-12 hours
	- Data stored across multiple Availability Zones

	> [!Recommended for]
	> Long-term backups
	> Cheaper storage options

	> Durability of 99.999999999%

6. S3 Glacier Instant Retravel
	- Long-term data storage and archival lower costs
	- data retrieval takes longer
	- more expensive then flexible
	- Data stored across multiple Availability Zones

	> [!Recommended for]
	> Long-term backups
	> Cheaper storage options

	> Durability of 99.999999999%

 7. S3 Glacier Deep Archive
	 - like S3 Glacier but longer access times
	 - 2 retrieval options
		 - 12 hours
		 - 48 hours
		 - Cheapest of all s3 options
	 - data stored across multiple [[4 - Leveraging the AWS Global Infrastructure#Availability Zones or AZ|AZ]]

 	> [!Recommended for]
 	> Long-term data archival accessed once or twice a year
 	> Retaining data for regulatory compliance

	> Durability of 99.999999999%

 8. S3 Outposts
	- Provides object storage on-premises
	- a single storage class
	- store data across multiple devices and servers

	> [!Recommended for]
	> Data that needs to be kept local
	> Demands application performances needs

# S3 in the Real World

1. Static websites
	- Deploy static websites to S3 and use CloudFront for global distribution
2. Data archive
	- Archive data using Amazon Glacier as a storage option for Amazon S3.
3. Analytics systems
	- Store data in Amazon S3 for use with analytics services like Redshift and Athena.
4. Mobile applications
	- Mobile application users can upload files to an Amazon S3 bucket.