**Gateway endpoint**: Amazon S3, Amazon DynamoDB

**Network Load Balancer** is Region bound

**AMI** koristi samo u regionu u kojem je kreiran.

**Athena** cannot be used to analyze data in real time

**Step scaling** reacts only to real-time metrics, such as CPU utilization, using predefined steps. 

The maximum size of a file that you can upload by using the **Amazon S3** console is 160 GB. To upload a file larger than 160 GB, use the AWS Command Line Interface (AWS CLI), AWS SDKs, or Amazon S3 REST API.

**S3 Object Lambda** supports processing only GET, LIST, and HEAD requests. Any other requests don't invoke AWS Lambda and instead return standard, non-transformed API responses. You can create a maximum of 1,000 Object Lambda Access Points per AWS account per Region.

**DataSync** - data transfer service that makes it easy for you to automate moving data between on-premises storage and Amazon S3 or Amazon Elastic File System (Amazon EFS).

**AWS Transfer Family** provides fully managed support for file transfers directly into and out of Amazon S3 or Amazon EFS.

**Multi-AZ deployments** - syncrohronous

**Read Replica** - asynchronous

**AWS CloudTrail** cannot stream data to Amazon Kinesis.

You cannot associate an **AWS WAF ACL** with an **Amazon S3 bucket policy**.

You can't have applications consuming data streams from **Amazon Kinesis Data Firehose**, that's the job of Amazon Kinesis Data Streams.

**AWS WAF** cannot be directly configured on ALB. AWS WAF can be deployed on Amazon CloudFront, the Application Load Balancer (ALB), and Amazon API Gateway.

**Transfer Family** only supports Amazon S3 and Amazon EFS as data stores.

**DynamoDB** global table has asynchronous replication across regions.

**EFA** -> HPC

**Elastic Network Adapter (ENA)** devices support enhanced networking via single root I/O virtualization (SR-IOV) to provide high-performance networking capabilities.

**ELB** cannot distribute incoming traffic for targets deployed in different regions.

For each **VPC** that you want to associate with the **Route 53** hosted zone, change the following VPC settings to true:

    enableDnsHostnames

    enableDnsSupport

The following are the benefits of **temporary queues**:

    They serve as lightweight communication channels for specific threads or processes.

    They can be created and deleted without incurring additional costs.

    They are API-compatible with static (normal) Amazon SQS queues. This means that existing code that sends and receives messages can send messages to and receive messages from virtual queues.

**Dead-letter queues** are useful for debugging your application or messaging system because they let you isolate problematic messages to determine why their processing doesn't succeed. Amazon SQS does not create the dead-letter queue automatically. You must first create the queue before using it as a dead-letter queue.

**Delay queues** let you postpone the delivery of new messages to a queue for a number of seconds, for example, when your consumer application needs additional time to process messages. If you create a delay queue, any messages that you send to the queue remain invisible to consumers for the duration of the delay period. The default (minimum) delay for a queue is 0 seconds. The maximum is 15 minutes.

**Amazon SQS FIFO (First-In-First-Out) queues** are designed to enhance messaging between applications when the order of operations and events is critical, or where duplicates can't be tolerated. FIFO queues also provide exactly-once processing but have a limited number of transactions per second (TPS).

Choose **Memcached** if the following apply to you:

    You need the simplest model possible.

    You need to run large nodes with multiple cores or threads (support for multi-threading).

    You need the ability to scale out and in, adding and removing nodes as demand on your system increases and decreases.

    You need to cache objects.

**Redis**, which stands for Remote Dictionary Server, is a fast, open-source, in-memory key-value data store for use as a database, cache, message broker, and queue. Redis now delivers sub-millisecond response times enabling millions of requests per second for real-time applications in Gaming, Ad-Tech, Financial Services, Healthcare, and IoT. Redis is a popular choice for caching, session management, gaming, leaderboards, real-time analytics, geospatial, ride-hailing, chat/messaging, media streaming, and pub/sub apps.

