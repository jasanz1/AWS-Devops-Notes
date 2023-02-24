Lambda is a serverless compute service that lets you run code without managing servers.
- You author application code, called functions, using many popular languages.
- Serverless means you don’t worry about managing servers like with EC2.
- Scales automatically 
# The Bigger Picture
Lambda allows developers to focus on core business logic for the apps they are developing instead of worrying about managing servers.
# Lambda in the Real World
- Lambda is a building block for many [[#Serverless]] applications.
	1. Real-time file processing
	2. Sending email notifications
	3. Backend business logic
# Lambda Pricing Options
1. compute time
	 - Pay only for compute time used — there is no charge if your code is not running.
2. Request count
	- A request is counted each time it starts execution. Test invokes in the console count as well.
3. Always free
	- The free usage tier includes 1 million free requests each month.
# Features
1. Supports popular programming languages like Java, Go, PowerShell, Node.js, C#, Python, and Ruby.
2. You author code using your favorite development environment or via the console.
3. Lambda can execute your code in response to events.
4. Lambda functions have a 15-minute timeout.
# Terms
##### Serverless
> simply means AWS manages the servers for you and you cannot access them. You can pretend they don't exist.