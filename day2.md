# Benefits of Cloud Computing

- **On-Demand Resourcing**  
- **Scalability**  
- **Economy of Scale**  
- **Flexibility and Elasticity**  
- **Utility-Based Metering**: You only pay for what you use, and only while using it.  
- **Shared Infrastructure**: Virtual machines reduce the amount of physical hardware required, resulting in lower costs.

---

# Amazon EC2 Instance Types

Amazon EC2 instance types are optimized for different tasks. The instance families include:

- General Purpose  
- Compute Optimized  
- Memory Optimized  
- Accelerated Computing  
- Storage Optimized

## General Purpose Instances

Provide a balance of compute, memory, and networking resources.  
Ideal for:

- Web servers  
- Code repositories  
- Application servers  
- Workloads with balanced resource needs  

## Compute Optimized Instances

Ideal for compute-intensive tasks.  
Use cases include:

- High-performance web servers  
- Gaming servers  
- Scientific modeling  
- HPC (High-Performance Computing)  
- Batch processing  

## Memory Optimized Instances

Designed for memory-intensive workloads.  
Use cases:

- High-performance databases  
- Real-time big data processing  
- In-memory caches  
- Large-scale data analytics  

## Accelerated Computing Instances

Use hardware accelerators (coprocessors) for efficient processing.  
Ideal for:

- Floating-point calculations  
- Graphics processing  
- Pattern matching  
- Game and application streaming  

## Storage Optimized Instances

Optimized for workloads requiring high IOPS and local storage performance.  
Use cases:

- Distributed file systems  
- Data warehousing  
- High-frequency OLTP systems  
- Large-scale analytics on local data  

---

# AWS EC2 Pricing Models

## On-Demand

- Ideal for short-term, irregular workloads that cannot be interrupted.  
- No upfront commitment.  

## Savings Plan

- “Flexible discount subscription”  
- Commit to consistent usage (in $/hr) for 1 or 3 years.  
- Up to **72% savings** on compute usage.  
- Flexible across instance types and regions.  
- **Example**: You want savings without locking into a specific instance.

## Reserved Instances

- “Book in advance for a discount”  
- Best for steady-state workloads with predictable usage.  
- Up to **75% discount** vs On-Demand.  
- Term: 1 or 3 years.  
- Payment options:
  - All Upfront  
  - Partial Upfront  
  - No Upfront  
# AWS EC2 Pricing

## On-Demand

- Ideal for short-term, irregular workloads that **cannot be interrupted**.
- **Pay-per-hour** pricing.
- No upfront payment or long-term commitment.

## Savings Plan

- **Flexible discount subscription**.
- Offers low prices on EC2 usage in exchange for a commitment to a **consistent dollar-per-hour usage** for 1 or 3 years.
- Up to **72% savings** on compute usage.
- **Example**: You want savings without locking into a specific instance.

## Reserved Instances

- **Book in advance for a discount**.
- Best suited for **steady-state** or **predictable workloads**.
- Up to **75% discount** compared to On-Demand pricing.
- Commit to a **1 or 3-year term**.
- Payment options:
  - All Upfront
  - Partial Upfront
  - No Upfront

### Types of Reserved Instances

#### Standard Reserved Instances = “Fixed Plan with Bigger Discount”

🧠 Think of it like: A prepaid mobile plan where you commit to using one phone, one number, for one year.  
🪙 **Cheapest option**, up to **75% off** compared to On-Demand prices.  
🛑 Not flexible — cannot change instance type or region once booked.

✅ Best for:
- Steady apps that always run
- Known, long-term resource requirements

#### Convertible Reserved Instances = “Flexible Plan with Smaller Discount”

🧠 Think of it like: A phone plan where you can switch phones or change data packages, but you pay a bit more.  
💸 Less discount (up to **45%**) than Standard RIs.

✅ Best for:
- Users needing flexibility
- Apps or teams that may evolve over time

## Spot Instances

- “**Grab it when it’s cheap**”
- Request **spare EC2 capacity** for **up to 90% off** On-Demand price.
- AWS **can reclaim** the instance with a **2-minute warning**.
- Ideal for **interruptible workloads** like:
  - Batch processing
  - Data analysis
  - Image rendering

## Dedicated Hosts

- **Physical EC2 servers** dedicated to you.
- Useful for **compliance** or licensing requirements.
- **More expensive** than shared EC2.

---

## EC2 Pricing Summary Table

| Type         | Pay Style           | Best For                   | Cost   |
| ------------ | ------------------- | -------------------------- | ------ |
| On-Demand    | Pay-per-hour        | Short use or testing       | 💸💸💸 |
| Reserved     | 1/3-year commitment | Long-term steady use       | 💸     |
| Spot         | Bid-based           | Flexible jobs, batch tasks | 🪙     |
| Savings Plan | Spend commitment    | Cost-saving, flexible use  | 💸     |

> **Question**: Which Amazon EC2 pricing option provides a discount when you specify a number of EC2 instances to run a specific OS, instance family and size, and tenancy in one Region?  
> **Answer**: ✅ **Standard Reserved Instances**

---

# Scaling Amazon EC2

- **Scalability** means starting with minimal resources and **automatically scaling out or in** based on demand.
- You **only pay** for the resources you use.
- Managed via **Amazon EC2 Auto Scaling**.

## Amazon EC2 Auto Scaling

- Automatically adds/removes EC2 instances in response to application demand.
- Helps maintain performance and reduce cost.
- Ensures high availability for your application.

---

# Directing Traffic with Elastic Load Balancing (ELB)

- **Load balancer**: Receives and distributes incoming requests to backend EC2 instances.
- ELB is **automatically scalable** — handles increasing load without requiring configuration changes.

## How ELB Works with Auto Scaling

1. Auto Scaling launches new instances as demand grows.
2. ELB detects and starts routing traffic to them.
3. When demand drops:
   - ELB **drains** existing connections.
   - Auto Scaling **terminates** unused instances safely.

### Benefits

- Distributes traffic to avoid overload on any single instance.
- Acts as a **single entry point** to your Auto Scaling group.
- Maintains **high availability and fault tolerance**.

---

