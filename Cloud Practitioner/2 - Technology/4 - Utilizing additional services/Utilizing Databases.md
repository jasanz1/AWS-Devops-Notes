In the AWS ecosystem, there are many different types of databases that support different use cases.

# Amazon Relational Database Service (RDS)

Supports popular database engines
- Launch read replicas across [[4 - Leveraging the AWS Global Infrastructure#Regions|Regions]] in order to provide enhanced performance and durability.
- Supports popular database engines
- Launch read replicas across [[4 - Leveraging the AWS Global Infrastructure#Regions|Regions]] in order to provide enhanced performance and durability.
- AWS manages the database with automatic software patching, automated backups, operating system maintenance, and more.

# Amazon Aurora

Aurora is a relational database compatible with MySQL and PostgreSQL that was created by AWS.
- Supports MySQL and PostgreSQL database engines
- Managed by [[Relational Database Service (RDS)|RDS]]
- Scales automatically while providing durability and high availability
- 5x faster than normal MySQL and 3x faster than normal PostgreSQL

# Amazon DynamoDB

DynamoDB is a fully managed NoSQL key-value and document database.
- NoSQL key-value database
- Fully managed and serverless
- Non-relational

# Amazon DocumentDB

DocumentDB is a fully managed document database that supports MongoDB.
- Document database
- MongoDB compatible
- Fully managed and serverless
- Non-relational

# Amazon ElastiCache

ElastiCache is a fully managed in-memory datastore compatible with Redis or Memcached.
- In-memory datastore
- Compatible with Redis or Memcached engines
- Data can be lost
- Offers high performance and low latency

# Amazon Neptune

Neptune is a fully managed graph database that supports highly connected datasets.
- Graph database service
- Supports highly connected datasets like social media networks
- Fully managed and serverless
- Fast and reliable

# Let's Take a Closer Look at Databases in the Real World

Although the databases on AWS support multiple use cases, let's look at the BEST option for each use case.
1. Migrate an on-premises Oracle database to the cloud.
	- RDS
2. Migrate an on-premises PostgreSQL database to the cloud.
	- RDS
	- Aurora
3. Alleviate database load for data that is accessed often.
	- ElastiCache
4. Process large sets of user profiles and social interactions.
	- Neptune
5. NoSQL database fast enough to handle millions of requests per second.
	- DynamoDB
6. Operate MongoDB workloads at scale.
	- DocumentDB