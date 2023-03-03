# EC2 Storage — the Big Picture
EC2 supports several storage options for your [[Exploring Compute Services_EC2#EC2 instances|EC2 instances]].

# Amazon Elastic Block Store (EBS)
EBS is a storage device (called a volume) that can be attached to (or removed from) your [[Exploring Compute Services_EC2#EC2 instances|EC2 instances]].
- Data Persists when the [[Exploring Compute Services_EC2#EC2 instances|EC2 instances]] is not running
- tied to one [[4 - Leveraging the AWS Global Infrastructure#Availability Zones or AZ|AZ]]
- Can only be attached to one instance in the same  [[4 - Leveraging the AWS Global Infrastructure#Availability Zones or AZ|AZ]]
> [!Recommend for:]
>- Quickly accessible data
>- Running a database on an instance
>- long-term storage

# EC2 Instance Store
An instance store is local storage that is physically attached to the host computer and cannot be removed.

- Storage on disks physically attached to an instance
* *Faster with higher I/O speeds
* Storage is temporary since data loss occurs when the [[Exploring Compute Services_EC2#EC2 instances|EC2 instances]] is stopped
>[!Recommended for:]
> -   Temporary storage needs
> -   Data replicated across multiple [[Exploring Compute Services_EC2#EC2 instances|EC2 instances]]


# Amazon Elastic File System (EFS)
EFS is a serverless network file system for sharing files.
- Only supports the Linux file system
- More expensive than [[EBS]]
* *Accessible across different [[4 - Leveraging the AWS Global Infrastructure#Availability Zones or AZ|AZ]] in the same [[4 - Leveraging the AWS Global Infrastructure#Regions|region]]
>[!Recommended for:]
> -   Main directories for business-critical apps
> -   Lift-and-shift existing enterprise apps

# Storage Gateway
Storage Gateway is a hybrid storage service.
- Connect on-premises and cloud data
- Supports a hybrid model
> [!Recommended for:]
>-   Moving backups to the cloud
> -   Reducing costs for hybrid cloud storage
>-   Low latency access to data


# AWS Backup
AWS Backup helps you manage data backups across multiple AWS services.
- Integrates with resources like [[EC2]], [[EBS]], [[EFS]], and more
- Create a backup plan that includes frequency and retention