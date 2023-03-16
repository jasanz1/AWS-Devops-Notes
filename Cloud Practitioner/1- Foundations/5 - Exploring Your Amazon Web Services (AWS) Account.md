# The AWS Management Console

The **AWS Management Console** allows you to access your AWS account and manage applications running in your account from a **web browser**.

The console has broad usage.

|new to cloud|Non-Technical Roles|Technical Roles|
|---|---|---|
|If you’re just getting started with the cloud.|If you serve in a non-technical role: business analyst, project manager, and many more.|If you serve in a technical role: software engineer, web developer, solutions architect, and many more.|

___

# Root User

- AWS accounts can have many users. use the email that was used to Initially create the AWS account will be associated with the root user.
- This is the user that Brought the AWS account into existence, and it's also the only user that can completely delete the AWS account, including all the resources that you've provisioned.
- root user must be secure. best Practice is to not to use the root user for day-to-day tasks in the AWS account highly suggested to use multi-factor Authentication on root user, which can be done from the [[0 - Key Terms# **Identity and Access Management or IAM**|IAM]] service.
___

# AWS Command Line Interface or CLI

 - Allows access your AWS account through a terminal or command line

## Programmatic Access

Programmatic access provides access to your AWS resources through an application or a tool like the CLI.

|Command Line Interface|Application Code|Software Development Kits or SDK|
|---|---|---|
|The CLI allows you to manage AWS services from a terminal session on your laptop.|AWS services can be accessed from application code using SDKs and programmatic calls.|SDKs allow you to access AWS services from popular programming languages like Java, Python, C#, and many more.|