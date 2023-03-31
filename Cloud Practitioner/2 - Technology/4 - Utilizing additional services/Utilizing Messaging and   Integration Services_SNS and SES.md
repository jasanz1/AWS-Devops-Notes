There are often times that users of your applications need to be notified when certain events happen.

# Simple Notification Service (SNS)

SNS allows you to send emails and text messages from your applications.
- Subscribers receive messages
- Send email and text messages
- Publish messages to a topic

## SNS in the Real World

Send an email when CPU utilization of an [[Exploring Compute Services_EC2#EC2 Instances|EC2 instance]] goes above 80%.
SNS works with CloudWatch when an alarm's metric threshold is breached to send an email.

# Simple Email Service (SES)

SES is an email service that allows you to send richly formatted HTML emails from your applications.
- *Ideal choice for marketing campaigns or professional emails
- Unlike SNS, SES sends HTML emails

## SES in the Real World

Send a marketing email and track open or click-through rates.
- SES allows you to send richly formatted HTML emails in bulk and gain valuable insights about the effectiveness of your campaign.