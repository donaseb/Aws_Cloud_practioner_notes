#  AWS Database Services

## Amazon Relational Database Service (Amazon RDS)
- Relational databases store data with defined relationships and use SQL to query data.
- Amazon RDS is a **managed relational database service** on AWS that automates:
  - Hardware provisioning
  - Database setup
  - Patching
  - Backups
- Supports encryption **at rest** and **in transit**.
- Available database engines:
  - Amazon Aurora
  - PostgreSQL
  - MySQL
  - MariaDB
  - Oracle Database
  - Microsoft SQL Server

### Amazon Aurora
- Enterprise-class relational DB compatible with MySQL and PostgreSQL.
- Up to 5x faster than MySQL and 3x faster than PostgreSQL standard databases.
- Cost-effective by reducing unnecessary I/O operations.
- Highly available: replicates 6 copies across 3 Availability Zones.
- Continuous backups to Amazon S3.

---

## Amazon DynamoDB (NoSQL, Non-Relational Database)
- Serverless key-value and document database.
- Tables contain items (rows) with attributes (columns).
- Delivers single-digit millisecond response times at any scale.
- Fully managed and automatically scales capacity.
- Data is redundantly stored across multiple Availability Zones and drives.
- Ideal for applications needing massive scalability and consistent low latency.
- No server management required (provisioning, patching, software updates handled by AWS).

---

## Amazon Redshift
- Data warehousing service for big data analytics.
- Enables collection and analysis of data from multiple sources.
- Helps identify relationships and trends across large datasets.

---

## AWS Database Migration Service (AWS DMS)
- Migrates data between source and target databases.
- Supports migration between different database types (e.g., Oracle to Aurora).
- Source database remains operational during migration, minimizing downtime.

---

## Additional AWS Database Services
- **Amazon Neptune**: Graph database designed for social networking, recommendation engines, and fraud detection.
