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