Redis does not support multi-threading.

A **Public VIF** allows your on-premises router to access public AWS services, such as Amazon S3 and DynamoDB, over the dedicated Direct Connect connection rather than the public internet. When you establish a Public VIF, AWS advertises a set of public IP prefixes corresponding to its services, including Amazon S3. This allows your data center to communicate with these services using public IPs routed privately over Direct Connect, delivering improved performance, lower latency, and enhanced security. Public VIFs are specifically designed for scenarios where you want to connect on-premises infrastructure to AWS public endpoints over private, high-bandwidth links.

Using **AWS Firewall Manager**, you can centrally configure 
    AWS WAF rules, 
    AWS Shield Advanced protection, 
    Amazon Virtual Private Cloud (VPC) security groups, 
    AWS Network Firewalls, 
    and Amazon Route 53 Resolver DNS Firewall rules across accounts and resources in your organization.

**Amazon Cognito** user pools provide authentication, not authorization for AWS resources like S3.

**CloudFront** only supports ACM certificates that are created in the us-east-1 (N. Virginia) Region. 

By using **AWS Global Accelerator**, you can:

    1. Associate the static IP addresses provided by AWS Global Accelerator to regional AWS resources or endpoints, such as Network Load Balancers, Application Load Balancers, EC2 Instances, and Elastic IP addresses. The IP addresses are anycast from AWS edge locations so they provide onboarding to the AWS global network close to your users.

    2. Easily move endpoints between Availability Zones or AWS Regions without needing to update your DNS configuration or change client-facing applications.

    3. Dial traffic up or down for a specific AWS Region by configuring a traffic dial percentage for your endpoint groups. This is especially useful for testing performance and releasing updates.

    4. Control the proportion of traffic directed to each endpoint within an endpoint group by assigning weights across the endpoints.

An **Application Load Balancer** cannot block or allow traffic based on geographic match conditions or IP based conditions. 

**Amazon Kinesis Data Firehose** can only write to Amazon S3, Amazon Redshift, Amazon Elasticsearch or Splunk. You can't have applications consuming data streams from Amazon Kinesis Data Firehose, that's the job of Amazon Kinesis Data Streams.

**AWS PrivateLink** is a fully managed service that enables private connectivity between Virtual Private Clouds (VPCs), AWS services, and supported third-party SaaS applications over the AWS network, without exposing traffic to the public internet. 

The following are the characteristics of **security group rules**: 
    1. By default, security groups allow all outbound traffic. 
    2. Security group rules are always permissive; you can't create rules that deny access. 
    3. Security groups are stateful

**Cost Optimization Hub** is an AWS Billing and Cost Management feature that helps you consolidate and prioritize cost optimization recommendations across your AWS accounts and AWS Regions, so that you can get the most out of your AWS spend. 

**AWS CloudFormation StackSet** extends the functionality of stacks by enabling you to create, update, or delete stacks across multiple accounts and regions with a single operation. A stack set lets you create stacks in AWS accounts across regions by using a single AWS CloudFormation template. Using an administrator account of an "AWS Organization", you define and manage an AWS CloudFormation template, and use the template as the basis for provisioning stacks into selected target accounts of an "AWS Organization" across specified regions.

**Amazon API Gateway HTTP APIs** support native JWT authorizers, allowing developers to configure the API to automatically validate JWT tokens issued by an OIDC-compliant identity provider, such as Auth0, Okta, or Amazon Cognito. This eliminates the need for custom authentication logic in Lambda functions and reduces both latency and cost. HTTP APIs are optimized for low-latency, high-performance workloads and are more cost-effective than REST APIs, making them ideal for modern, serverless applications that require standard JWT validation and claim-based access control.

**Amazon Security Lake** is a fully managed, purpose-built service designed to automatically collect, normalize, and centralize security-related data from various AWS accounts, Regions, services, and even third-party sources. 

