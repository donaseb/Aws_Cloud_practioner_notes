# AWS Cloud Adoption Framework (AWS CAF)

[AWS Cloud Adoption Framework (AWS CAF)] organizes guidance into six areas of focus, called **Perspectives**.  
In general, the **Business**, **People**, and **Governance** Perspectives focus on business capabilities,  
whereas the **Platform**, **Security**, and **Operations** Perspectives focus on technical capabilities.

---

## Migration Strategies

### 6 Strategies for Migration

1. **Rehosting**  
   Also known as “lift-and-shift,” involves moving applications without changes.  
   In large legacy migrations where quick scaling is essential, most applications are rehosted.

2. **Replatforming**  
   Also known as “lift, tinker, and shift,” involves minor cloud optimizations for tangible benefits  
   without changing the core architecture of the application.

3. **Refactoring (Re-architecting)**  
   Involves reimagining the application architecture using cloud-native features.  
   Driven by the need to add features, scale, or improve performance not possible in the existing setup.

4. **Repurchasing**  
   Involves moving from a traditional license to a **Software-as-a-Service (SaaS)** model.  
   Example: Migrating from a CRM system to Salesforce.com.

5. **Retaining**  
   Keeping critical applications in the source environment.  
   These may need major refactoring or can be migrated later.

6. **Retiring**  
   Removing applications that are no longer needed.

---

## AWS Snow Family

The [AWS Snow Family] is a collection of physical devices that help physically transport large volumes of data into and out of AWS.  
It includes:

- **AWS Snowcone**  
  A small, rugged, and secure edge computing and data transfer device.  
  - Specs: 2 CPUs, 4 GB memory, up to 14 TB storage.

- **AWS Snowball**  
  Two device types:
  - **Snowball Edge Storage Optimized**: Ideal for large-scale data migrations and recurring transfer workflows.
  - **Snowball Edge Compute Optimized**: Powerful for ML, video analysis, analytics, and edge computing.

- **AWS Snowmobile**  
  A truck-sized data transfer solution for exabyte-scale migrations.

---

## AI & Machine Learning Services

- **Amazon Q Developer**: A machine learning-powered code generator that gives real-time code recommendations.

- **AI Services**:
  - Convert speech to text with **[Amazon Transcribe]**.
  - Discover patterns in text with **[Amazon Comprehend]**.
  - Detect online fraud with **[Amazon Fraud Detector]**.
  - Build voice/text chatbots with **[Amazon Lex]**.

- **Machine Learning (ML)**:
  - Traditional ML development is complex and time-consuming.
  - **[Amazon SageMaker]** simplifies the process of building, training, and deploying ML models.
  - Use ML to analyze data, solve problems, and predict outcomes.

---


* Convert speech to text with Amazon Transcribe.
* Discover patterns in text with Amazon Comprehend.
* Identify potentially fraudulent online activities with Amazon Fraud Detector.
* Build voice and text chatbots with Amazon Lex.
- Traditional machine learning (ML) development is complex, expensive, time consuming, and error prone. AWS offers Amazon SageMaker to remove the difficult work from the process and empower you to build, train, and deploy ML models quickly.You can use ML to analyze data, solve complex problems, and predict outcomes before they happen.
- 
