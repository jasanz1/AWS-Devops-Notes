# The Bigger Picture
Let's discuss how content delivery fits in the bigger picture.

## What is a content delivery network (CDN)?
A CDN is a mechanism to deliver content quickly and efficiently based on geographic location.
Remeber [[4 - Leveraging the AWS Global Infrastructure#Latency|Latency]]

# Amazon CloudFront
CloudFront is a CDN that delivers data and applications globally with low latency.
- Makes content available globally or restricts it based on location
- Uses [[4 - Leveraging the AWS Global Infrastructure#Edge Locations|edge locations]] to cache content
- Speeds up delivery of static and dynamic web content
- if the content is already in the edge location, CloudFront delivers it immediately? If not, CloudFront retrieves the files from the origin.

# CloudFront in the Real World
1. S3 static websites
	 - CloudFront is often used with S3 to deploy content globally.
2. Prevent attacks
	- CloudFront can stop certain web attacks, like DDoS. We'll talk more about DDoS in the security lesson.
3. IP address blocking
	- Geo-restriction prevents users in certain countries from accessing conten

# Amazon Global Accelerator
Global Accelerator sends your users through the AWS global network when accessing your content, speeding up delivery.
* *Improves latency and availability of single-Region applications
* *Sends traffic through the AWS global network infrastructure
* *60% performance boost
* *Automatically re-routes traffic to healthy available regional endpoints

# Amazon S3 Transfer Acceleration
S3 Transfer Acceleration improves content uploads and downloads to and from S3 buckets
- Fast transfer of files over long distances
- Uses CloudFront’s globally distributed edge locations
- Customers around the world can upload to a central bucket