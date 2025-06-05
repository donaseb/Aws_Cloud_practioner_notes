# AWS Identity and Access Management (IAM)

[AWS Identity and Access Management (IAM)](https://docs.aws.amazon.com/IAM/latest/UserGuide/introduction.html) enables you to manage access to AWS services and resources securely.

## AWS Account Root User

When you first create an AWS account, you begin with an identity known as the [root user](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_root-user.html).  
The root user is accessed by signing in with the email address and password that you used to create your AWS account.  
It has complete access to all the AWS services and resources in the account.

## IAM Users

An IAM user is an identity that you create in AWS. It represents the person or application that interacts with AWS services and resources.  
It consists of a name and credentials.  
By default, when you create a new IAM user in AWS, it has no permissions associated with it.  
You must grant the IAM user the necessary permissions.

## IAM Policies

An IAM policy is a JSON document that explicitly allows or denies permissions to AWS services and resources.

## IAM Groups

An IAM group is a collection of IAM users.  
When you assign an IAM policy to a group, all users in the group are granted permissions specified by the policy.

## IAM Roles

An IAM role is an identity that you can assume to gain temporary access to permissions.  
It is commonly used for granting permissions to applications, EC2 instances, or users from other AWS accounts.

## Multi-Factor Authentication (MFA)

Multi-factor authentication (MFA) adds an extra layer of security to your AWS account by requiring a second form of verification.

---

# AWS Organizations
- is a central location to manage multiple AWS accounts.

- You can group accounts into **Organizational Units (OUs)** to manage accounts with similar business or security requirements.
- When you apply a **Service Control Policy (SCP)** to an OU, all the accounts in the OU automatically inherit the permissions specified in the policy.

---

## AWS Artifact

- provides on-demand access to AWS security and compliance reports and select online agreements.

AWS Artifact has two main sections:
- **Artifact Agreements**: Manage your organization’s agreements with AWS.
- **Artifact Reports**: Access third-party audit reports of AWS services.

---

## AWS Shield

-is a managed DDoS protection service.

- **Shield Standard**: Automatically included at no extra cost.
- **Shield Advanced**: Offers additional detection and mitigation capabilities for higher levels of protection.

# Additional Security Services

## AWS Key Management Service (AWS KMS)

You must ensure that your applications’ data is secure while in storage (*encryption at rest*) and while it is transmitted (*encryption in transit*). Aws key management service enables you to perform encryption operations using cryptographic keys.  
A cryptographic key is a random string of digits used for locking (encrypting) and unlocking (decrypting) data.  
You can use AWS KMS to create, manage, and use cryptographic keys.

## AWS WAF

- is a web application firewall that lets you monitor network requests that come into your web applications.

## Amazon Inspector

- helps improve the security and compliance of applications by running automated security assessments.  
It checks for:
- Security vulnerabilities
- Deviations from best practices such as open EC2 access or outdated software

## Amazon GuardDuty

- is a threat detection service that continuously monitors:
- Network activity
- Account behavior  
To detect potential threats in your AWS environment.

---

# Monitoring

Monitoring refers to observing systems, collecting metrics, evaluating those metrics over time, and taking action based on insights.

## Amazon CloudWatch

- allows you to monitor your AWS infrastructure and applications in real time.  
It tracks and analyzes metrics sent by AWS services, and generates graphs and dashboards to visualize performance over time.

### CloudWatch Alarms

 allow you to take automated actions when metrics cross a predefined threshold (e.g., send notifications or trigger Auto Scaling).

### CloudWatch Dashboard

 provide a single view of all the metrics across your AWS resources in one place.

## AWS CloudTrail

 records API activity across your AWS account, including:
- API caller identity
- Time of API call
- Source IP address

This allows you to maintain a full audit trail of AWS account activity.

### CloudTrail Insights

is an optional feature that detects unusual activity in API calls and helps identify security risks or operational anomalies.

