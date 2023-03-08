# Data Warehousing
## The Bigger Picture
Let's take a closer look at data warehousing.
A data warehouse is a data storage solution that aggregates massive amounts of historical data from disparate sources. A data warehouse is a data storage solution that aggregates massive amounts of historical data from disparate sources.
## Amazon Redshift
Redshift is a scalable data warehouse solution.
- Handles exabyte-scale data
- Improves speed and efficiency
- Data warehousing solution
### Redshift in the Real World
Let's discuss when you would use Redshift in the real world.
1. Data consolidation
	- When you need to consolidate multiple data sources for reporting
2. Relational databases 
	- When you want to run a database that doesn't require real-time transaction processing (insert, update, and delete)
# Analytics
## The Bigger Picture
Analytics is the act of querying or processing your data.
-   There are several services that allow you to gain deeper insights, enhance decision-making, and act in real time to what your data is telling you.
## Athena
Athena is a query service for Amazon [[S3]].
- Query service
- Analyze [[S3]] data using SQL
- Pay per query
- Considered serverless
# Glue
Glue prepares your data for analytics.
- Prepare and load data
- Extract, transform, load (ETL) service
- Helps to better understand your data 
# Kinesis
Kinesis allows you to analyze data and video streams in real time.
- Analyze real-time, streaming data
- Supports video, audio, application logs, website clickstreams, and IoT
# Elastic MapReduce (EMR)
EMR helps you process large amounts of data.
- Works with big data frameworks
- Analyze data using Hadoop
- Process big data
# Data Pipeline
Data Pipeline helps you move data between compute and storage services running either on AWS or on-premises.
- Moves data at specific intervals
- Moves data based on conditions
- Sends notifications on success or failure
# QuickSight
QuickSight helps you visualize your data.
- Build interactive dashboards
- Embed dashboards in your applications
# Analytics in the Real World
Let's discuss when you would use analytics services in the real world.
1. Search data in [[S3]]
	- Athena helps you query historical data stored in [[S3]] as if they were relational data using standard SQL.
2. Log analytics
	- Kinesis helps you analyze logs in near real time for application monitoring or fraud detection.