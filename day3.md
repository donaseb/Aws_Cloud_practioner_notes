# Message and Queueing

This idea of placing messages into a buffer is called **messaging and queuing**. Messages are sent into the queue by Application A and they are processed by Application B. If Application B fails, Application A doesn't experience any disruption. Messages being sent can still be sent to the queue and will remain there until they are eventually processed. This is **loosely coupled**, which is what we strive to achieve with architectures on AWS.

### Amazon SQS (Amazon Simple Queue Service)
SQS allows you to send, store, and receive messages between software components at any volume. This is without losing messages or requiring other services to be available.  
- The data contained within a message is called a **payload**, and it's protected until delivery.  
- SQS queues are where messages are placed until they are processed.  
- AWS manages the infrastructure for you.  
- These queues scale automatically, are reliable, and are easy to configure and use.

### Amazon SNS (Amazon Simple Notification Service)
Amazon SNS is used to send messages to services and notifications to end users using a **publish/subscribe (pub/sub) model**.  
- You can create an SNS **topic**, which is a channel for message delivery.  
- **Subscribers** to the topic receive published messages.  
- SNS supports endpoints such as SQS queues, AWS Lambda, and HTTP/HTTPS webhooks.  
- It also supports mobile push, SMS, and email notifications.

---

# Additional Compute Services

### Serverless Compute
Serverless means the infrastructure is managed by AWS.  
- You do not manage provisioning, scaling, or maintenance.  
- You only focus on your code/application.

#### AWS Lambda
- Upload code into a **Lambda function**.  
- Configure a **trigger** (like an event or schedule).  
- Automatically runs code in a managed environment.  
- Designed for short executions (less than 15 minutes).  
- Ideal for use cases like web backends, microservices, and automation.

#### AWS Fargate
- A **serverless compute engine** for ECS/EKS.  
- No need to provision/manage servers.  
- AWS manages infrastructure for you.

---

## Containers

Containers provide a standard way to package application code and dependencies.

### Amazon ECS (Elastic Container Service)
- Highly scalable, high-performance **container orchestration**.  
- Supports **Docker containers**.  
- Allows running and scaling containerized applications.

---

# AWS Global Infrastructure

### AWS Regions
- Geographically isolated locations for deploying services.  
- Each region includes multiple **Availability Zones (AZs)**.

### Availability Zones
- One or more data centers with redundant power/networking.  
- Recommended: deploy across **at least two AZs** for high availability.

### Edge Locations
- Used by **Amazon CloudFront** for low-latency content delivery.  
- **AWS Outposts**: fully functional mini AWS regions in your own data center.

---

### AWS Elastic Beanstalk
- Simplifies provisioning of **EC2-based environments**.  
- You provide code and configuration; Beanstalk handles deployment.  
- Saves configurations for easy reuse.  
- Gives convenience with full visibility and control over resources.

### AWS CloudFormation
- **Infrastructure as Code (IaC)**.  
- Write templates to provision AWS resources automatically.  
- Ensures consistent, safe, and repeatable deployments.

---

# Networking

### Amazon Virtual Private Cloud (VPC)
- Provision a logically isolated section of AWS Cloud.  
- Define **private/public subnets** based on whether resources need internet access.

### Subnets
- Logical segments of the VPC's IP address range.  
- **Public subnet**: Connected to an internet gateway.  
- **Private subnet**: No direct internet access.

### Public-facing Resources
- Use an **Internet Gateway (IGW)** to allow public traffic.

### AWS Direct Connect
- Provides a **dedicated private fiber line** between your data center and AWS.

### Internet Gateway
- Attach to a VPC to enable **public access** to resources.

### Virtual Private Gateway
- Enables **VPN connections** to private resources in a VPC.  
- Allows traffic **only from approved networks**.

---

### Network Access Control Lists (ACLs)
- Stateless, **subnet-level** firewall.  
- Evaluates **inbound and outbound traffic** crossing subnet boundaries.  
- Custom ACLs deny all traffic until explicit rules are added.  
- Contains an implicit **deny rule** if no match is found.

### Security Groups
- Stateful, **instance-level** firewall.  
- Default: all inbound traffic is blocked, all outbound traffic allowed.  
- You define rules to allow specific traffic (e.g., HTTP, HTTPS).  
- **Remembers previous decisions**, unlike network ACLs.

---

## Subnets and Network Access Control Lists Summary

- **Public subnets** have access to the Internet Gateway; private do not.  
- **Network ACLs** check packets crossing subnet boundaries.  
- **Security groups** handle access at instance level (e.g., EC2).  
- Example packet flow:  
  1. Instance A sends packet to Instance B (different subnet).  
  2. Packet passes A’s security group (outbound traffic allowed).  
  3. Packet is evaluated by network ACL at subnet boundary.  
  4. If allowed, it continues to target subnet.

**Key Differences**:
- **Security Group**:  
  - Instance-level  
  - Stateful  
  - Allows outbound traffic by default  
  - Inbound traffic must be explicitly allowed  
- **Network ACL**:  
  - Subnet-level  
  - Stateless  
  - Evaluates each packet individually

---

# Network Traffic in a VPC

- Data is transmitted as **packets**.  
- Packets enter VPC via Internet Gateway.  
- **ACLs** evaluate packets entering/leaving subnets.  
- **Security Groups** evaluate packets targeting instances.  
- **Stateless ACL** vs. **Stateful Security Group**:  
  - ACL: doesn’t remember previous traffic.  
  - Security Group: remembers and allows related response traffic.

---

