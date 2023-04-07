# The Bigger Picture

These services help you quickly stand up new applications, automate the management of infrastructure, and provide real-time visibility into system health.

# Infrastructure As Code (IaC)

IaC allows you to write a script to provision AWS resources. The benefit is that you provision resources in a reproducible manner that saves time.

# CloudFormation

CloudFormation allows you to provision AWS resources using Infrastructure as Code (IaC).
- Create templates for the resources you want to provision
- Provides a repeatable process for provisioning resources
- Works with most AWS services

## CloudFormation in the Real World

Automate the infrastructure-provisioning process for [[EC2]] servers
- You can use CloudFormation to automate the creation of [[Exploring Compute Services_EC2#EC2 Instances|EC2 instances]] in your AWS account

# Elastic Beanstalk

Elastic Beanstalk allows you to deploy your web applications and web services to AWS.
- Monitors application health via a health dashboard
- Orchestration service that provisions resources
- Automatically handles the deployment

## Elastic Beanstalk in the Real World

Quickly deploy a scalable Java-based web application to AWS.
After you upload your Java code, Elastic Beanstalk deploys it and handles capacity provisioning, load balancing, and Auto Scaling. Elastic Beanstalk even monitors the health of your application.

# OpsWorks

OpsWorks allows you to use Chef or Puppet to automate the configuration of your servers and deploy code.
- Deploy code and manage applications
- Manage on-premises servers or [[Exploring Compute Services_EC2#EC2 Instances|EC2 instances]] in AWS Cloud
- Works with Chef and Puppet automation platforms

## OpsWorks in the Real World

Automate software configurations and infrastructure management for your application.
- OpsWorks allows you to define software installation scripts and automate configuration for your application servers.