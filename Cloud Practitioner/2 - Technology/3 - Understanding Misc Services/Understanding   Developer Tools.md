# The Bigger Picture

Let's discuss why developer tools are important.
Software developers use tools to accelerate the software development and release cycle.

# Cloud9

Cloud9 allows you to write code within an integrated development environment (IDE) from within your web browser.
- Supports popular programming languages
- Integrated development environment (IDE)
- Write and debug code

## Cloud9 in the Real World

Build serverless applications
- Cloud9 preconfigures the development environment with the needed SDKs and libraries. You can easily write the code for your [[Lambda]] function directly in your web browser.

# CodeCommit

CodeCommit is a source control system for private [[Git]] repositories.
- Create repositories to store code
- Commit, branch, and merge code
- Collaborate with other software developers

## CodeCommit in the Real World

Manage versions of source code files for your applications
- CodeCommit can be used to manage source code and the different versions of application files. CodeCommit is similar to GitHub.

# CodeBuild

CodeBuild allows you to build and test your application source code.
- Compiles source code and runs tests
- Produces build artifacts ready to be deployed
- Enables continuous integration and delivery

## CodeBuild in the Real World

Run tests before deploying a new version of an application to production
- CodeBuild allows you to run as many parallel streams of tests as needed, allowing you to deploy your changes to production more quickly.

# CodeDeploy

manages the deployment of code to compute services in the cloud or on-premises.
- Maintains application uptime
- Deploys code to [[EC2]], [[Fargate]], [[Lambda]], and on-premises.

## CodeDeploy in the Real World

Maintain application uptime when rolling out a new version
CodeDeploy eliminates the downtime of your application when deploying a new version due to its rolling deployments.

# CodePipeline

CodePipeline automates the software release process. Integrates with [[CodeCommit]] to retrieve source code
- Quickly deliver new features and updates
- Integrates with [[CodeBuild]] to run builds and unit tests
- Integrates with [[CodeDeploy]] to deploy your changes

## CodePipeline in the Real World

Add automation to the building, testing, and deployment of your application
- When combined with other developer tools, CodePipeline helps development teams implement DevOps practices that automate testing and the movement of code to production

# X-Ray

X-Ray helps you debug production applications.
- View requests end to end
- Analyze and debug production applications
- Map application components

## X-Ray in the Real World

Trace calls to an RDS database
- X-Ray can help you map requests made to your [[Relational Database Service (RDS)|RDS]] database from within your application. You can track information about the SQL queries generated and more.

# CodeStar

CodeStar helps developers collaboratively work on development projects.
- Contains issue tracking dashboard
- Developers connect their development environment
- Integrates with [[CodeCommit]], [[CodeBuild]], and [[CodeDeploy]]

## CodeStar in the Real World

CodeStar can manage the development pipeline