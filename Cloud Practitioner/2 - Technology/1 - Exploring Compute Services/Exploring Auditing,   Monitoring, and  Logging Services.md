# The Bigger Picture

Let's discuss how auditing, monitoring, and logging fit in the bigger picture.
- These services give you insight into how well your systems are performing and help you proactively find and resolve errors.

### Questions

You can answer many questions using auditing, monitoring, and logging services on AWS.
1. Who signed in and made changes via the AWS Management Console?
2. What is the current load on this EC2 instance?
3. What is the root cause of this application error?
4. Which execution path resulted in this error?

# CloudWatch

CloudWatch is a collection of services that help you monitor and observe your cloud resources.
- Collects metrics, logs, and events
- Visualize logs
- Detect anomalies in your environment
- Set alarms

## CloudWatch in the Real World

Provide real-time monitoring on [[Exploring Compute Services_EC2#EC2 Instances|EC2 instances]].
- CloudWatch Alarms can notify you if an [[Exploring Compute Services_EC2#EC2 Instances|EC2 instances]] goes into the stopped state or usage goes above a certain utilization.
Receive a notification when root user activity is detected in your account.
- Create a CloudWatch event rule to notify you when root user API calls are detected in your account indicating root user activity.

# CloudTrail

CloudTrail tracks user activity and API calls within your account.
- Log and retain account activity
- Track activity through the console, SDKs, and CLI
- Identify which user made changes
- Detect unusual activity in your account

## CloudTrail in the Real World

Track the time a particular event occurred in your account.
- You can troubleshoot events over the past 90 days using the CloudTrail event history log to find the specific time an event occurred on a per-Region basis. You can create a custom trail to extend past 90 days.