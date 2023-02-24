# EC2 Storage — the Big Picture
EC2 supports several storage options for your instances.

# Amazon Elastic Block Store (EBS)
EBS is a storage device (called a volume) that can be attached to (or removed from) your instance.
- Data Persists when the instance is nor running
- tied to one [[4 - Leveraging the AWS Global Infrastructure#Availability Zones or AZ|AZ]]
- Can only be attached to one instance in the same  [[4 - Leveraging the AWS Global Infrastructure#Availability Zones or AZ|AZ]]
> [!Recommend for:]
>- Quickly accessible data
>- Running a database on an instance
>- long-term storage

# EC2 Instance Store
An instance store is local sotrage that is physucally attached to the host computer and cannot be removed.

- Storage on disks physically attached to an instance
* *Faster with higher I/O speeds
* Storage is temporary since data loss occurs when the EC2 instance is stopped
>[!Recommended for:]
> -   Temporary storage needs
> -   Data replicated across multiple instances


# Amazon Elastic File System (EFS)
EFS is a serverless network file system for sharing files.
- Only supports the Linux file system
- More expensive than EBS
* *Accessible across different [[4 - Leveraging the AWS Global Infrastructure#Availability Zones or AZ|AZ]] in the same [[4 - Leveraging the AWS Global Infrastructure#Regions|region]]
>[!Recommended for:]
> -   Main directories for business-critical apps
> -   Lift-and-shift existing enterprise apps
