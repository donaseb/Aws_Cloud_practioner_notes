## 🛰️ Global Networking

### ✅ Amazon Route 53 (DNS Service)
- **Purpose:** Translates domain names to IP addresses (DNS resolution).
- **Key Features:**
  - Domain registration and management.
  - Routing policies:
    - Latency-based
    - Geolocation
    - Geoproximity
    - Weighted round-robin
  - Integration with CloudFront and ELB for web delivery.

### ✅ DNS Resolution Flow (Example: AnyCompany)
1. User enters domain in browser.
2. Request goes to DNS resolver.
3. Resolver queries the authoritative DNS (e.g., Route 53).
4. Route 53 resolves domain to IP address (e.g., 192.0.2.0).
5. Traffic flows:
   - Route 53 → CloudFront → Load Balancer → EC2 instance.

---

## 💾 Storage & Databases

### ✅ EC2 Storage Options

#### 🔹 Instance Store
- **Temporary storage** tied to EC2 instance host.
- Data **lost** when instance stops or terminates.

#### 🔹 Amazon EBS (Elastic Block Store)
- **Persistent block storage**, independent of EC2 lifecycle.
- Features:
  - Volume configuration (size, type).
  - Snapshots (incremental backups).
  - Must be in the **same Availability Zone** as EC2.

#### 🔹 EBS Snapshots
- **Incremental backups**: only changed blocks are stored after the first snapshot.
- Used for:
  - Backup & recovery
  - Volume cloning
  - Region-to-region replication

---

### ✅ Amazon S3 (Simple Storage Service)
- Stores data as **objects** in **buckets**.
- Max object size: **5 TB**.
- Serverless, highly durable (99.999999999%).

#### 🔹 S3 Storage Classes

| Class                     | Use Case                              | AZ Redundancy | Retrieval Time       |
|--------------------------|----------------------------------------|----------------|-----------------------|
| S3 Standard              | Frequently accessed data               | ✅ 3 AZs        | Milliseconds          |
| S3 Standard-IA           | Infrequent but critical access         | ✅ 3 AZs        | Milliseconds          |
| S3 One Zone-IA           | Infrequent, reproducible data          | ❌ 1 AZ         | Milliseconds          |
| S3 Intelligent-Tiering   | Unknown or changing access patterns    | ✅ 3 AZs        | Automatically managed |
| S3 Glacier Instant       | Archived data, fast access             | ✅ 3 AZs        | Milliseconds          |
| S3 Glacier Flexible      | Archives with flexible SLA             | ✅ 3 AZs        | Minutes to hours      |
| S3 Glacier Deep Archive  | Long-term archives                     | ✅ 3 AZs        | 12 to 48 hours        |
| S3 Outposts              | On-premises S3 compatible storage      | ❌ Local        | Milliseconds          |

---

### ✅ Amazon EFS (Elastic File System)
- Fully-managed, **scalable NFS file system**.
- Supports shared access across **multiple EC2 instances**.
- Auto-scales from GBs to PBs.
- Data is stored across **multiple Availability Zones** (durable & available).
- Can connect from on-prem via **AWS Direct Connect**.

> 🔁 Unlike EBS (single AZ), EFS is **multi-AZ** and can be accessed by many instances concurrently.

---

