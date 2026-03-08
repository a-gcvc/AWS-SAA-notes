# AWS Services and Features

## **Gateway Endpoint**
- **Amazon S3**, **Amazon DynamoDB**

## **Networking**

- **Network Load Balancer** is Region bound
- **Elastic Network Adapter (ENA)** devices support enhanced networking via single root I/O virtualization (SR-IOV) to provide high-performance networking capabilities.
- **AWS PrivateLink** is a fully managed service that enables private connectivity between Virtual Private Clouds (VPCs), AWS services, and supported third-party SaaS applications over the AWS network, without exposing traffic to the public internet.
- **Public VIF** allows your on-premises router to access public AWS services (e.g., Amazon S3, DynamoDB) over a dedicated Direct Connect connection rather than the public internet.

## **Storage Services**

- **Amazon S3**
  - The maximum size of a file that you can upload using the **Amazon S3** console is 160 GB. To upload a file larger than 160 GB, use the AWS CLI, AWS SDKs, or Amazon S3 REST API.
  - **S3 Object Lambda** supports processing only GET, LIST, and HEAD requests. Any other requests return standard, non-transformed API responses. 
  - You can create a maximum of 1,000 Object Lambda Access Points per AWS account per Region.
- **DataSync** - data transfer service that makes it easy for you to automate moving data between on-premises storage and Amazon S3 or Amazon EFS.
- **AWS Transfer Family** provides fully managed support for file transfers directly into and out of Amazon S3 or Amazon EFS.
- **Amazon Cognito** user pools provide authentication, not authorization for AWS resources like S3.

## **Compute and Scaling**

- **AMI** can only be used in the region in which it is created.
- **Step Scaling** reacts only to real-time metrics (e.g., CPU utilization) using predefined steps.
- **Multi-AZ deployments** - synchronous
- **Read Replica** - asynchronous
- **EFA** - used for **HPC** (High-Performance Computing).

## **Load Balancing and Traffic Management**

- **Application Load Balancer (ALB)** cannot block or allow traffic based on geographic match conditions or IP-based conditions.
- **Elastic Load Balancer (ELB)** cannot distribute incoming traffic for targets deployed in different regions.
- **AWS Global Accelerator**:
  1. Associate static IPs to regional AWS resources such as NLBs, ALBs, EC2 instances, and Elastic IPs.
  2. Move endpoints between Availability Zones or AWS Regions without needing to update DNS configurations.
  3. Control traffic percentage for specific regions.
  4. Assign weights to endpoints within an endpoint group.

## **Messaging and Queues**

- **Dead-letter queues**: Used for debugging and isolating problematic messages.
- **Delay queues**: Used to postpone the delivery of messages for a specific duration (0 seconds to 15 minutes).
- **Temporary queues**: Serve as lightweight communication channels. They are API-compatible with static Amazon SQS queues.
- **Amazon SQS FIFO (First-In-First-Out) queues**: Designed for scenarios where the order of events is critical, and duplicates cannot be tolerated.
  
## **Databases**

- **DynamoDB** global tables have asynchronous replication across regions.
  
## **Caching**

- **Memcached**: 
  - Simple model
  - Supports multi-threading
  - Scalable with large nodes
  - Best for caching objects
- **Redis**: 
  - Fast, open-source, in-memory key-value store.
  - Not multi-threaded but ideal for caching, session management, gaming, and real-time analytics.

## **Web and API Services**

- **AWS WAF** cannot be directly configured on ALB but can be deployed on Amazon CloudFront, ALB, and API Gateway.
- **Amazon API Gateway HTTP APIs**:
  - Supports native JWT authorizers for OIDC-compliant identity providers like Auth0, Okta, or Amazon Cognito.
  - Optimized for low-latency, high-performance workloads, ideal for serverless apps requiring JWT validation.

## **Monitoring and Security**

- **AWS CloudTrail** cannot stream data to Amazon Kinesis.
- **AWS Firewall Manager**:
  - Allows centralized configuration of AWS WAF rules, AWS Shield Advanced protection, VPC security groups, AWS Network Firewalls, and Route 53 Resolver DNS Firewall rules across accounts and resources.
- **AWS CloudFormation StackSet**: 
  - Enables creation, update, or deletion of stacks across multiple accounts and regions using a single operation.
  
## **Cost Management**

- **Cost Optimization Hub**: Helps consolidate and prioritize cost optimization recommendations across AWS accounts and Regions.

## **Other Services**

- **AWS Transfer Family** only supports Amazon S3 and Amazon EFS as data stores.
- **Amazon Security Lake**: A fully managed service designed to collect, normalize, and centralize security-related data from various sources across AWS accounts, regions, and services.