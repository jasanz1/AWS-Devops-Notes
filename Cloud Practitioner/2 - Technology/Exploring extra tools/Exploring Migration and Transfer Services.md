# The Bigger Picture
A lot of companies are migrating to the cloud, and they need inexpensive, fast, and secure ways to move their on-premises data to AWS.
# Database Migration Service (DMS)
DMS helps you migrate databases to or within AWS.
- Migrate on-premises databases to AWS
- Continuous data replication
- Supports homogeneous and heterogeneous migrations
- Virtually no downtime
## DMS in the Real World
Let's discuss when you would use DMS in the real world.
1. Oracle to Aurora MySQL
	- Migrate an on-premises Oracle database to Aurora MySQL
2. Oracle to Oracle
	- Migrate an on-premises Oracle database to Oracle on [[EC2]]
3. RDS Oracle to Aurora MySQL
	- Migrate an [[Relational Database Service (RDS)|RDS]] Oracle database to Aurora MySQL
# Server Migration Service (SMS)
SMS allows you to migrate on-premises servers to AWS.
- Migrates on-premises servers to AWS
- Server saved as a new Amazon Machine Image (AMI)
- Use AMI to launch servers as [[Exploring Compute Services_EC2#EC2 instances|EC2 Instance]]
# The Snow Family
The Snow Family allows you to transfer large amounts of on-premises data to AWS using a physical device.
- Snowcone
	- Smallest member of data transport devices
	- Offline shipping
	- Online with [[DataSync]]
	- 8 terabytes of usable storage
- Snowball
	- Transfer data in and out
	- Petabyte-scale data transport solution
	- Cheaper than internet transfer
	- Snowball Edge supports [[EC2]] and [[Lambda]]
- Snowmobile
	- Multi-petabyte or exabyte scale
	- Data loaded to [[S3]]
	- Securely transported
# DataSync
DataSync allows for online data transfer from
	on-premises to AWS storage services like [[S3]] or [[EFS]].
- Migrates data from on-premises to AWS
- Copy data over [[Direct Connect]] or the internet
- Replicate data cross-Region or cross-account
- Copy data between AWS storage services