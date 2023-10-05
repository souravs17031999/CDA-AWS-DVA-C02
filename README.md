# CDA-AWS-DVA-C02
AWS Certified Developer - Associate

# Development with AWS Services

## AWS FUNDAMENTALS 

### EC2
### EC2 INSTANCE STORAGE

#### ROUTE 53

![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/cea5818e-24cd-4b8c-9c3d-bf014e8686e8)  

- A – maps a hostname to IPv4
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/78ac182b-8b53-41e2-9ce7-72ac7515ab88) 

- AAAA – maps a hostname to IPv6
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/01f09dae-f4c1-4f34-93f0-28cb372480ec)  

- CNAME – maps a hostname to another hostname
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/478400c8-d1f1-4f27-a36b-b58a2cad1048)  

  - The target is a domain name which must have an A or AAAA record
  - Can’t create a CNAME record for the top node of a DNS namespace (Zone Apex)
  - Example: you can’t create for example.com, but you can create for www.example.com
- NS – Name Servers for the Hosted Zone
  - Control how traffic is routed for a domain
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/e37637cd-8a4a-482b-ae0d-ac18243b96f0)  

- HOSTED ZONES 
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/ad90c870-6f2a-4ac4-a51e-5d28a3f64fc3)

- CNAME VS ALIAS
- ALIAS TARGETS
- A type of record that you can create with Amazon Route 53 to route traffic to AWS resources such as Amazon CloudFront distributions and Amazon S3 buckets.
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/cf1e572e-cdda-465d-b6bf-42cbf67c9fec)

- You cannot set an ALIAS record for an EC2 DNS name

- Routing policies: Simple routing policy, Failover routing policy, Geolocation routing policy, Geoproximity routing policy, Latency routing policy, weighted (load balancing across regions) etc...

![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/dcdc14bf-961b-4676-bd15-e9dc8c05c453)  
- Traffic flow policy   
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/681c1805-7d88-4a02-83aa-d94ccc4256ac)    
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/745b789a-0cdf-459f-97a8-822d860185bb)
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/a899e27c-ac42-4be5-9710-4c94455d0c4f)
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/c80e3625-7013-4a0d-9d7d-3c2b22cdf508)
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/a9aa57c9-ea86-4f5d-9e5e-984348d30e9e)
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/04b8dee5-056e-4f18-8720-71ece0faa4fa)  
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/39104857-33d7-458f-ab2b-f7d6ec2a18e4)  
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/2c2599bb-51c9-4865-b8bb-df6c287192c3)  

- Combining health checks
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/6b040a3f-c33a-4810-ad49-c80a12154f7f)  
 

#### ELB + ASG
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/2b945445-6cdc-4994-9aba-3a4955afe965)
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/6edb04fe-025b-406d-a0cc-b6a33e7a8add)
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/d410d447-59e8-4979-adf5-993b4bbfdb3f)
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/135d9fab-f0c3-4042-8656-54391efd5ef0)
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/acea93ce-c429-4548-838b-500172a5e3c8)
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/3508b60b-8a4f-4084-92dc-1ba38b4956df)
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/c2757128-d6f3-4488-b89c-bd2019c53ebc)   
- Session affinity/stickness
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/bc03ff3c-4db6-4bf0-bfea-6aeb588d8ed7)
- SNI solves the problem of loading multiple SSL certificates onto one web server (to serve multiple websites)
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/229f4a86-056a-4fbf-9efe-5be846800de6)
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/80f8c4ab-5ad2-44f0-a124-d8f7ce1cd4c3)

#### VPC 
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/ce9cfd04-fa4f-4fa9-99d2-e1a23c104c40)
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/4f535f71-e1ca-47d1-aa2f-c163019f0afd)  
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/b6ed9a1f-ab38-4f21-9ff6-1b7d85108823)
- NACL
  - Can have ALLOW and DENY rules
  - Are attached at the Subnet level
  - Rules only include IP addresses
- SECURITY GROUPS
  - A firewall that controls traffic to and from an ENI / an EC2 Instance
  - Can have only ALLOW rules
  - Rules include IP addresses and other security groups
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/8146682e-85f4-45b0-9f40-fd794a0754d4)
- VPC Flow logs
- VPC peering
  - VPC Peering connection is not transitive (must be established for each VPC that need to communicate with one another)
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/3aea1cdf-062e-47e8-8935-cafd0f4d1c60)  
- VPC endpoints
  - Endpoints allow you to connect to AWS Services using a private network instead of the public www network

![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/65645ab5-f9a3-4f8d-b6f6-76da609ec553)   

![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/b7cd1997-0311-4fc0-b5bb-556717623ef0)  

#### RDS
- MULTI-AZ DEPLOYMENTS

  - MULTI-AZ INSTANCE DEPLOYMENTS
    - Amazon RDS automatically provisions and maintains a synchronous standby replica in a different Availability Zone. The primary DB instance is synchronously replicated across Availability Zones to a standby replica
    - ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/b090d1a7-8d62-40b1-9929-fafbd8e83ca4)
  - MULTI-AZ CLUSTER DEPLOYMENTS
    - A Multi-AZ DB cluster has a writer DB instance and two reader DB instances in three separate Availability Zones in the same AWS Region.
    - semisynchronous replication, which requires acknowledgment from at least one reader DB instance in order for a change to be committed.
    - ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/9e20dbcd-349b-41aa-95dd-1109d51f55c4)
  - CROSS REGION DEPLOYMENTS
    - ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/213e62da-f664-4a65-a2d2-9c290654e403)
    - when you perform a cross-Region restore of a DB snapshot, first you copy the snapshot to the desired Region. Then, you can restore the DB snapshot to a new DB instance.

  - RDS PROXY

#### ELASTICCACHE
- CACHE STRATEGIES

  - READ ASIDE (LAZY LOADING)
    ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/d28499e6-4473-4e8b-991f-64522048883d)  

  - WRITE ASIDE
    ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/e1405aaf-c712-4877-91ef-e221fff7fcac)   

  - READ THROUGH
   ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/440f41a6-217d-495f-bc73-ee5bc3131bdd)  
     
  - WRITE THROUGH
    ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/a4b871be-7fce-49d4-b347-19617dc4355e)

  - WRITE BACK
    ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/8200ab1d-e247-4054-97a4-1bbd875b2890)   


#### ECS, ECR, FARGATE, DOCKER 
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/3203bd9b-2b8e-4665-9d96-efb010cc00de)
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/1df65b06-0fa4-450a-a28b-ba21367561c7)
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/fa3c42ed-2402-4b21-a694-2398d11cd305)
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/fb6957a9-6784-4c37-9beb-2af1b980fb03)
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/eef7c504-c461-4008-9e8e-43677ee36a74)
- ROLLING UPDATES
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/26f3b6ca-5049-49ca-bba7-fdc7a14e4fce)
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/0dd357ca-80ca-40a0-9e28-768567f6e91e)  
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/a1501f07-a120-4c9c-92bb-690032919475)
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/1165e87f-94bb-4779-b51f-27f5b72f6398)
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/38d4f995-0fa1-4fc0-82b6-089d802697ed)
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/c8c1a769-3ed6-478f-ae20-b64683f110a4)


#### CloudFront
- Improves read performance, content is cached at the edge
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/0ed8c808-eb63-463e-b7d3-5f70aa7415bb)
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/d673b0be-dde3-44fc-a5de-22084e83e250)
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/813b075e-43b0-4930-84c6-44d88ae845c8)
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/692f2293-22a1-47f5-89cc-b79c26ea6496)
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/59330963-923b-43c6-a6de-9494d184bb7c)
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/5161e0e2-defd-4d14-8b2d-e22968221950)

## AWS LAMBDA FUNCTION
- AWS Lambda is a compute service that lets you run code without provisioning or managing servers.
- With Lambda, all you need to do is supply your code in one of the language runtimes that Lambda supports.
- The Lambda service runs your function only when needed and scales automatically. You only pay for the compute time that you consume—there is no charge when your code is not running.

**When to Use Lambda**
- File processing: Use Amazon Simple Storage Service (Amazon S3) to trigger Lambda data processing in real time after an upload.
- Stream processing: Use Lambda and Amazon Kinesis to process real-time streaming data for application activity tracking, transaction order processing, clickstream analysis, data cleansing, log filtering, indexing, social media analysis, Internet of Things (IoT) device data telemetry, and metering.
- Web applications: Combine Lambda with other AWS services to build powerful web applications that automatically scale up and down and run in a highly available configuration across multiple data centers.
- IoT backends: Build serverless backends using Lambda to handle web, mobile, IoT, and third-party API requests.
- Mobile backends: Build backends using Lambda and Amazon API Gateway to authenticate and process API requests. Use AWS Amplify to easily integrate with your iOS, Android, Web, and React Native frontends.

**Pricing**
- Request pricing: Free tier of 1,000,000 AWS Lambda requests
- Duration pricing: 400,000 GBs (400,000 SECONDS IF 1 GB RAM) of compute time
- Data transfer with AWS Lambda Functions is free in the same AWS Region between the following services: S3, SNS, SQS ETC...
- Data transferred “in” to and “out” of your AWS Lambda functions, from outside the region the function executed, will be charged at the Amazon EC2 data transfer rates

**Language support**
- Node.js (JavaScript) • Python • Java (Java 8 compatible) • C# (.NET Core) • Golang • C# / Powershell • Ruby • Custom Runtime API (community supported, example Rust)
- • Lambda Container Image • The container image must implement the Lambda Runtime API

![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/c5d36b0f-bcf6-45bd-9274-fa17f3e29254)     
- Ex. 
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/2e182266-52f8-434f-8e27-6dffaca1853b)  
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/720c396d-7351-4a5b-b2bd-abeb60d3192f)   

**Key features**
- Use environment variables to adjust your function's behavior without updating code.
- Manage the deployment of your functions with versions
- Create a container image for a Lambda function by using an AWS provided base image or an alternative base image so that you can reuse your existing container tooling

**Concepts**
- programming model:
  - The programming model defines the interface between your code and the Lambda system.
  - You tell Lambda the entry point to your function by defining a handler in the function configuration
  - The runtime passes in objects to the handler that contain the invocation event and the context, such as the function name and request ID.
  - When the handler finishes processing the first event, the runtime sends it another.
  - The function's class stays in memory, so clients and variables that are declared outside of the handler method in initialization code can be reused.
  - The runtime captures logging output from your function and sends it to Amazon CloudWatch Logs.
  - Lambda scales your function by running additional instances of it as demand increases, and by stopping instances as demand decreases.
- Execution environment:
  - The execution environment manages the resources required to run your function.
  - The execution environment also provides lifecycle support for the function's runtime and any external extensions associated with your function.
  - The function's runtime communicates with Lambda using the Runtime API. Ex. ```/runtime/invocation/next```, ```/runtime/invocation/AwsRequestId/response```, ```/runtime/init/error```, ```/runtime/invocation/AwsRequestId/error```
    ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/80fa5e71-3edf-4f13-a9c3-e16a3fd8df68)
  - Execution environment lifecycle 
    ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/04ab3e72-bb9e-4eea-bc3f-0a6ef9ae3e25)
    - Init phase capped at 10 seconds
    - Invoke phase capped as configurable by the user (total execution time + extensions)
    - Shutdown phase capped at 2 seconds
  - After the function and all extensions have completed, Lambda maintains the execution environment for some time in anticipation of another function invocation.
  - When you write your function code, do not assume that Lambda automatically reuses the execution environment for subsequent function invocations.
- Deployment packages: container images, .zip archives
- Private networking: A Lambda function always runs inside a VPC owned by the Lambda service. Lambda applies network access and security rules to this VPC and Lambda maintains and monitors the VPC automatically.
- Concurrency controls: reserved concurrency, provisioned concurrency
- Lambda offers built-in HTTP(S) custom endpoint support through function URLs.
- When you invoke a function, you can choose to invoke it synchronously or asynchronously. With synchronous invocation, you wait for the function to process the event and return a response. With asynchronous invocation, Lambda queues the event for processing and returns a response immediately.
- Event source mapping:
  - An event source mapping is a resource in Lambda that reads items from an Amazon Simple Queue Service (Amazon SQS) queue, an Amazon Kinesis stream, or an Amazon DynamoDB stream, and sends the items to your function in batches.
  - maintain a local queue of unprocessed items and handle retries if the function returns an error or is throttled
  - customize batching behavior and error handling, or to send a record of items that fail processing to a destination.
    
- **Tuning for optimal Performance**:
  - If your application is CPU-bound (computation heavy), increase RAM
  - Timeout: default 3 seconds, maximum is 900 seconds (15 minutes)
  - The execution context is a temporary runtime environment that initializes any external dependencies of your lambda code: can be reused for multiple invocations reducing latency and increasing speed of execution
  - ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/626e7bc1-7a50-42b0-9187-f232dde7b3be)
  - /tmp space directory: If your Lambda function needs disk space to perform operations (Max 10GB)
  - To encrypt content on /tmp, you must generate KMS Data Keys
  - Concurrency limit: up to 1000 concurrent executions
  - Can set a “reserved concurrency” at the function level (=limit)
  - Each invocation over the concurrency limit will trigger a “Throttle”
    • Throttle behavior:
    • If synchronous invocation => return ThrottleError - 429
    • If asynchronous invocation => retry automatically and then go to DLQ
  - ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/7ba37227-5039-4fa7-96d4-1682c7f1388a)
  - Cold Start:
    • New instance => code is loaded and code outside the handler run (init)
    • If the init is large (code, dependencies, SDK…) this process can take some time.
    • First request served by new instances has higher latency than the rest
  - Provisioned concurrency:
    - Concurrency is allocated before the function is invoked (in advance)
    - So the cold start never happens and all invocations have low latency


  
  ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/5c631f78-c45b-466c-8270-2ce14de63506) 

**How does it works**
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/1868d3ec-718e-4d0e-ac80-4f7d7e072e6f)
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/f60bb556-38bd-419c-aa50-e07006f9e835)
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/bc8cf5f1-efaf-4b41-ab65-a354783d09bf) 

**Working Example Basic lambda function deploy**
- Basic python lambda handler  
  ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/682d9cbc-459e-4f05-a07b-219ebdd97b6f)   
- General Configuration: memory, timeout, roles/permissions etc....
  ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/88bc6fe7-4e6f-4449-b6f4-6c44fedf816c)
- Monitoring cloudwatch
  ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/69929e1d-d782-4bb1-8bb9-32dc0406154a)
- Logging cloudwatch
  ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/48628f90-5d08-45ec-80d0-14776205d3e8)
- Execution role
  ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/9a1907d3-b473-49a0-a327-93e6505a1dd3)
- Versioning: A published version is a snapshot of your function code and configuration that can't be changed
  ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/edbeb769-3edb-4e16-adaf-10036da6bf05)
- Environment Variables: When you publish a version, the environment variables are locked for that version along with other. Some environment variables are reserved and set by lambda runtimes. For ex. ```AWS_DEFAULT_REGION```, ```_X_AMZN_TRACE_ID``` etc...
  ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/19df7b7e-efa2-4e8b-a2e2-b408770d0c5d)
  ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/e5c8efd7-38f6-4f39-8803-4fba5a706cee)
  ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/2e376aa6-20ac-4445-9a28-d7d0f59b71dd)
- Securing Environment variables
  - Security at rest: Lambda always provides server-side encryption at rest with an AWS KMS key
  - Security at transit: For additional security, you can enable helpers for encryption in transit, which ensures that your environment variables are encrypted client-side for protection in transit.

**Invoking Lambda functions**
- You can invoke Lambda functions directly using the Lambda console, a function URL HTTP(S) endpoint, the Lambda API, an AWS SDK, the AWS Command Line Interface (AWS CLI), and AWS toolkits
- You can also configure other AWS services to invoke your function in response to events or external requests, or on a schedule.
- For another AWS service to invoke your function directly, you need to create a trigger using the Lambda console. A trigger is a resource you configure to allow another AWS service to invoke your function when certain events or conditions occur. Multiple triggers can co-exist independently and each event that Lambda passes to your function has data from only one trigger.
- For your Lambda function to process items from a stream or a queue, such as an Amazon Kinesis stream or an Amazon Simple Queue Service (Amazon SQS) queue, you need to create an event source mapping. An event source mapping is a resource in Lambda that reads items from a stream or a queue and creates events containing batches of items to send to your Lambda function. Each event that your function processes can contain hundreds or thousands of items.
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/46f255b1-39a3-4948-ba7a-6691df9727e8)  

  - **Synchronous invokation**  
    - With synchronous invocation, you wait for the function to process the event and return a response.
    - Ex. User Invoked:
    • Elastic Load Balancing (Application Load Balancer)
    • Amazon API Gateway
    • Amazon CloudFront (Lambda@Edge)
    • Amazon S3 Batch
    • Service Invoked:
    • Amazon Cognito
    • AWS Step Functions
    • Other Services:
    • Amazon Lex
    • Amazon Alexa
    • Amazon Kinesis Data Firehose   
    - Default response
    ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/6cda5d89-0445-4854-bf0e-2d6b324b929a)
    - The payload is a string that contains an event in JSON format. The name of the file where the AWS CLI writes the response from the function is response.json
    - If the function returns an object or error, the response is the object or error in JSON format. If the function exits without error, the response is null.
    - If Lambda was able to run the function, the status code is 200, even if the function returned an error.

  - **Asynchronous invokation**  
      • Amazon Simple Storage Service (S3)
      • Amazon Simple Notification Service (SNS)
      • Amazon CloudWatch Events / EventBridge
      • AWS CodeCommit (CodeCommitTrigger: new branch, new tag, new push)
      • AWS CodePipeline (invoke a Lambda function during the pipeline, Lambda must callback)
      ----- other -----
      • Amazon CloudWatch Logs (log processing)
      • Amazon Simple Email Service
      • AWS CloudFormation
      • AWS Config
      • AWS IoT
      • AWS IoT Events   
    - Lambda queues the event for processing and returns a response immediately. For asynchronous invocation, Lambda handles retries and can send invocation records to a destination.
    ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/b9553267-d04a-4317-a1e6-f1403d00c6f8)  
    ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/4f2e39ad-2749-4499-bdd0-69bbbf8307ef)
    - Returns statusCode "202" here for success/failure 

    - For asynchronous invocation, Lambda places the event in a queue and returns a success response without additional information.
    - A separate process reads events from the queue and sends them to your function
    ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/f96290f1-fb34-4760-8e2b-0af82624cfb6)
    - Lambda will perform retries with exponential backoff incase of failure of async invokation of event
    - If the function returns an error, Lambda attempts to run it two more times, with a one-minute wait between the first two attempts, and two minutes between the second and third attempts.
    -  For throttling errors (429) and system errors (500-series), Lambda returns the event to the queue and attempts to run the function again for up to 6 hours. The retry interval increases exponentially from 1 second after the first attempt to a maximum of 5 minutes.
    -  Events might also get deleted from queue if it becomes too late to process them.
    -  Send invokation record to SNS, SQS, AWS LAMBDA, EVENTBRIDGE
    -  The invocation record contains details about the request and response in JSON format. You can configure separate destinations for events that are processed successfully, and events that fail all processing attempts.
    -   dead-letter queue for discarded events: For dead-letter queues, Lambda only sends the content of the event, without details about the response.
    -   If Lambda can't send a record to a destination you have configured, it sends a DestinationDeliveryFailures metric to Amazon CloudWatch.
    -   ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/47bb9c7c-1714-4455-921b-c296de97ed51)
    -   ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/9d249bdc-0d3e-443f-856e-8aa334891261)
    -   A dead-letter queue acts the same as an on-failure destination in that it is used when an event fails all processing attempts or expires without being processed. However, a dead-letter queue is part of a function's version-specific configuration, so it is locked in when you publish a version.
    -   To reprocess events in a dead-letter queue, you can set it as an event source for your Lambda function. Alternatively, you can manually retrieve the events.
    -   Choose an Amazon SQS standard queue if you expect a single entity, such as a Lambda function or CloudWatch alarm, to process the failed event.
    -   Choose an Amazon SNS standard topic if you expect multiple entities to act on a failed event. For example, you can configure a topic to send events to an email address, a Lambda function, and/or an HTTP endpoint.
    -   ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/0d8ca1d1-f096-49d1-b247-f35a1eb1cf93)   

    -   If you're using Amazon SQS as an event source, configure a dead-letter queue on the Amazon SQS queue itself and not on the Lambda function.

**Event Source Mappings**
- An event source mapping is a Lambda resource that reads from an event source and invokes a Lambda function i.e. cases when services can't directly invoke lambda functions.
- Ex of such services: Amazon DynamoDB, Amazon Kinesis, Amazon MQ, Amazon Managed Streaming for Apache Kafka (Amazon MSK), Self-managed Apache Kafka, Amazon Simple Queue Service (Amazon SQS), Amazon DocumentDB (with MongoDB compatibility) (Amazon DocumentDB)
- An event source mapping uses permissions in the function's execution role to read and manage items in the event source.
- For event source mapping to be created, we need ARN of that stream resource.
- Lambda event source mappings process events at least once due to the distributed nature of its pollers.
- By default, an event source mapping batches records together into a single payload that Lambda sends to your function based on Either of follwing conditions: The batching window reaches its maximum value (time), The batch size is met, The payload size reaches 6 MB.
- Events needs to be polled from source, Your Lambda function is invoked synchronously.
- For DLQ in case of events failure, DLQ should be on SQS itself and not on lambda function since it's synchronous invocation and DLQ on Lambda only works with async invocations.
- Streaming via Kineses/DynamoDB
  - A Kinesis data stream is a set of shards. Each shard contains a sequence of data records. A consumer is an application that processes the data from a Kinesis data stream. You can map a Lambda function to a shared-throughput consumer (standard iterator), or to a dedicated-throughput consumer with enhanced fan-out.
  ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/cea817ac-f548-4e9c-83ca-56b7c07e4f3e)
  ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/59ba1153-011e-48c6-827a-aab5331df1ae)  
- SQS standard/SQS FIFO queues
  - Lambda reads messages in batches and invokes your function once for each batch. When your function successfully processes a batch, Lambda deletes its messages from the queue.
  ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/231fda0c-d6de-4b98-beef-53e50ceb8aea)
  ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/b11c1182-24e2-4dc3-a94b-4bd2637c6c9a) 
  - By default, Lambda polls up to 10 messages in your queue at once and sends that batch to your function. To avoid invoking the function with a small number of records, you can tell the event source to buffer records for up to 5 minutes by configuring a batch window. Before invoking the function, Lambda continues to poll messages from the SQS standard queue until the batch window expires, the invocation payload size quota is reached, or the configured maximum batch size is reached.

 ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/c3a8503d-9ecb-4ae6-87d5-ec7d8054263f)  

**LAMBDA DESTINATIONS**
- More control other than simple DLQ for async invocations
- Sucess and failure events from async invocation both can be sent to multiple targets (destinations) and discarded batch of events from eventsource mappings (sync invocation) can be sent.
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/1afa73bc-2beb-4987-8bd2-d552bc211dee)
- Destinations provide more useful capabilities by passing additional function execution information, including code exception stack traces, to more destination services.


**Event Filtering**
- control which records from a stream or queue Lambda sends to your function. For example, you can add a filter so that your function only processes Amazon SQS messages containing certain data parameters.
- By default, you can define up to five different filters for a single event source mapping.
- Your filters are logically ORed together. If a record from your event source satisfies one or more of your filters, Lambda includes the record in the next event it sends to your function.
- A filter criteria (FilterCriteria) object is a structure that consists of a list of filters (Filters).
- Your filter pattern can include metadata properties (fields containing information about the event that created the record. ) , data properties (fields of the record containing the data from your stream or queue) , or both.
- Ex.
  ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/eced0654-e933-45ee-8f1b-3246991df575)

**ERRORS SCENARIOS HANDLING FOR LAMBDA**
- Asynchronous invocation: You can configure a dead-letter queue on the function to capture events that weren't successfully processed.
- Event source mappings: you determine the length of time between retries and destination for failed events by configuring the visibility timeout and redrive policy on the source queue.
- AWS services: services decide whether to retry or to relay the error back to requester.

**Recursive loop detection**
- If your function is invoked more than 16 times in the same chain of requests, then Lambda automatically stops the next function invocation in that request chain and notifies you.
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/785f34bd-d248-40a6-a590-686c926cb0ef)

**Security Auth for Lambda endpoint Function URL**
- Dedicated HTTP(S) endpoint for your Lambda function
• A unique URL endpoint is generated for you (never changes)
• https://<url-id>.lambda-url.<region>.on.aws (dual-stack IPv4 & IPv6)
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/121e5d11-df88-4835-ae7b-b6be32cc7a99)  
- Access your function URL through the public Internet only. Doesn’t support PrivateLink (Lambda functions do support).

- ```AWS_IAM```: users who need to invoke your Lambda function URL must have the ```lambda:InvokeFunctionUrl``` permission. Depending on who makes the invocation request, you may have to grant this permission using a resource-based policy.
- ```NONE```: you may want your function URL to be public. For example, you might want to serve requests made directly from a web browser. To allow public access to your function URL. However, users must still have ```lambda:InvokeFunctionUrl``` permissions in order to successfully invoke your function URL.
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/8407892f-ae7a-4c9a-aa40-aa24c34854e4)  


**AWS IAM PERMISSIONS FOR LAMBDA**
- LAMBDA EXECUTION ROLE: Grants the Lambda function permissions to AWS services / resources
  ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/ad296769-f704-4822-9931-d57802bc1141)
- Use resource-based policies to give other accounts and AWS services permission to use your Lambda resources.

**ENVIRONMENT VARIABLES**
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/7962ebeb-656f-4007-9004-d7ced36e2d6b)
- Security of environment variables
  - At REST
    - Lambda always provides server-side encryption at rest with an AWS KMS key. By default, Lambda uses an AWS managed key. 
  - At TRANSIT
    - For additional security, you can enable helpers for encryption in transit, which ensures that your environment variables are encrypted client-side for protection in transit.
    - Environment variables to communicate with X-Ray
    • _X_AMZN_TRACE_ID: contains the tracing header
    • AWS_XRAY_CONTEXT_MISSING: by default, LOG_ERROR
    • AWS_XRAY_DAEMON_ADDRESS: the X-Ray Daemon IP_ADDRESS:PORT
- Your AWS Lambda function can interact with AWS Secrets Manager using the Secrets Manager API or any of the AWS Software Development Kits (SDKs). You can also use the AWS Parameters and Secrets Lambda Extension to retrieve and cache AWS Secrets Manager secrets in Lambda functions without using an SDK

**Lambda layers**
- A Lambda layer is a .zip file archive that contains supplementary code or data. Layers usually contain library dependencies, a custom runtime, or configuration files.
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/34e3aaf3-3687-4f7d-ac55-00183cee9a8b)
- Lambda extracts the layer contents into the /opt directory in your function’s execution environment. This gives your function access to your layer content.
- You can include up to five layers per function. Also, you can use layers only with Lambda functions deployed as a .zip file archive.
- You should be able to import any library that you’ve added as a layer to the current function.
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/ee86556d-ea15-4cdf-9d30-e2ecaf748d6e)  

**TRACEABILITY**
- Lambda integrates with ```AWS X-Ray``` to help you trace, debug, and optimize Lambda applications. You can use X-Ray to trace a request as it traverses resources in your application, which may include Lambda functions and other AWS services.

**Few Lambda Commands**
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/4f90ecb2-6630-47b9-932c-ddfcd6081757)   
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/65275ca7-7895-4dd8-8659-1762113d321b)   

### Lambda Integrations 

**Lambda + ALB**  
- When the load balancer forwards the request to a target group with a Lambda function as a target, it invokes your Lambda function and passes the content of the request to the Lambda function, in JSON format.
- Elastic Load Balancing invokes your Lambda function synchronously with an event that contains the request body and metadata.
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/53fb96e7-9c09-4753-abf9-ec3c49fb44fc)
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/6920e4ee-4fb9-4126-97f3-1eb911e58aa1)
- If requests from a client or responses from a Lambda function contain headers with multiple values or contains the same header multiple times, or query parameters with multiple values for the same key, you can enable support for multi-value header syntax. After you enable multi-value headers, the headers and query parameters exchanged between the load balancer and the Lambda function use arrays instead of strings. If you do not enable multi-value header syntax and a header or query parameter has multiple values, the load balancer uses the last value that it receives.
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/052a8c88-e7c0-44d5-ae62-b3c7e36e5c73)
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/3a92c8a1-eaab-41d3-b2e2-709f82790517)
- Permissions 
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/06c48ab3-7fd2-4ff2-85b5-aef64edb1485)

**Lambda + ALB**

![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/55f26f79-17e5-4f4c-9b01-4049c8fac106)    
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/6a34d023-b816-4cc0-ae2d-356b35971fc9)   
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/02fee79b-1736-4172-a858-3ed3b9f3f76c)   
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/80d83231-b41a-48ba-90e1-07b52113f037)  
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/c9212f76-7146-4d38-9a07-5eaa1278f0cf)  
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/905d7413-b078-448e-b9fb-be8bb22d6b6a)   
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/34a96f12-f621-4fd2-82b3-511ff245e103)   
![tempsnip](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/6d066c92-d829-4523-ae4f-48c471a95b25)  

**Lambda + SQS (DLQ)**
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/9318acd9-289f-4892-b465-cb8102e0e533)
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/08a76795-1d88-4529-b029-e852c7215133)   
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/14292f1c-2d3d-4bb8-8504-61906f883c4d)   
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/fb29b551-b888-43fc-b105-80ec310642ff)  
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/335038b4-a1de-46c1-8a10-43796a36614d)  
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/83510582-3a88-439e-9cbd-631f95a43a7d)  
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/2b6ed1bd-5533-4be0-8a04-44a136c4643f)  
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/ce5cc5f1-d797-4a38-b2c4-29255d6bdcfb)  
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/4c06a472-9552-4752-a74f-ebc7270ddc1b)  
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/72f91c18-0de3-45c8-be81-4c0f1ba22dba)   
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/6e211af9-afeb-4c8a-bdf2-67a401464095)  
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/fd30c380-3b53-47a5-98e1-f8b16bdff9ec)  
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/9e33d1b0-3ca0-43b5-801a-c9b686a4488b)  

**Lambda + Cloudwatch events/EventBridge**
- EventBridge (CloudWatch Events) helps you to respond to state changes in your AWS resources.
- With EventBridge (CloudWatch Events), you can create rules that match selected events in the stream and route them to your AWS Lambda function to take action.
- You can also create a Lambda function and direct AWS Lambda to invoke it on a regular schedule. You can specify a fixed rate (CRON expression).
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/6e584023-c75d-471e-a4dd-34c6d454065f)
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/dca51139-ff06-4e79-ac8c-763b67683982)
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/065da954-6c07-4e3f-afd5-9f3e1325da70)
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/b5586409-4824-4a0b-8f39-c4cf5622d61b)
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/0104bc31-a9e7-4475-a702-c848698a3996)
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/f0de7719-4a1a-4656-a633-dba73a0a16a8)
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/d2838bfa-0fee-437a-a682-8ad56df11fc4)

**Lambda + S3**  
- Amazon S3 can send an event to a Lambda function when an object is created or deleted. You configure notification settings on a bucket, and grant Amazon S3 permission to invoke a function on the function's resource-based permissions policy.
- Amazon S3 invokes your function asynchronously with an event that contains details about the object.
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/7780ecdd-6219-4fde-99c0-233ec1ecc7f0)
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/76dbe87c-53a5-4ec7-8ea4-c86d40f6dd4a)
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/332a761c-ff45-4ed7-a3a2-98a96ae88bb9)
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/e8fe1836-2507-4acf-88b0-c7e65a2b92a9)
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/7e22ed62-6326-47e6-9f0d-92bbf5f4705f)
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/fabcd3a0-31af-46c3-9e6b-8006a0279114)
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/0821b2d2-4abd-4f50-9ff7-9f25e82f682f)

**Lambda + EventSourceMappings (SQS)**  
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/fd0720fe-71c4-488d-9536-2a0a846e9eba)  
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/eab22360-dcf9-4a60-97c4-0a29fa30ee33)   
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/d5f6eb13-6ead-492f-b320-225fa631e04a)   
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/1f8a7c9a-b947-4209-907e-0661677c3776)   
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/80e2ae78-0c13-4327-b7fd-52f77eafabe6)   

**LAMBDA@EDGE + CLOUDFRONT**
- Lambda@Edge is an extension of AWS Lambda that lets you deploy Python and Node.js functions at Amazon CloudFront edge locations. A common use case of Lambda@Edge is to use functions to customize the content that your CloudFront distribution delivers to your end users.
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/6ec008b7-f878-49b7-9e73-885242bc4edd)
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/8733baf0-e876-4462-adb6-7805d8bcd85f)
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/24569365-fb27-450a-a740-820db72aa0b3)

**Lambda + VPC (Virtual private cloud)**
- By default, your Lambda function is launched outside your own VPC (in an AWS -owned VPC)
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/b5dfedb8-1260-4751-893b-44e9898980e6)
- Lambda will create an ENI (Elastic Network Interface) in your subnets
• AWSLambdaVPCAccessExecutionRole
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/ef3e77be-abda-4d2f-8534-a4604b148548)
- Deploying a Lambda function in a public subnet does not give it internet access or a public IP
- Deploying a Lambda function in a private subnet gives it internet access if you have a NAT Gateway / Instance
- You can use VPC endpoints to privately access AWS services without a NAT
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/3751e9c3-4da5-4751-8a81-03ecb36d2025)
- Note: Lambda - CloudWatch Logs works even without endpoint or NAT Gateway
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/5df528ec-38ba-4f62-873e-6686e281b3f5)  
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/404b6492-36f0-4d11-bd3f-aae2ac338b79)     
- You can connect other VPCs to the VPC with interface endpoints using VPC peering.
- Traffic between peered VPCs stays on the AWS network and does not traverse the public internet. Once VPCs are peered, resources like Amazon Elastic Compute Cloud (Amazon EC2) instances, Amazon Relational Database Service (Amazon RDS) instances, or VPC-enabled Lambda functions in both VPCs can access the Lambda API through interface endpoints created in the one of the VPCs.

**Lambda + EFS (elastic file system)**
- You can configure a function to mount an Amazon Elastic File System (Amazon EFS) file system to a local directory.
- For performance and resilience, use at least two Availability Zones. For example, in a simple configuration you could have a VPC with two private subnets in separate Availability Zones. The function connects to both subnets and a mount target is available in each.
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/35192b0d-e873-45e5-a7c9-47052b6207ab)
- You can configure a function to mount an Amazon EFS file system in another AWS account. For this to happen, it needs: VPC peering must be configured, The security group for the Amazon EFS file system you want to mount must be configured to allow inbound access from the security group associated with your Lambda function., Subnets must be created in each VPC with matching Availability Zone (AZ) IDs., DNS Hostnames must be enabled in both VPCs.
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/3662025d-7738-4c68-8a66-fa894c0f9e5f)
  
**Lambda + CloudFormation**
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/c37edab7-9bd8-4716-a0ad-4821324e0f66)
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/4e8a1048-95d0-4fd0-bef6-9d0d7eb8a433)
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/09d6b4af-c7fa-4a42-8d64-1af1fd0db202)   

**Lambda container images**
- Deploy Lambda function as container images of up to 10GB from ECR
- Pack complex dependencies, large dependencies in a container
- Base images are available for Python, Node.js, Java, .NET, Go, Ruby
- Can create your own image as long as it implements the Lambda Runtime API
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/3c91c287-9baa-4cde-a83d-c994a34d0a45)
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/52b973c4-3e95-4169-905d-86a13ea4279d)

**Lambda versions and aliases**
- Aliases are ”pointers” to Lambda function versions
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/e69c526d-8c81-448a-b995-2edcddfea091)
- ```CodeDeploy``` can help you automate traffic shift for Lambda aliases
- Linear: grow traffic every N minutes until 100%
  • Linear10PercentEvery3Minutes
  • Linear10PercentEvery10Minutes
  • Canary: try X percent then 100%
  • Canary10Percent5Minutes
  • Canary10Percent30Minutes
  • AllAtOnce: immediate
- Can create Pre & Post Traffic hooks to check the health of the Lambda function

**Lambda Insights and Profiler**
- Gain insights into runtime performance of your Lambda functions using ```CodeGuru``` Profiler 
- ```AmazonCodeGuruProfilerAgentAccess``` policy to your function  

![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/514b6aa1-1c83-4d37-899e-6eb06c1d42c0)   

## AWS STEP FUNCTIONS 
- AWS Step Functions is a serverless orchestration service, Through Step Functions' graphical console, you see your application’s workflow as a series of event-driven steps.
- Written in JSON notation 
- Step Functions is based on state machines and tasks.
- In Step Functions, a workflow is called a state machine, which is a series of event-driven steps. Each step in a workflow is called a state.
- A Task state represents a unit of work that another AWS service, such as AWS Lambda, performs.  
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/700e7c1c-260b-472f-b7ff-50430fe96389)   

**Standard workflows**
- Standard workflows have exactly-once workflow execution and can run for up to one year. This means that each step in a Standard workflow will execute exactly once.

**Express workflows**
- Express workflows, however, have at-least-once workflow execution and can run for up to five minutes. This means that one or more steps in an Express Workflow can potentially run more than once, while each step in the workflow executes at least once.

![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/2b501d00-4418-4983-98e0-6580551e2c46)   

**Use Cases**

- You create a workflow that runs a group of Lambda functions (steps) in a specific order. 
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/91385fb5-209d-4ad8-8c6d-c07116a50ff1)
- Using a Choice state, you can have Step Functions make decisions based on the Choice state’s input  
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/2eb87b17-635b-4dbf-a25b-58263aac7aa3)
- Retry/Catch
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/f91b2b14-834e-4dac-84b7-4f5819c00b3b)
- With a callback and a task token, you have Step Functions tell Lambda to send your customer’s money and report back when your customer’s friend receives it.
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/30ace6f2-9448-4e7e-955c-0718aade1a14)
- Using a Parallel state, Step Functions inputs the video file, so Lambda can process it into the five display resolutions at the same time.
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/94a4609a-6711-4f5d-bc22-38cf5d28ea53)
- Using a Map state, Step Functions has Lambda process each of your customer's items in parallel.
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/dcf25e5e-6d18-4e64-8c9c-5544eaa84b9b)   

**states**

- ```Choice State``` -Test for a condition to send to a branch (or default branch)
- ```Fail or Succeed State``` - Stop execution with failure or success
- ```Pass State``` - Simply pass its input to its output or inject some fixed data, without performing work.
- ```Wait State``` - Provide a delay for a certain amount of time or until a specified time/date.
- ```Map State``` - Dynamically iterate steps.
- ```Parallel State``` - Begin parallel branches of execution.   
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/c4add06a-d2b3-47f7-8de0-17b0a6126f91)   

**Error handling**

- All states, except Pass and Wait states, can encounter runtime errors.
- Predefined error codes:   
• ```States.ALL``` : matches any error name   
• ```States.Timeout```: Task ran longer than TimeoutSeconds or no heartbeat received  
• ```States.TaskFailed```: execution failure  
• ```States.Permissions```: insufficient privileges to execute code
- Instead of the application handling the error handling mechanisms, retry and catch fallbacks can be used as cross cutting concerns
- Retry examples   
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/d30154e7-f8a3-49fd-aed7-ffdc29ddf7aa)
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/bec5f5e5-fef3-4e45-b031-7b091df5ad79)   

- Catch fallbacks
- When a state reports an error and either there is no Retry field, or if retries fail to resolve the error, Step Functions scans through the catchers in the order listed in the array. When the error name appears in the value of a catcher's ErrorEquals field, the state machine transitions to the state named in the Next field.   
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/92da9b24-8cdd-4aa3-9379-ef8e9847079d)   
- ResultPath
  - A path that determines what input the catcher sends to the state specified in the Next field.
  - for the first catcher in the example, the catcher adds the error output to the input as a field named error-info if there isn't already a field with this name in the input
  - Then, the catcher sends the entire input to RecoveryState. For the second catcher, the error output overwrites the input and the catcher only sendsthe error output to EndState.

- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/6419c89c-d864-441b-955a-91f2b9e9095b)
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/f780f9d5-d97f-4853-a45b-84e21e5f66e0)
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/28cb71ba-1bca-425f-a5cd-343641dca340)

**Service Integration patterns**
- Each of these service integration patterns is controlled by how you create a URI in the ```Resource``` field of your task definition.
- Wait for a Callback with the ```Task Token```
  - Callback tasks provide a way to pause a workflow until a task token is returned.
  - For tasks like these, you can pause Step Functions until the workflow execution reaches the one year service quota, and wait for an external process or workflow to complete.
  - The task will pause until it receives that task token back with a ```SendTaskSuccess``` or ```SendTaskFailure``` call.
  - ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/a5b8c97e-1616-47ed-8425-f72bbe6d3459)
  - ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/f15bf54e-3ce5-4b15-8a28-31eb68c89eee)
  - To avoid stuck executions you can configure a heartbeat timeout interval in your state machine definition.
  - Push mechanism

- ```Activity tasks```
  - Enables you to have the Task work performed by an Activity Worker
  - Pull mechanism
  - ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/76814c50-75c6-4949-9fa6-54f949700832)
  - Activity Worker poll for a Task using GetActivityTask API
  - After Activity Worker completes its work, it sends response of its success/failure using ```SendTaskSuccess``` or ```SendTaskFailure```

## AWS APPSYNC
- AWS AppSync enables developers to connect their applications and services to data and events with secure, serverless and high-performing GraphQL and Pub/Sub APIs. You can do the following with AWS AppSync
- Access data from one or more data sources from a single GraphQL API endpoint.
- Retrieve data in real-time with WebSocket or MQTT on WebSocket
- For mobile apps: local data access & data synchronization
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/8ec2eb8e-3eda-4860-be82-5e83032c19ae) 
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/29682e2c-7117-480e-ac24-88850ba4b300)
- For Security, ```API_KEY```, ```AWS_IAM```, ```OPENID_CONNECT```, ```AMAZON_COGNITO_USER_POOLS```

## AWS AMPLIFY
- AWS Amplify is a set of purpose-built tools and features that enables frontend web and mobile developers to quickly and easily build full-stack applications on AWS. Amplify provides two services:
  - ```Amplify Hosting``` and ```Amplify Studio```
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/d85a5b6b-6bb2-4a85-93d2-03b72a9f57ba)
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/3348964a-24b2-4844-8c4c-0f062364bd56)
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/5a5af532-2b80-498b-bccf-f9db3b4931a7)
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/b651246f-b340-4607-9afa-135ba1cdb0e5)
- • Integrated with Cypress testing framework
• Allows you to generate UI report for your tests  

## AWS DYNAMODB  

- fully managed NoSQL database service that provides fast and predictable performance with seamless scalability
- create database tables that can store and retrieve any amount of data and serve any level of request traffic.
- core components:
  - A table is a collection of items, and each item is a collection of attributes.
  - DynamoDB uses primary keys to uniquely identify each item in a table and secondary indexes to provide more querying flexibility.
  - You can use DynamoDB Streams to capture data modification events in DynamoDB tables.
  ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/8359d9e1-0cfd-4a5b-b284-d9f59a366369)
  - An item is a group of attributes that is uniquely identifiable among all of the other items.
  - An attribute is a fundamental data element, something that does not need to be broken down any further. For example, an item in a People table contains attributes called PersonID, LastName, FirstName, and so on.
  - Each item in the table has a unique identifier, or primary key, that distinguishes the item from all of the others in the table. In the People table, the primary key consists of one attribute (PersonID).
  ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/b6b50bc2-4c9d-49a0-93dd-4545bc78857c)
  - The primary key for Music consists of two attributes (Artist and SongTitle). Each item in the table must have these two attributes. The combination of Artist and SongTitle distinguishes each item in the table from all of the others.
  - Millions of requests per seconds, trillions of row, 100s of TB of storage
 
**Partitioning**
- DynamoDB stores data in partitions. A partition is an allocation of storage for a table, backed by solid state drives (SSDs) and automatically replicated across multiple Availability Zones within an AWS Region.
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/11ba9151-75ce-4db0-9ad3-60000196c146)
- DynamoDB stores and retrieves each item based on its partition key value.
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/3867c985-4e6a-4c41-aa94-2e40013ce30b)

**Primary Key**
- _Partition key_:
  - A simple primary key, composed of one attribute known as the partition key.
  - DynamoDB uses the partition key's value as input to an internal hash function. The output from the hash function determines the partition (physical storage internal to DynamoDB) in which the item will be stored.
  - ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/2b58b130-009d-4e31-9406-2cfdaa143865)
  - The partition key of an item is also known as its hash attribute. 

- _Partition key and sort key_:
  - composite primary key, this type of key is composed of two attributes. The first attribute is the partition key (same as above to determine physical storage area internal), and the second attribute is the sort key.
  - All items with the same partition key value are stored together, in sorted order by sort key value.
  - ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/551a4865-bc4d-4473-a86a-6d9958c82f76)
  - In a table that has a partition key and a sort key, it's possible for multiple items to have the same partition key value. However, those items must have different sort key values.
  - The sort key of an item is also known as its range attribute.
  - ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/39b51d77-966d-4198-827a-62a9293a1533)

  ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/3f698ecd-c484-40ba-8e3c-665e9aca3eab)

**HOW TO Choose Partition key**
- Use high-cardinality attributes. These are attributes that have distinct values for each item, like emailid, employee_no, customerid, sessionid, orderid, and so on.
- Use composite attributes. Try to combine more than one attribute to form a unique key, if that meets your access pattern. For example, consider an orders table with customerid#productid#countrycode as the partition key and order_date as the sort key, where the symbol # is used to split different field.
- a randomizing strategy can greatly improve write throughput. But it’s difficult to read a specific item because you don’t know which suffix value was used when writing the item.
- Isolate frequently accessed items
  - If your application drives disproportionately high traffic to one or more items, adaptive capacity rebalances your partitions such that frequently accessed items don't reside on the same partition. This isolation of frequently accessed items reduces the likelihood of request throttling due to your workload exceeding the throughput quota on a single partition.

**Antipatterns for partition keys**
- Use sequences or unique IDs generated by the DB engine as the partition key, especially when you are migrating from relational databases.
- Using low-cardinality attributes like Product_SKU as the partition key and Order_Date as the sort key greatly increases the likelihood of hot partition issues.
- For example, if one product is more popular, then the reads and writes for that partition key are high resulting in throttling issues.

**How to Choose Sort Keys**
- Careful design of the sort key lets you retrieve commonly needed groups of related items using range queries with operators such as begins_with, between, >, <, and so on.


**Secondary Indexes**
- A secondary index lets you query the data in the table using an alternate key, in addition to queries against the primary key. 
  - _Global secondary index_ – An index with a partition key and sort key that can be different from those on the table. A global secondary index is considered "global" because queries on the index can span all of the data in the base table, across all partitions.
  - Can be added/modified after table creation
  - ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/9f94a1ad-8f25-4bd6-94fc-d69a7b38fc7c)
  - In the Above table, Scenario: Now suppose that you wanted to write a leaderboard application to display top scores for each game. A query that specified the key attributes (UserId and GameTitle) would be very efficient. However, if the application needed to retrieve data from GameScores based on GameTitle only, it would need to use a ```Scan``` operation, making it slow. To speed up queries on non-key attributes, you can create a global secondary index.
  - ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/587f188f-893b-4532-bb9d-1d49df42dc17)
  - you could create a global secondary index named GameTitleIndex, with a partition key of GameTitle and a sort key of TopScore. The base table's primary key attributes are always projected into an index, so the UserId attribute is also present.
  - If the writes are throttled on the GSI, then the main table will be throttled!
  - Attribute projection:   
   ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/ccd4b8f0-2952-47c8-b261-c66140eefc02)
  - Because the non-key attributes Wins and Losses are projected into the index, an application can determine the wins vs. losses ratio for any game, or for any combination of game and user ID.
  - When an application writes an item to a table, DynamoDB automatically copies the correct subset of attributes to any global secondary indexes in which those attributes should appear.
  - AWS account is charged for storage of the item in the base table and also for storage of attributes in any global secondary indexes on that table.
  - ```KEYS_ONLY, INCLUDE, ALL```
  - ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/fee4bae3-5563-4b4a-8d84-7291c42de886)  


  - _Local secondary index_ – An index that has the same partition key as the table, but a different sort key. A local secondary index is "local" in the sense that every partition of a local secondary index is scoped to a base table partition that has the same partition key value.
  - Must be defined at table creation time
  - Each table in DynamoDB has a quota of 20 global secondary indexes (default quota) and 5 local secondary indexes.
  - ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/c8b8037f-c231-4bce-9d40-d0d30a23e21a)
  - given a particular ForumName, a Query operation could immediately locate all of the threads for that forum. Within a group of items with the same partition key value, the items are sorted by sort key value. If the sort key (Subject) is also provided in the query
  - Sceanrio: Which forum threads get the most views and replies, Which thread in a particular forum has the largest number of messages?, How many threads were posted in a particular forum within a particular time period?
  - you can specify one or more local secondary indexes on non-key attributes, such as Replies or LastPostDateTime.
  - ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/58d235f2-be84-4df3-a88d-eead5d24288d)
  - ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/95a84d7c-3802-4ba9-9dab-720532f44665)

**DynamoDB table creation**
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/aebcf53e-60b2-4734-8499-67152c8e316e)   
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/d4107cfa-0a59-484c-9716-55ce667a7f1d)  
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/9d127e22-e161-46a6-82a2-4a0ade999342)  
Composite Primary Key
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/4c2efe51-8278-4e26-9365-4bd764ebfd48)   
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/fb8b7ae3-a21a-4fd6-a85d-f7c46fad1aa6)  
Single Partition/primary key
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/979c7f10-d4b3-452c-b9e8-4640f6392b57)   
Schemaless/flexible schema
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/aec53a1e-6704-429b-93b3-da402240cd07)  
Global Indexes
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/d55d4d7f-a2f0-44bc-ad1a-97e4eaa373d0)   


**Capacity Modes**
- read/write capacity mode controls how you are charged for read and write throughput and how you manage capacity
- Secondary indexes inherit the read/write capacity mode from the base table.

- _On-demand_
  - DynamoDB on-demand offers pay-per-request pricing for read and write requests so that you pay only for what you use.
  - DynamoDB instantly accommodates your workloads as they ramp up or down to any previously reached traffic level. If a workload’s traffic level hits a new peak, DynamoDB adapts rapidly to accommodate the workload.
  - Scenarios: You create new tables with unknown workloads, You have unpredictable application traffic, You prefer the ease of paying for only what you use.
  - Tables can be switched to on-demand mode once every 24 hours. Creating a table as on-demand also starts this 24-hour period. Tables can be returned to provisioned capacity mode at any time. 

- _Provisioned_ (default, free-tier eligible)
 - RCU: Read Capacity Units: throughput for reads
 - WCU: Write Capacity Units: throughput for writes
 - ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/9c4a375e-9238-4415-b593-0bb430fc2b06)
 - ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/d3520875-4918-4c24-b289-1341bf7597da)
 - For example, suppose that you create a provisioned table with 6 read capacity units and 6 write capacity units.
   - Perform strongly consistent reads of up to 24 KB per second
   - Perform eventually consistent reads of up to 48 KB
   - Write up to 6 KB per second
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/2877e02e-2b99-4da9-a41a-516b4312cbc6)
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/334bb8fe-caec-468f-a0a8-0976822d8ec9)
   - When DynamoDB throttles a read or write, it returns a ```ProvisionedThroughputExceededException``` to the caller
   - DynamoDB uses burst capacity to accommodate reads or writes in excess of your table's throughput settings.  
     With burst capacity, unexpected read or write requests can succeed where they otherwise would be throttled  


**Basic Operations**
- CRUD operations
  - ```PutItem```
    - Creates a new item or fully replace an old item (same Primary Key)

  - ```GetItem```
    - Read based on Primary key.
    - Primary Key can be HASH or HASH+RANGE
    - Eventually Consistent Read (default)
    - ```ProjectionExpression``` can be specified to retrieve only certain attributes

  - ```UpdateItem```
    - Edits an existing item’s attributes or adds a new item if it doesn’t exist
    - Can be used to implement Atomic Counters – a numeric attribute that’s unconditionally incremented

  - ```Conditional Writes```
    - Accept a write/update/delete only if conditions are met, otherwise returns an error
    - attribute_exists
• attribute_not_exists
• attribute_type
• contains (for string)
• begins_with (for string)
• ProductCategory IN (:cat1, :cat2) and Price between :low and :high
• size (string length)   

  - ```DeleteItem```
    - Delete an individual item
    - Ability to perform a conditional delete

  - ```DeleteTable```
    - Delete a whole table and all its items

  - ```Query```
    - KeyConditionExpression: Partition Key value (must be = operator) – required, Sort Key value (=, <, <=, >, >=, Between, Begins with) – optional
    - FilterExpression: Additional filtering after the Query operation, Use only with non-key attributes
   
  - ```Scan```
    - Scan the entire table and then filter out data (inefficient)
    - For faster performance, use Parallel Scan

  - ```BatchWriteItem```
    - Up to 25 PutItem and/or DeleteItem in one call
    - Up to 16 MB of data written, up to 400 KB of data per item
    - Can’t update items (use UpdateItem)
    - ```UnprocessedItems``` for failed write operations (exponential backoff or add WCU)

  - ```BatchGetItem```
    - Return items from one or more tables
    - Up to 100 items, up to 16 MB of data
    - Items are retrieved in parallel to minimize latency
    - ```UnprocessedKeys``` for failed read operations (exponential backoff or add RCU) 

- Few Examples:
  - ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/2369be41-71bf-4b26-8a61-408736ad19d0)  
  - ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/005b0e5f-0698-420a-b788-4fb95b259ab4)  
  - ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/a5eb07f6-7851-4ba3-9674-d91cbdbca97f)   
  - ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/e7597d50-9cf7-47aa-94c6-95ba773953dc)  
  - To Prevent Overwrite
    - attribute_not_exists() if single primary key, attribute_not_exists(pk) AND attribute_not_exists(sk) evaluate to true or false before attempting the write operation.
  - string comparison
    ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/fa096c28-acb3-44f0-93a6-7019b3e8f4d3)  
  - check element in a set
    ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/d99c1513-719a-48a0-8348-5d906394ff7e)  
  - Complex condition using logical operators 
    ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/f2e40706-a26d-4aff-af66-f6a9203eb534)   

**PartiQL**
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/a8066aa3-49fd-42ab-ab67-e09b2e49ba35)
- a SQL-compatible query language, to select, insert, update, and delete data in Amazon DynamoDB. Using PartiQL, you can easily interact with DynamoDB tables and run ad hoc queries
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/c82f489e-b7ca-419d-a397-c8af88693cea)

**Optimistic locking**
- Optimistic locking is a strategy to ensure that the client-side item that you are updating (or deleting) is the same as the item in Amazon DynamoDB. If you use this strategy, your database writes are protected from being overwritten by the writes of others
- each item has an attribute that acts as a version number. If you retrieve an item from a table, the application records the version number of that item. You can update the item, but only if the version number on the server side has not changed.
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/da46a68e-b675-4a9c-8a1d-47338995d1c4)

**DAX (DynamoDB Accelerator)**   
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/fa239a53-1267-42ac-b1dc-45fd2bf5e036)
- DynamoDB response times can be measured in single-digit milliseconds. However, there are certain use cases that require response times in microseconds. For these use cases, DynamoDB Accelerator (DAX) delivers fast response times for accessing eventually consistent data.
- For read-heavy or bursty workloads, DAX provides increased throughput and potential operational cost savings by reducing the need to overprovision read capacity units: beneficial for applications that require repeated reads for individual keys.
- DAX supports server-side encryption. With encryption at rest, the data persisted by DAX on disk will be encrypted.
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/c737afe6-d4a0-48f7-9ec2-33d4618d85be)
- When an application sends a GetItem or BatchGetItem request, DAX tries to read the items directly from the item cache using the specified key values. If the items are found (cache hit), DAX returns them to the application immediately. If the items are not found (cache miss), DAX sends the request to DynamoDB. DynamoDB processes the requests using eventually consistent reads and returns the items to DAX. DAX stores them in the item cache and then returns them to the application.
- The item cache has a Time to Live (TTL) setting, which is 5 minutes by default.
- If you specify zero as the item cache TTL setting, items in the item cache will only be refreshed due to an LRU eviction or a "write-through" operation.
- DAX also maintains a query cache to store the results from Query and Scan operations.
- Every DAX cluster provides a cluster endpoint for use by your application. By accessing the cluster using its endpoint, your application does not need to know the hostnames and port numbers of individual nodes in the cluster.
- Ex. ```dax://my-cluster.l6fzcv.dax-clusters.us-east-1.amazonaws.com```
- Amazon DynamoDB Accelerator (DAX) is a write-through/read-through caching service
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/e7a4a504-12a6-437c-88ab-1ad439a8737c)
- If your application needs to write large quantities of data (such as a bulk data load), it might make sense to bypass DAX and write the data directly to DynamoDB. Such a write-around strategy reduces write latency. However, the item cache doesn't remain in sync with the data in DynamoDB.
- This pattern of loading data into the cache only when the item is requested is often referred to as lazy loading. The advantage of this approach is that data that is populated in the cache has been requested and has a higher likelihood of being requested again.
- The disadvantage of lazy loading is the cache miss penalty on the first read of the data, which takes more time to retrieve the data from the table instead of directly from the cache.
- _DAX handles cache evictions in three different ways_:
  - First, it uses a Time-to-Live (TTL) value that denotes the absolute period of time that an item is available in the cache.
  - Second, when the cache is full, a DAX cluster uses a Least Recently Used (LRU) algorithm to decide which items to evict.
  - Third, with the write-through functionality, DAX evicts older values as new values are written through DAX.

**DynamoDB Streams**
- feature that captures data modification events in DynamoDB tables. The data about these events appear in the stream in near-real time, and in the order that the events occurred.
- Each event is represented by a stream record: A new item is added to the table, An item is updated, An item is deleted from the table
- You can use DynamoDB Streams together with AWS Lambda to create a trigger—code that runs automatically whenever an event of interest appears in a stream
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/015352a9-bd8d-4d3d-848f-910f003b1947)
- When to choose DynamoDB streams over Kinesis data streams 
Properties	Kinesis Data Streams for DynamoDB	DynamoDB Streams
Data retention	Up to 1 year.	24 hours.
Kinesis Client Library (KCL) support	Supports KCL versions 1.X and 2.X.	Supports KCL version 1.X.
Number of consumers	Up to 5 simultaneous consumers per shard, or up to 20 simultaneous consumers per shard with enhanced fan-out.	Up to 2 simultaneous consumers per shard.
Throughput quotas	Unlimited.	Subject to throughput quotas by DynamoDB table and AWS Region.
Record delivery model	Pull model over HTTP using GetRecords and with enhanced fan-out, Kinesis Data Streams pushes the records over HTTP/2 by using SubscribeToShard.	Pull model over HTTP using GetRecords.
Ordering of records	The timestamp attribute on each stream record can be used to identify the actual order in which changes occurred in the DynamoDB table.	For each item that is modified in a DynamoDB table, the stream records appear in the same sequence as the actual modifications to the item.
Duplicate records	Duplicate records might occasionally appear in the stream.	No duplicate records appear in the stream.
Stream processing options	Process stream records using AWS Lambda, Kinesis Data Analytics, Kinesis data firehose , or AWS Glue streaming ETL.	Process stream records using AWS Lambda or DynamoDB Streams Kinesis adapter.
Durability level	Availability zones to provide automatic failover without interruption.	Availability zones to provide automatic failover without interruption.
- Specifies the information that will be written to the stream whenever data in the table is modified:
  - KEYS_ONLY — Only the key attributes of the modified item.
  - NEW_IMAGE — The entire item, as it appears after it was modified.
  - OLD_IMAGE — The entire item, as it appeared before it was modified.
  - NEW_AND_OLD_IMAGES — Both the new and the old images of the item.
- To read and process a stream, your application must connect to a DynamoDB Streams endpoint and issue API requests.
- Stream records are organized into groups, or shards. Each shard acts as a container for multiple stream records, and contains information required for accessing and iterating through these records. The stream records within a shard are removed automatically after 24 hours.
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/c13f3fd0-cd76-4e28-b5b3-cbda9d7604cb)
- Combining DynamoDB Time to Live (TTL), DynamoDB Streams, and AWS Lambda can help simplify archiving data, reduce DynamoDB storage costs, and reduce code complexity. Using Lambda as the stream consumer provides many advantages, most notably the cost reduction compared to other consumers such as Kinesis Client Library (KCL). You aren’t charged for GetRecords API calls on your DynamoDB stream when using Lambda to consume events, and Lambda can provide event filtering by identifying JSON patterns in a stream event.
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/8766b713-02d8-4719-871b-3124346bbcbb)
- The AWS Lambda service polls the stream for new records four times per second. When new stream records are available, your Lambda function is synchronously invoked
- Records are not retroactively populated in a stream after enabling it
- Adapter design pattern for kinesis with DYNAMODB
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/c947f74a-80cf-4e23-9e2b-82ca0f432dda)
- Integration Architechture
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/3e6ed2ac-b24d-473c-a730-ea70fa7094b7)  



**DynamoDB TTL (TIME TO LIVE)**
- Time to Live (TTL) allows you to define a per-item timestamp to determine when an item is no longer needed.
- Doesn’t consume any WCUs (i.e., no extra cost) EXCEPT when the deletion is replicated to additional Regions
- TTL is useful if you store items that lose relevance after a specific time.
- you must identify a specific attribute name that the service will look for when determining if an item is eligible for expiration. After you enable TTL on a table, a per-partition scanner background process automatically and continuously evaluates the expiry status of items in the table.
- A second background process scans for expired items and deletes them. Both processes take place automatically in the background, do not affect read or write traffic to the table, and do not have a monetary cost.
- Items are removed from any local secondary index and global secondary index in the same way as a DeleteItem operation. This operation comes at no extra cost.
- A delete operation for each item enters the DynamoDB Stream, but is tagged as a system delete and not a regular delete
- Items that have expired, but haven’t yet been deleted by TTL, still appear in reads, queries, and scans. If you do not want expired items in the result set, you must filter them out (CLIENT-SIDE)
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/e01a688f-5424-4b4e-9cae-8b008a8e32f8)
- The TTL mechanism will work on items that have been inserted after the TTL has been enabled on the table
- DynamoDB is removing items with expired TTL in up to 48 hours from the original expiration time
- Archiving TTL deletes to S3 is a common use-case to offload cold data, reduce table storage and maintain most current data in the table.

**DynamoDB transactions**
- transactions simplify the developer experience of making coordinated, all-or-nothing changes to multiple items both within and across tables.
- Transactions provide atomicity, consistency, isolation, and durability (ACID) in DynamoDB, helping you to maintain data correctness in your applications.
- DynamoDB performs two underlying reads or writes of every item in the transaction: one to prepare the transaction and one to commit the transaction.
- ```TransactWriteItems```
  - is a synchronous and idempotent write operation that groups up to 100 write actions in a single all-or-nothing operation. These actions can target up to 100 distinct items in one or more DynamoDB tables
  - You can optionally include a client token when you make a TransactWriteItems call to ensure that the request is idempotent.
- ```TransactGetItems```
  - is a synchronous read operation that groups up to 100 Get actions together. These actions can target up to 100 distinct items in one or more DynamoDB tables
  - actions are performed atomically so that either all of them succeed or all of them fail:
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/e0e49e66-7da3-4bc3-8243-f07e501fee53)
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/485d3f13-aaea-42fa-a52b-0fc25d1b9855)  



**DynamoDB CLI examples**
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/7b9d0d48-01d2-41f0-9c86-ef24e9226e5d)  

**Dynamo DB as session state**
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/82dad4a7-e360-44c7-a1db-4544a17dde27)   

**DynamoDB with S3 integration**
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/e0477379-cc45-4afe-a2d3-9a1cca7a918b)   

**DynamoDB security**
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/2048c6d4-ce09-436f-89b1-bba415c593b3)
- In addition to controlling access to DynamoDB API actions, you can also control access to individual data items and attributes
- To implement this kind of fine-grained access control, you write an IAM permissions policy that specifies conditions for accessing security credentials and the associated permissions. You then apply the policy to users, groups, or roles that you create using the IAM console. Your IAM policy can restrict access to individual items in a table, access to the attributes in those items, or both at the same time.
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/8fc6d547-91c8-4bf9-b027-541eb52b8f35)   

## AWS S3 

- Amazon S3 allows people to store objects (files) in “buckets” (directories)
- Buckets must have a globally unique name (across all regions all accounts)
- Buckets are defined at the region level
- The key is the FULL path:
• ```s3://my-bucket/my_file.txt```
• ```s3://my-bucket/my_folder1/another_folder/my_file.txt```
• The key is composed of prefix + object name
• ```s3://my-bucket/my_folder1/another_folder/my_file.txt```
- Max. Object Size is 5TB (5000GB), If uploading more than 5GB, must use “multi-part upload”
- _Buckets_
  - A bucket is a container for objects stored in Amazon S3. You can store any number of objects in a bucket and can have up to 100 buckets in your account.
- _Objects_
  - Objects are the fundamental entities stored in Amazon S3.
  - The metadata is a set of name-value pairs that describe the object. These pairs include some default metadata, such as the date last modified, and standard HTTP metadata, such as Content-Type. You can also specify custom metadata at the time that the object is stored.
  - An object is uniquely identified within a bucket by a key (name) and a version ID (if S3 Versioning is enabled on the bucket)
  - For example, in the URL https://DOC-EXAMPLE-BUCKET.s3.us-west-2.amazonaws.com/photos/puppy.jpg, DOC-EXAMPLE-BUCKET is the name of the bucket and photos/puppy.jpg is the key.

**Security: Bucket policies**
- you can secure access to objects in your buckets, so that only users with the appropriate permissions can access them
- How Authorizor works:
  - Converts all the relevant access policies (user policy, bucket policy, ACLs) at run time into a set of policies for evaluation.
  - Amazon S3 evaluates a subset of policies in a specific context, based on the context authority: ```User context, Bucket context, Object context```
    
- Ex. JSON policies 
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/a5b93ecf-05df-4421-9c1b-cd82cf6d34da)   

- User-Based:
  - IAM Policies – which API calls should be allowed for a specific user from IAM
  - Ex.
  - Allowing an IAM user access to one of your buckets
  ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/59ce7c4a-fae3-41fe-9592-55bb571220f0)
  - Allowing each IAM user access to a folder in a bucket
  ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/85a95ae7-1d70-47b6-9d48-527b1179d0ae)
  ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/61af6e0a-f53a-45f7-823c-2ea9b5fb4b1a)
  - Restricting access to Amazon S3 buckets within a specific AWS account
  ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/c25c51bb-52f4-4cb2-9b76-b34e44890303)   

  - EX. OF AWS MANAGED POLICIES: ```AmazonS3FullAccess```, ```AmazonS3ReadOnlyAccess```, ```AmazonS3ObjectLambdaExecutionRolePolicy```


- Resource-Based
  - Bucket Policies – bucket wide rules from the S3 console - allows cross account
  - The policy allows Dave, a user in account Account-ID, s3:GetObject, s3:GetBucketLocation, and s3:ListBucket Amazon S3 permissions on the awsexamplebucket1 bucket.
  - ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/6c52e3ea-9d48-420c-b3b8-9af30b485a94)   

  - Resources
  - Ex. ```arn:partition:service:region:namespace:relative-id```
  - Principals
    - "AWS":"account-ARN"
  - Actions
    - Object operations
  ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/31275f8b-9626-47e1-91ed-919149d68567)  
    - Bucket operations
  ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/062523f1-a2df-4c7b-b764-0b44d6cd5923)
    - Explicit deny
  ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/068eb91d-06e8-4da8-a50d-cc2bf909d3aa)
    - Account operations
  ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/80d51b26-afdb-403a-95fd-1415ddcdf28e)  
    - Condition keys
  ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/6efcd248-0370-4fac-992e-ea4dd9a84f75)   
    - Objects upload requiring SSE (SERVER SIDE ENCRYPTION)
  ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/ab3d5ed0-e6d2-4f28-bcd3-9c87fc52769b)
    - Granting access to specific version of object
  ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/d6ab7cc9-8689-4ada-a91b-7be37b6ad8f0)
    - Allow access on the basis of tags
  ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/7204b9e4-53ed-430a-96a2-c1fa9f77cbbf)   

  - Object Access Control List (ACL) – finer grain (can be disabled)
  ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/e1275f71-2c0b-410e-a4e6-6421529454e7)
  - ACLs enabled
    - Bucket owner preferred – The bucket owner owns and has full control over new objects that other accounts write to the bucket with the bucket-owner-full-control canned ACL.
    - Object writer – The AWS account that uploads an object owns the object, has full control over it, and can grant other users access to it through ACLs.
    ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/0734c0e6-6ce2-4870-bdd3-cff696a3190c)

  - Bucket Access Control List (ACL) – less common (can be disabled)   
  ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/7793078d-a237-463d-bd45-754a15cf725f)
  - ACL permissions are mapped to policy permissions for buckets and objects
   ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/83abd187-f690-4139-9455-c84eb72f9ba5)    
  - Supports canned ACL's: predefined set of grantees and permissions. Ex. ```private```, ```public-read```, ```public-read-write```, ```bucket-owner-read``` etc...

**S3 BLOCK PUBLIC ACCESS**
- ```BlockPublicAcls```: PUT Bucket acl and PUT Object acl calls fail if the specified access control list (ACL) is public.
- ```IgnorePublicAcls```: Setting this option to TRUE causes Amazon S3 to ignore all public ACLs on a bucket and any objects that it contains. This setting enables you to safely block public access granted by ACLs while still allowing PUT Object calls that include a public ACL
- ```BlockPublicPolicy```: Setting this option to TRUE for a bucket causes Amazon S3 to reject calls to PUT Bucket policy if the specified bucket policy allows public access.
- ```RestrictPublicBuckets```: Setting this option to TRUE restricts access to an access point or bucket with a public policy to only AWS service principals and authorized users within the bucket owner's account and access point owner's account.

**Static website hosting**
- S3 can host static websites and have them accessible on the Internet
- the website is available at the AWS Region-specific website endpoint of the bucket: ```http://bucket-name.s3-website-Region.amazonaws.com``` or ```http://bucket-name.s3-website.Region.amazonaws.com``` (returns the default index.html/configured)
- need public read access permissions
- if not want to grant public read permissions and still host the website, Amazon CloudFront distribution to serve your static website.

**S3 versioning**
- means of keeping multiple variants of an object in the same bucket
- When you enable versioning in a bucket, all new objects are versioned and given a unique version ID.
- Objects that are stored in your bucket before you set the versioning state have a version ID of null
- If you delete an object, instead of removing the object permanently, Amazon S3 inserts a delete marker, which becomes the current object version.
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/9224fc9c-b924-4080-9c26-f275f400aa75)  
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/dbdf6ef9-9e13-49ed-aa41-8045e5ab3030)
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/ef4d74bf-54f5-414d-a044-b27e86631ccf)
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/10381e85-1539-449e-8200-ff064e26ae0d)
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/7fdc8acf-dfc1-4042-8ad6-6e2534c494e9)

**S3 REPLICATION**
- automatic, asynchronous copying of objects across Amazon S3 buckets.
- You can replicate objects to a single destination bucket or to multiple destination buckets.
- To automatically replicate new objects as they are written to the bucket, use live replication, such as Cross-Region Replication (CRR). To replicate existing objects to a different bucket on demand, use ```S3 Batch Replication```.
- _Pre-requisites_:
  - Both source and destination buckets must have versioning enabled
  - permissions to replicate objects from the source bucket to the destination bucket or buckets on your behalf.
- Cross-Region Replication (CRR)
- Same-Region Replication (SRR)
- For DELETE operations   
• Can replicate delete markers from source to target (optional setting)   
• Deletions with a version ID are not replicated (to avoid malicious deletes)
- There is no “chaining” of replication   
• If bucket 1 has replication into bucket 2, which has replication into bucket 3  
• Then objects created in bucket 1 are not replicated to bucket 3  

**S3 Storage classes, Tiers and Lifecycle management**

- High durability (99.999999999%, 11 9’s) of objects across multiple AZ
• If you store 10,000,000 objects with Amazon S3, you can on average expect to
incur a loss of a single object once every 10,000 years
- Availibility: • Example: S3 standard has 99.99% availability = not available 53 minutes a year

- _Storage classes for frequently accessed objects_
  - **S3 Standard** – The default storage class. If you don't specify the storage class when you upload an object, Amazon S3 assigns the S3 Standard storage class.
- _Storage classes for infrequently accessed objects_
  - **S3 Standard-IA** - Amazon S3 stores the object data redundantly across multiple geographically separated Availability Zones (minimum storage duration period of 30 days)
  - **S3 One Zone-IA** - Amazon S3 stores the object data in only one Availability Zone, which makes it less expensive than S3 Standard-IA (minimum storage duration period of 30 days)
- _Storage classes for archiving objects_
  - **S3 Glacier Instant Retrieval** - Use for archiving data that is rarely accessed and requires milliseconds retrieval.
  - **S3 Glacier Flexible Retrieval** - Use for archives where portions of the data might need to be retrieved in minutes. (1-5 minutes), minimum storage duration period of 90 days
  - **S3 Glacier Deep Archive** - Use for archiving data that rarely needs to be accessed. has a minimum storage duration period of 180 days and a default retrieval time of 12 hours.
- _S3 Intelligent-Tiering automatically optimizing data with changing or unknown access patterns_
  - Frequent Access (automatic), Infrequent Access (automatic, object is not accessed for 30 consecutive days), Archive Instant Access (automatic, object is not accessed for 90 consecutive days), Archive Access (optional, 90 - 730 days ), Deep Archive Access (optional, 180-730 days)

- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/5c55acc9-6c1b-469c-ae60-ab5b197ee173)
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/09c2d060-cd95-40ec-8e9d-287d8a184581)
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/f4737bb2-0f6f-45ef-8db2-35d8b6f458ec)
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/5b9d9078-6211-4ade-92d7-7134e90ab4e4)  

- Retrieval options for archived data
  - Expedited: available within 1–5 minutes, Intelligent-Tiering Archive Access tier
  - Standard:  3–5 hours for objects, Glacier Flexible Retrieval storage class or S3 Intelligent-Tiering Archive Access tier
  - Bulk: finish within 5–12 hours for objects that are stored in the S3 Glacier Flexible Retrieval storage class or S3 Intelligent-Tiering Archive Access tier. typically finish within 48 hours for objects stored in the S3 Glacier Deep Archive storage class or S3 Intelligent-Tiering Deep Archive Access tier.  

- S3 lifecycle actions
  - An S3 Lifecycle configuration is an XML file that consists of a set of rules with predefined actions that you want Amazon S3 to perform on objects during their lifetime.
  - Amazon S3 supports a waterfall model for transitioning between storage classes
    ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/b91d80eb-3904-4792-b6a0-58a12f642bfb)   

  - _Transition actions_:
    - These actions define when objects transition to another storage class. 
  - _Expiration actions_:
    - These actions define when objects expire. Amazon S3 deletes expired objects on your behalf.
  - ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/f82049fc-3029-40b9-aa1a-9d2e95a2a1bc)
  - ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/b63a55b0-8f60-4ee9-92a9-fa6057b86bad)   

- Amazon S3 Analytics – Storage Class Analysis: Help you decide when to transition objects to the right storage class

- S3 EVENT NOTIFICATIONS
  - receive notifications when certain events happen in your S3 bucket.
  - SQS, SNS, LAMBDA (NEEDS IAM PERMISSIONS ATTACHED TO S3 BUCKETS)
  - ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/23088ffe-f7e9-4851-9cf9-c500e262fea2)
  - EVENTBRIDGE (Amazon S3 does not require any additional permissions to deliver events to Amazon EventBridge)
  - ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/cb49e3ff-5281-4560-9f1e-8b460bdfefa0)  

**S3 PERFORMANCE OPTIMIZATION**
- Your application can achieve at least 3,500 PUT/COPY/POST/DELETE or 5,500 GET/HEAD requests per second per prefix in a bucket.
- ```Multi-Part upload```: recommended for files > 100MB, must use for files > 5GB
- ```S3 Transfer Acceleration```: Increase transfer speed by transferring file to an AWS edge location which will forward the data to the S3 bucket in the target region
- ```Byte-Range Fetches```: Parallelize GETs by requesting specific byte ranges  
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/765d8ef5-c2a9-458a-8855-6821a0b298d7)   
- ```S3 SELECT```: you can use structured query language (SQL) statements to filter the contents of an Amazon S3 object and retrieve only the subset of data that you need, works on objects stored in CSV, JSON, or Apache Parquet format. works with Glacier as well, so Glacier SELECT.
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/e6865eaf-ee86-4fac-9aa1-ecf430b2a059)  

**Metadata and tags**
- S3 User-Defined Object Metadata: Name-value (key-value) pairs, User-defined metadata names must begin with "x-amz-meta-”
- S3 Object Tags: Useful for fine-grained permissions (only access specific objects with specific tags), can be used in s3 analytics
  - In bucket lifecycle configuration, you can specify a filter to select a subset of objects to which the rule applies. You can specify a filter based on the key name prefixes, object tags, or both.
- You cannot search the object metadata or object tags. Instead, you must use an external DB as a search index such as DynamoDB

**S3 ENCRYPTION**

- SSE (SERVER SIDE ENCRYPTION)
  - _SSE-S3_
    - Encryption type is AES-256
    - Must set header "x-amz-server-side-encryption": "AES256"
    - automatically applied to new objects stored in S3 bucket
    - Bucket policy to force to require encryption 
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/4975b2ca-3135-47b4-b11d-c3479d51a35a)  

  - _SSE-KMS_
    - Must set header "x-amz-server-side-encryption": "aws:kms"
    - Encryption using keys handled and managed by AWS KMS (Key Management Service)
    - When you upload, it calls the GenerateDataKey KMS API
    - When you download, it calls the Decrypt KMS API
    - you can configure your buckets to use S3 Bucket Keys for SSE-KMS. Using a bucket-level key for SSE-KMS can reduce your AWS KMS request costs by up to 99 percent by decreasing the request traffic from Amazon S3 to AWS KMS.
    - AWS generates a short-lived bucket-level key from AWS KMS then temporarily keeps it in S3. This bucket-level key will create data keys for new objects during its lifecycle. S3 Bucket Keys are used for a limited time period within Amazon S3, reducing the need for S3 to make requests to AWS KMS to complete encryption operations
    ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/03c5ac80-6845-4540-8857-60c8df94a7b8)  

  - _SSE-C_
    - keys fully managed by the customer outside of AWS
    - HTTPS must be used
    - Encryption key must provided in HTTP headers, for every HTTP request made

- CSE (CLIENT SIDE ENCRYPTION)
  - Use client libraries such as Amazon S3 Client-Side Encryption Library
  ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/eabad170-d546-4c70-97d6-fe198d8113eb)

**S3 CORS**
- The request's ```Origin``` header must match an ```AllowedOrigin``` element.
- The request method (for example, GET or PUT) or the ```Access-Control-Request-Method``` header in case of a preflight ```OPTIONS``` request must be one of the AllowedMethod elements.
- Every header listed in the request's ```Access-Control-Request-Headers``` header on the preflight request must match an ```AllowedHeader``` element.
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/5d63c8d8-c90a-49c9-8e91-e21dcbede369)  
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/0edf810a-681d-4ac2-8e51-09607fd90cb9)

**S3 MFA DELETE**
- MFA (Multi-Factor Authentication) – force users to generate a code on a device (usually a mobile phone or hardware) before doing important operations on S3
- Permanently delete an object version, Suspend Versioning on the bucket
- To use MFA Delete, Versioning must be enabled on the bucket
- Only the bucket owner (root account) can enable/disable MFA Delete

**S3 PRE-SIGNED URL'S**
- You can use presigned URLs to grant time-limited access to objects in Amazon S3 without updating your bucket policy.
- The credentials used by the presigned URL are those of the AWS user who generated the URL.
- You can also use presigned URLs to allow someone to upload a specific object to your Amazon S3 bucket. This allows an upload without requiring another party to have AWS security credentials or permissions.
- A presigned URL remains valid for the period of time specified when the URL is generated. If you create a presigned URL with the Amazon S3 console, the expiration time can be set between 1 minute and 12 hours. If you use the AWS CLI or AWS SDKs, the expiration time can be set as high as 7 days.
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/f0590d92-55de-45e3-8d0d-a194655d4c34)   

**S3 ACCESS POINTS**
- Access points are named network endpoints that are attached to buckets that you can use to perform S3 object operations, such as GetObject and PutObject.
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/0d2b5f13-a3c7-4211-969f-4d9f501648cb)
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/e2c69ec7-7b9b-43ba-9e16-39ab9efc2d31)
- You can delegate access control for a bucket to the bucket's access points.
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/a0021cea-46d2-4a16-9002-3e75c996ff44)  

**S3 OBJECT LAMBDA**
- Use AWS Lambda Functions to change the object before it is retrieved by the caller application
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/0e017563-a6a2-4c91-ad1d-087139baf2df)   

## API GATEWAY

- AWS service for creating, publishing, maintaining, monitoring, and securing REST, HTTP, and WebSocket APIs at any scale
- Create a single interface for all the microservices in your company
  ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/e359759c-8877-472b-b37e-9b60ab62befd)  

- _API Gateway creates RESTful APIs that_:
  - Are HTTP-based.
  - Enable stateless client-server communication.
  - Implement standard HTTP methods such as GET, POST, PUT, PATCH, and DELETE.
  - For example, /incomes could be the path of a resource representing the income of the app user.
  - In API Gateway REST APIs, the frontend is encapsulated by method requests and method responses. The API interfaces with the backend by means of integration requests and integration responses.
  - API Gateway enables you to define a schema or model for the payload  to facilitate setting up the body mapping template.
- _API Gateway to create HTTP APIs_
  - HTTP APIs to send requests to AWS Lambda functions or to any publicly routable HTTP endpoint.
  - you can create an HTTP API that integrates with a Lambda function on the backend. When a client calls your API, API Gateway sends the request to the Lambda function and returns the function's response to the client.
  - HTTP APIs support OpenID Connect and OAuth 2.0 authorization
- _API Gateway creates WebSocket APIs that_:
  - Adhere to the WebSocket protocol, which enables stateful, full-duplex communication between client and server.
  - Route incoming messages based on message content.
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/8d550704-7b56-47a6-995f-23fa93e473ad)
- Together with AWS Lambda, API Gateway forms the app-facing part of the AWS serverless infrastructure.
- Backend servers can easily push data to connected users and devices, avoiding the need to implement complex polling mechanisms. Ex. Chat applications, Real-time dashboards such as stock tickers, Real-time alerts and notifications.
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/defa9687-b866-4373-ade7-f0ed316300ef)
- Client to server connection
  ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/afb08447-5293-4870-af00-9fe17719757e)  
- Server to client connection  
  ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/9c5b23c4-a28f-4dbf-97b2-102c082ab43d)
- Routing for websocket API's
  - • Incoming JSON messages are routed to different backend
• If no routes => sent to $default
• You request a route selection expression to
select the field on JSON to route from
• Sample expression: $request.body.action
• The result is evaluated against the route keys
available in your API Gateway
• The route is then connected to the backend
you’ve setup through API Gateway


- Ex. Integration with Kinesis data streams
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/36d94087-b5b6-4503-a375-97ddf176425d)   

**Endpoint types**
- _Edge-optimized API endpoints_
  - An edge-optimized API endpoint is best for geographically distributed clients. API requests are routed to the nearest CloudFront Point of Presence (POP). This is the default endpoint type for API Gateway REST APIs.
- _Regional API endpoints_
  - A regional API endpoint is intended for clients in the same region. When a client running on an EC2 instance calls an API in the same region, or when an API is intended to serve a small number of clients with high demands, a regional API reduces connection overhead.
- _Private API endpoints_
  - A private API endpoint is an API endpoint that can only be accessed from your Amazon Virtual Private Cloud (VPC) using an interface VPC endpoint, which is an endpoint network interface (ENI) that you create in your VPC.

**Creating REST API**
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/7750566f-6ecc-4c4d-867b-e75bc27197d4) 
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/0a776896-610a-43d8-aad9-a916c8415eff)   
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/fa528630-b721-4e7b-a5b1-7353645de237)   
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/9993665f-f3ab-426f-b834-38e0083459be)  
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/b38776a7-70bc-4da1-abc8-76596c6eb1f4)  
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/58fe801e-a973-422c-8057-a400a2091f44)   
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/c4a9ed57-66c4-4c06-bdee-f4e73ef9d2d1)    
![tempsnip](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/8f9907b7-3328-4267-8068-0cafece8603f) 

**Deploying REST API**
- After creating your API, you must deploy it to make it callable by your users.
- To deploy an API, you create an API deployment and associate it with a stage. A stage is a logical reference to a lifecycle state of your API (for example, dev, prod, beta, v2).
- Ex. ```https://{restapi-id}.execute-api.{region}.amazonaws.com/{stageName}```
- Stage variables are name-value pairs that you can define as configuration attributes associated with a deployment stage of a REST API. They act like environment variables and can be used in your API setup and mapping templates.
- To use a stage variable to customize the HTTP integration endpoint, you must first configure a stage variable of a specified name (for example, url), and then assign it a value, (for example, example.com). Next, from your method configuration, set up an HTTP proxy integration. Instead of entering the endpoint's URL, you can tell API Gateway to use the stage variable value, ```http://${stageVariables.url}```. This value tells API Gateway to substitute your stage variable ```${}``` at runtime, depending on which stage your API is running.
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/12714061-4220-4f4e-a20f-edd2a9e29f44)
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/8856728f-7d71-463c-9a56-70c8941b8a52)
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/0de59743-34fe-4939-9865-2e3234a6d20c)
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/b2683acf-a6fc-4233-9af3-ecf8710fbf2b)
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/6d3452fc-a5b7-4f92-a69f-244f0bedfab1)
- Ex. ```stageVariables.<variable_name>, { "name" : "$stageVariables.<variable_name>"}, http://${stageVariables.<variable_name>}, arn:aws:apigateway:<region>:<service>:${stageVariables.<variable_name>}```

**Canary release deployment**
- software development strategy in which a new version of an API (as well as other software) is deployed for testing purposes, and the base version remains deployed as a production release for normal operations on the same stage.
- total API traffic is separated at random into a production release and a canary release with a pre-configured ratio. Typically, the canary release receives a small percentage of API traffic and the production release takes up the rest. The updated API features are only visible to API traffic through the canary. You can adjust the canary traffic percentage to optimize test coverage or performance.
- After the test metrics pass your requirements, you can promote the canary release to the production release and disable the canary from the deployment.
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/00ad6f0a-8200-4723-b007-eb5e9f23b5c9)
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/e365e981-4fb2-444a-9d88-e1c896ecc6db)

**Integration type**
- _AWS/HTTP_
  - you must configure both the integration request and integration response and set up necessary data mappings from the method request to the integration request, and from the integration response to the method response.
  - Setup data mapping using mapping templates for the request & response
  - ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/a085b448-a8d8-4054-8ad8-6de0f3ad9c02)   

- _AWS_PROXY_
  - This type of integration lets an API method be integrated with the Lambda function invocation action
  - you do not set the integration request or the integration response.
  - API Gateway passes the incoming request from the client as the input to the backend Lambda function.
  - This is the preferred integration type to call a Lambda function through API Gateway
  - ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/9502f581-8f04-4997-864e-65ae60b55c61)   

- _HTTP_PROXY_
  - The HTTP proxy integration allows a client to access the backend HTTP endpoints with a streamlined integration setup on single API method.
  - You do not set the integration request or the integration response.
  - Possibility to add HTTP Headers if need be (ex: API key)
  - ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/bc93f751-8ec3-4e6e-9d20-75ec91117f9a)    

- _MOCK_
  - return a response without sending the request further to the backend. This is useful for API testing because it can be used to test the integration set up without incurring charges for using the backend and to enable collaborative development of an API.

**Integration Request**

- An integration request is an HTTP request that API Gateway submits to the backend, passing along the client-submitted request data, and transforming the data, if necessary.
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/bd1b3f0f-0f3e-4786-b7c1-b1300542cda5)
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/e442d033-3786-455f-84ef-1b9417bbcd63)  

**Integration Response**

- You can choose to pass through the result as-is or to transform the integration response data to the method response data if the two have different formats.
- you can map the endpoint response data to the method response data. The response data that can be mapped includes the response status code, response header parameters, and response body.
- If no method response is defined for the returned status code, API Gateway returns a 500 error.
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/5468ec48-7828-4f9c-85f1-a4ca4ae704fd)
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/242d599b-c776-4d31-8738-cd468dbd838d)
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/3f83320c-9e39-4e48-a4b8-5e63a6181f28)

**Mapping templates**

- Mapping template examples integration  
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/97a04b68-7471-4aaa-ac3f-59850be3e229)
- A mapping template is a script expressed in ```Velocity Template Language (VTL)``` and applied to the payload using JSONPath .
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/a72b4bed-bee3-4408-a83d-a517d1ac7f57)
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/b68a0493-84ed-4b5f-91c1-fb9d9b27c506)
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/aeb2ee6e-e5a8-472d-a381-9544dd3bdadf)   

**Request Validation via OpenAPI spec**

- You can use API Gateway to import a REST API from an external definition file into API Gateway. Currently, API Gateway supports OpenAPI v2.0 and OpenAPI v3.0 definition files
- configure API Gateway to perform basic validation of an API request before proceeding with the integration request. When the validation fails, API Gateway immediately fails the request, returns a 400 error response to the caller, and publishes the validation results in CloudWatch Logs.
- The required request parameters in the URI, query string, and headers of an incoming request are included and not blank.
- The applicable request payload adheres to the configured JSON schema request of the method.
- In API Gateway, a model defines the data structure of a payload. In API Gateway, models are defined using the JSON schema draft 4. The following JSON object is sample data in the Pet Store example.
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/d5793e77-aafb-46cf-abe4-356e36e31a2b)
- There are two request validators declared in the ```x-amazon-apigateway-request-validators``` map at the API level.
- The ```params-only``` validator is enabled on the API and inherited by the GET method.
- This validator allows API Gateway to verify that the required query parameter (q1) is included and not blank in the incoming request.
- The ```all``` validator is enabled on the POST method.
- This validator verifies that the required header parameter (h1) is set and not blank. It also verifies that the payload format adheres to the specified ```RequestBodyModel``` If there is no matching content type is found, request validation is not performed.
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/2f56e2e6-d3ee-430b-a25d-cafd032f604d)  

**API Caching**

- With caching, you can reduce the number of calls made to your endpoint and also improve the latency of requests to your API.
- API Gateway caches responses from your endpoint for a specified time-to-live (TTL) period, in seconds. Ex. 300 seconds
- This is a HIPAA Eligible Service. For more information about AWS, U.S. Health Insurance Portability and Accountability Act of 1996 (HIPAA), and using AWS services to process, store, and transmit protected health information (PHI)
- Clients can invalidate the cache with header: Cache- Control: max-age=0

**API KEYS and Usage plans**

- alphanumeric string values to distribute to your customers
- Can use with usage plans to control access
- Throttling limits are applied to the API keys
- Quotas limits is the overall number of maximum requests
- Associate API stages and API keys with the usage plan.
- Callers of the API must supply an assigned API key in the x-api-key header in requests to the API
- If there is a match, API Gateway throttles the requests based on the plan's request limit and quota
- A throttling limit sets the target point at which request throttling should start. This can be set at the API or API method level.
- A quota limit sets the target maximum number of requests with a given API key that can be submitted within a specified time interval

**API gateway throttling**
- AWS throttling limits are applied across all accounts and clients in a region. These limit settings exist to prevent your API—and your account—from being overwhelmed by too many requests. These limits are set by AWS and can't be changed by a customer.
- Per-account limits are applied to all APIs in an account in a specified Region. The default rate limit is 10.000 requests per second, and the default burst limit is 5000 requests.
- Per-API, per-stage throttling limits are applied at the API method level for a stage.
- Per-client throttling limits are applied to clients that use API keys associated with your usage plan as client identifier
- In API Gateway, the burst limit represents the target maximum number of concurrent request submissions that API Gateway will fulfill before returning 429 Too Many Requests error responses.

**CORS**
- A cross-origin HTTP request is one that is made to:
  - A different domain (for example, from example.com to amazondomains.com)
  - A different subdomain (for example, from example.com to petstore.example.com)
  - A different port (for example, from example.com to example.com:10777)
  - A different protocol (for example, from https://example.com to http://example.com)
- The ```OPTIONS``` pre-flight request must contain the following headers:
  - ```Access-Control-Allow-Methods```
  - ```Access-Control-Allow-Headers```
  - ```Access-Control-Allow-Origin```
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/1de2c266-1d2d-4cf0-86f1-e6f739d3ab72)   
- For the proxy: lambda should return response headers itself in the response
- For the non-proxy: it can be configured from the console.

**Security (IAM PERMISSIONS)**
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/2e5d4238-9883-4c74-9fb1-36e0a7258063)
- With IAM identity-based policies, you can specify which actions and resources are allowed or denied as well as the conditions under which actions are allowed or denied.
- The following example shows an identity-based policy that allows a user to create or update only private REST APIs.
 ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/7c33f369-4cbd-4269-a33f-c6642a803c35)
- Authentication = IAM | Authorization = IAM Policy
- Resource based policies
  - Ex. resource policy grants API access in one AWS account to two roles in a different AWS account via Signature Version 4 (SigV4) protocols
    ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/27a75c12-7adb-4dd5-835e-0461f94dd9c2)
  - Ex. resource policy denies (blocks) incoming traffic to an API from two specified source IP address blocks.
    ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/77457e82-9cde-439d-b254-52276a5dc218)
  - Ex. resource policies allow incoming traffic to a private API only from a specified virtual private cloud (VPC) or VPC endpoint.
    ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/7a9dd666-7b53-4aa6-bcb9-6d6ed4fc39b4)
- Service-linked roles: ```AWSServiceRoleForAPIGateway``` – Allows API Gateway to access Elastic Load Balancing, Amazon Kinesis Data Firehose, and other service resources on your behalf.


**Security (Cognito User pools)**
- Cognito fully manages user lifecycle, token expires automatically
- API gateway verifies identity automatically from AWS Cognito
- No custom implementation required
- Authentication = Cognito User Pools | Authorization = API Gateway Methods
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/e21b6804-f852-4dc7-a4c0-209e49a8d691)  


**Security (LAMBDA AUTHORIZER)**
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/067ac85e-7b48-4250-bcba-e903cc058497)
- Authentication = External | Authorization = Lambda function
- Token-based authorizer (bearer token) – ex JWT (JSON Web Token) or Oauth
- A request parameter-based Lambda authorizer (headers, query string, stage var)
- Lambda must return an IAM policy for the user, result policy is cached
- V1 example:  
  ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/a2096409-9086-46ac-aa06-afd2800e034a)
- V2 example:
  ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/ee34baf8-440c-421e-9489-cbf14ce5b242)
- JWT Authorizer:
  - Decode the token, Check the token's algorithm and signature by using the public key that is fetched from the issuer's jwks_uri, Validate claims,
    - kid – The token must have a header claim that matches the key in the jwks_uri that signed the token.
    - iss – Must match the issuer that is configured for the authorizer.
    - aud or client_id – Must match one of the audience entries that is configured for the authorizer.
    - exp – Must be after the current time in UTC.
    - nbf – Must be before the current time in UTC.
    - iat – Must be before the current time in UTC.
    - scope or scp – The token must include at least one of the scopes in the route's authorizationScopes.

## SERVERLESS APPLICATION MODEL (SAM)

- The AWS Serverless Application Model (AWS SAM) is a toolkit that improves the developer experience of building and running serverless applications on AWS. AWS SAM consists of two primary parts:
  - **AWS SAM template specification**: can use to define your serverless application infrastructure on AWS.
  - Use the AWS CloudFormation syntax directly within your AWS SAM template, taking advantage of its extensive support of resource and property configurations
  - AWS SAM does the complex work of transforming your template into the code necessary to provision your infrastructure through AWS CloudFormation
  - **AWS SAM command line interface (AWS SAM CLI)**: A command line tool that you can use with AWS SAM templates and supported third-party integrations to build and run your serverless applications. Perform local debugging and testing.

- Example 
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/5ebffa18-014c-4840-a43a-0f2bee5dc13c)
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/c8100b4d-3ac8-4424-8317-cb10e116ef34)   

- SAM process in breif
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/7f1030ba-f742-49c0-b8d6-81f1f92ac9fc)  
- ```sam init```
![what-is-sam-01](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/7b41ee73-2d51-440f-aafd-0dc0c96e396d)
- ```sam build```
![what-is-sam-02](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/d5ab3491-3d59-4f13-9509-e2ee1270f5d2)  
- ```sam local invoke```:  Invoke Lambda function with payload once and quit after invocation completes
![what-is-sam-04](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/84921cad-5276-4a33-a0f9-7d7b089d27fa)
- ```sam local start-lambda```: Starts a local endpoint that emulates AWS Lambda
- ```sam local start-api```: Starts a local HTTP server that hosts all your functions
- ```sam local generate-event```: Generate sample payloads for event sources 
- ```sam deploy```
![what-is-sam-03](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/e72ab33b-180d-49f9-8370-4b0f9239f233)
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/400c1ad3-d2bd-40d8-b243-e3036ddd4cc6)   

- ```sam build```
  - creates a .aws-sam build directory containing The AWS SAM template, The build.toml file, Contains your Lambda functions and layers structured independently of each other. 
  - The ```--use-container``` option downloads a container image and uses it to build your Lambda functions. The local container is then referenced in your .aws-sam/build.toml file.
  - Use the ```--container-env-var``` to pass environment variables to the build container.
- ```sam deploy```
  - ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/27975e83-c50c-4950-8f4b-599913d64f9e)
  - ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/42fe6619-6e91-49c4-a601-45c69ff88286)

- ```AWS::Serverless::Function```
  - Creates an AWS Lambda function, an AWS Identity and Access Management (IAM) execution role, and event source mappings that trigger the function.
  - ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/ceb275dd-1f75-4ad5-8e78-b4bd95ca9120)
  - ```DeploymentPreference```: enable gradual Lambda deployments.
  - ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/190c72b7-3b87-4cf8-992f-9bd2518f5d9a)
  - ```Hooks```: Validation Lambda functions that are run before and after traffic shifting.
  - ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/ee7e31be-a050-4e50-9b4d-062f0f0af4d8)   

- ```AWS::Serverless::Api```
  - Creates a collection of Amazon API Gateway resources and methods that can be invoked through HTTPS endpoints.
  - ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/ac235e12-9de2-4d57-bae4-4b698e26e6df)

- ```AWS::Serverless::SimpleTable```
  - Creates a DynamoDB table with a single attribute primary key. It is useful when data only needs to be accessed via a primary key.
  - ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/65473eab-3512-41e9-a578-ae54ee5035e8)  
  
**AWS SAM policy templates**

- The AWS Serverless Application Model (AWS SAM) allows you to choose from a list of policy templates to scope the permissions of your Lambda functions and AWS Step Functions state machines to the resources that are used by your application.
- ```S3ReadPolicy```: Gives read only permissions to objects in S3
- ```SQSPollerPolicy```: Allows to poll an SQS queue
- ```DynamoDBCrudPolicy```: CRUD = create read update delete

![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/d4a340a3-0a13-4f7f-b87a-c638baa17600)  

**SAR (Serverless Application Repository)**
- managed repository for serverless applications. It enables teams, organizations, and individual developers to store and share reusable applications, and easily assemble and deploy serverless architectures
- you can use pre-built applications from the Serverless Application Repository in your serverless architectures, helping you and your teams reduce duplicated work, ensure organizational best practices, and get to market faster
- When you publish a serverless application to the AWS Serverless Application Repository, you make it available for others to find and deploy.
- Before you can deploy an application, the AWS Serverless Application Repository checks the application’s template for IAM roles, AWS resource policies, and nested applications that the template specifies that it should create. Applications can contain any of the following four capabilities: ```CAPABILITY_IAM, CAPABILITY_NAMED_IAM, CAPABILITY_RESOURCE_POLICY, and CAPABILITY_AUTO_EXPAND```.   
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/cd57867e-5188-4f8b-9d63-82c364991934)  
- ```sam publish```


## Messaging systems and patterns + Integration

- The following lists out a few common ways AWS customers are using a combination of services.
  - Routing Amazon EventBridge or Amazon Simple Notification Service (Amazon SNS) events to an Amazon Simple Queue Service (Amazon SQS) queue as a buffer for downstream consumers.
  - Pulling events directly from a stream (Kinesis Data Streams or Amazon Managed Streaming for Apache Kafka (Amazon MSK)) or a queue (SQS or Amazon MQ) with EventBridge Pipes and sending events to an     
    EventBridge bus to push out to consumers.
  - Routing EventBridge or SNS events to a Kinesis Data Streams or Amazon MSK for gathering and viewing analytics.

- Consumer
  - 

### SQS (SIMPLE QUEUE SERVICE)

- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/649b6634-896e-4b47-abd9-e92d6702420e)
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/5db10bc2-1717-4a72-8166-5316acfa7db6)

- offers hosted queues that integrate and decouple distributed software systems and components
- Messages in the queue are typically processed by a single subscriber.
- Can have duplicate messages (at least once delivery, occasionally)
- Can have out of order messages (best effort ordering)
- _Producer_
  - Produced to SQS using the SDK (```SendMessage``` API)
  - The message is persisted in SQS until a consumer deletes it
  - Message retention: default 4 days, up to 14 days
- _Consumer_
  - Poll SQS for messages (receive up to 10 messages at a time)
  - Delete the messages using the ```DeleteMessage``` API
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/f022fc17-04f5-4724-9205-df0b78887f07)  
- Increasing throughput of processing of consumers 
  - ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/224ca7e3-77b9-4bff-8428-205d72b3806c)  
- SQS with auto scaling group
  - ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/c015b475-0de9-44c5-9fb0-d54abc05ae66)  
- SQS decoupling
  - ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/9d0ee309-e360-4619-8a6b-fcf213e9b36f)
- _Standard vs FIFO queues_
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/937d6729-dbc8-40f7-a660-70ba89531060)
- Short polling:
  - Amazon SQS sends the response right away, even if the query found no messages.
- Long polling:
  - Amazon SQS sends an empty response only if the polling wait time expires. sends a response after it collects at least one available message, up to the maximum number of messages specified in the request

**SQS MESSAGE VISIBILITY**

- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/efbf4ebd-3aa1-45df-b262-6ba1070d5650)  
- Amazon SQS sets a visibility timeout, a period of time during which Amazon SQS prevents all consumers from receiving and processing the message. The default visibility timeout for a message is 30 seconds. The minimum is 0 seconds. The maximum is 12 hours.
- If you don't know how long it takes to process a message, create a heartbeat for your consumer process: Specify the initial visibility timeout (for example, 2 minutes) and then—as long as your consumer still works on the message—keep extending the visibility timeout by 2 minutes every minute.
- You can shorten or extend a message's visibility by specifying a new timeout value using the ```ChangeMessageVisibility``` action.

**SQS WITH (DLQ)**

- Amazon SQS supports dead-letter queues (DLQ), which other queues (source queues) can target for messages that can't be processed (consumed) successfully.
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/6676e2a7-fd79-4e16-83d8-e178b996df94)
- The ```maxReceiveCount``` is the number of times a consumer tries receiving a message from a queue without deleting it before being moved to the dead-letter queue.
- The redrive allow policy specifies which source queues can access the dead-letter queue (Good to set a retention of 14 days in the DLQ)
- You can use dead-letter queue redrive to manage the lifecycle of unconsumed messages. After you have investigated the attributes and related metadata available for standard unconsumed messages in a dead-letter queue, you can redrive the messages back to their source queues.
- DLQ of a FIFO queue must also be a FIFO queue
- DLQ of a Standard queue must also be a Standard queue
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/45e03fc8-151f-446c-a4ec-93216b2f2c19)

**SQS DELAY QUEUE**
- Delay queues let you postpone the delivery of new messages to consumers for a number of seconds, for example, when your consumer application needs additional time to process messages.
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/fd84f9c6-1826-406c-92b2-977c64177eea)  (0-15MINS)

- SQS JAVA EXTENDED CLIENT
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/271e849e-51af-4a32-ad5c-a63260c6b167)    

**SQS FIFO DEDUPLICATION**
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/f42fdf6e-78fc-4656-b069-bc00afe02f97)
- Message deduplication ID is the token used for deduplication of sent messages. If a message with a particular message deduplication ID is sent successfully, any messages sent with the same message deduplication ID are accepted successfully but aren't delivered during the 5-minute deduplication interval.
- Content-based deduplication: will do a SHA-256 hash of the message body

**SQS GROUPING MESSAGES**
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/dd7ee710-8fab-42b0-9d7b-eb6c94aa4e85)
- MessageGroupId is the tag that specifies that a message belongs to a specific message group. Messages that belong to the same message group are always processed one by one, in a strict order relative to the message group (however, messages that belong to different message groups might be processed out of order).


**SQS SECURITY**
- IAM POLICY SYSTEM
  - Attach a permission policy to a user or a group in your account, Attach a permission policy to a user in another AWS account, Attach a permission policy to a role (grant cross-account permissions) 
- SQS ACCESS POLICIES
  - Grant one permission to one AWS account
  - ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/0a87684d-f001-453e-b9b9-2cb1b01f1b83)
  - Grant all permissions to two AWS accounts
  - ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/0aab93ca-3ee8-4d9f-a542-f2d1093c6dcc)
  - Grant a permission to all users
  - ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/a07e00ee-0eb8-49df-99dd-75693b9a6609)  


**IMPORTANT APIS**

• CreateQueue (MessageRetentionPeriod), DeleteQueue   
• PurgeQueue: delete all the messages in queue   
• SendMessage (DelaySeconds), ReceiveMessage, DeleteMessage   
• MaxNumberOfMessages: default 1, max 10 (for ReceiveMessage API)   
• ReceiveMessageWaitTimeSeconds: Long Polling  
• ChangeMessageVisibility: change the message timeout  
• Batch APIs for SendMessage, DeleteMessage, ChangeMessageVisibility helps decrease your costs

**CREATING SQS**
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/930e7095-87b3-481f-ab59-d2125746bd6e)   
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/9202b7f6-2e46-4d31-bda2-845e59a295b3)  
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/c3bc3be8-0280-4f18-9291-aad2fe9353e3)  
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/5aa44b98-0716-466c-ba6a-12b13c9c3a02)   
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/2aac1bb7-ba8f-426d-9ccd-1d89bbcd651c)   

### SNS (SIMPLE NOTIFICATION SERVICE)

- publish-subscribe service that provides message delivery from publishers (also known as producers) to multiple subscriber endpoints(also known as consumers)
- Publishers communicate asynchronously with subscribers by sending messages to a _topic_
- Subscribers can subscribe to an Amazon SNS topic and receive published messages using a supported endpoint type
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/40cffb7c-5879-43ee-96ef-12338906a409)   

**SQS-SNS FANOUT PATTERN**

- Push once in SNS, receive in all SQS queues that are subscribers
- S3 Events to multiple queues
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/85dd2535-b474-4aed-9186-fa064fdd0183)
- SNS to Amazon S3 through Kinesis Data Firehose
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/82cca1e3-cdda-44db-928e-a83a2f546b50)
- FIFO FANOUT
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/434270c7-ed5a-41c4-b2e5-cd8a9ed5e476)   

**SNS FIFO**

- provide strict message ordering and message deduplication
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/b55a507a-80ed-4c6d-af24-5be17c41cc1b)
- An Amazon SNS FIFO topic always delivers messages to subscribed Amazon SQS queues in the exact order in which the messages are published to the topic, and only once.
- With an Amazon SQS FIFO queue subscribed, the consumer of the queue receives the messages in the exact order in which the messages are delivered to the queue, and no duplicates
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/fecc5f6a-c4fd-4d80-800b-0c2c689f6ffc)
- You can have multiple applications (or multiple threads within the same application) publishing messages to an SNS FIFO topic in parallel. To determine the established sequence of messages, you can check the sequence number (ASSIGNED BY AWS SNS)
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/921ec06d-908b-4717-bad1-6f3b4fb5fdcb)
- Messages that belong to the same group are processed one by one, in a strict order relative to the group.
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/74b6761b-7189-4b10-83a5-79abe4a4122c)

**MESSAGE FILTERING**
- A filter policy is a JSON object containing properties that define which messages the subscriber receives
- Amazon SNS FIFO topics support message filtering.
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/2c7c2a0d-1836-47c8-a1af-10d36b3e1294)
- Ex. for messageAttributes policy 
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/5e51e379-8b2a-4c20-91c1-a4b02db3cc00)
- For messageBody policy
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/240bad2a-8f73-4d36-be93-0cb147a2a4a6)


**DLQ**
- For any type of error, Amazon SNS can sideline messages to Amazon SQS dead-letter queues so data isn't lost.
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/f0c1b366-c27e-4398-924d-6a5b058fe51d)  

**SNS SECURITY**
- RAW MESSAGE DELIVERY:
  - ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/32398b0c-dd25-4b0d-86fc-e4e8adb4b5aa)
- CROSS ACCOUNT DELIVERY
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/e98a6bd0-e08d-4c89-8706-daee9bc3d997)   

### KINESIS

- Kinesis Data Streams to collect and process large streams of data records in real time.
- Data Streams application reads data from a data stream as data records.
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/c9f4c82c-3de2-4e2c-9963-7115768256f7)
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/8f2af240-da79-464e-8d28-672758027f9e)    
- A Kinesis data stream is a set of shards. Each shard has a sequence of data records. Each data record has a sequence number that is assigned by Kinesis Data Streams.
- Data records are composed of a sequence number, a partition key, and a data blob, which is an immutable sequence of bytes.
- The retention period is the length of time that data records are accessible after they are added to the stream (1-365 days), Ability to reprocess (replay) data
- _Provisioned mode_
  - you must specify the number of shards for the data stream. The total capacity of a data stream is the sum of the capacities of its shards. You can increase or decrease the number of shards in a data stream as needed and you are charged for the number of shards at an hourly rate.
- _On-demand mode_: 
  - Kinesis Data Streams automatically manages the shards in order to provide the necessary throughput. You are charged only for the actual throughput that you use and Kinesis Data Streams automatically accommodates your workloads’ throughput needs as they ramp up or down
- Producers put records into Amazon Kinesis Data Streams
- Consumers get records from Amazon Kinesis Data Streams and process them.
- A shard is a uniquely identified sequence of data records in a stream
- A partition key is used to group data by shard within a stream
- Each data record has a sequence number that is unique per partition-key within its shard.
- The Kinesis Client Library (KCL) is compiled into your application to enable fault-tolerant consumption of data from the stream.

**Producers**
- Puts data records into data streams
• Data record consists of:  
• Sequence number (unique per partition-key within shard)  
• Partition key (must specify while put records into stream)  
• Data blob (up to 1 MB)   
• Producers:  
• AWS SDK: simple producer  
• Kinesis Producer Library (KPL): C++, Java, batch, compression, retries  
• Kinesis Agent: monitor log files 
• Write throughput: 1 MB/sec or 1000 records/sec per shard  
• ```PutRecord``` API  
• Use batching with PutRecords API to reduce costs & increase throughput  

![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/896cde65-c8a4-4d15-8167-31dacd2bf99c)   
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/c35f4501-3079-4fa4-b467-9cf4fa6b92e9)  

**Consumers**
- Custom Consumer (AWS SDK) – Classic or Enhanced Fan-Out
  - Classic
    - pull records by consumers
    - shared throughput
  - Enhanced
    - subscribed, push records to consumers
    - same throughput to all consumers 
• Kinesis Client Library (KCL): library to simplify reading from data stream
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/096f9883-69fa-4624-be5d-c3ed7409a2f9)   
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/c714cf7b-c847-42fc-b072-b061bdf00d25)  

**KCL**
- A Java library that helps read record from a Kinesis Data Stream with distributed applications sharing the read workload
- Each shard is to be read by only one KCL instance
• 4 shards = max. 4 KCL instances  
• 6 shards = max. 6 KCL instances
- Records are read in order at the shard level  
- Versions:  
• KCL 1.x (supports shared consumer)   
• KCL 2.x (supports shared & enhanced fan-out consumer
- For each Amazon Kinesis Data Streams application, KCL uses a unique lease table (stored in a Amazon DynamoDB table) to keep track of the shards in a KDS data stream that are being leased and processed by the workers of the KCL consumer application.

- Task split by KCL workers via DynamoDB
- Max it can be as number of shards, otherwise extra KCL workers wouldn't do anything (idle)
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/59b2ea74-91b1-4363-b33d-8872485b729e)
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/e901c896-e055-4691-9ae6-fd2502ea92e0)
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/9970d975-829c-4271-8dfe-9ba941151705)
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/81e735f6-6089-49e8-b233-0d7a6e092bf1)  

**kinesis shard split and merge**
- Used to divide a “hot shard”
- The old shard is closed and will be deleted once the data is expired
- Can’t split into more than two shards in a single operation
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/bda17017-4a4d-431d-beb7-b0e0422c5f38)
- Can be used to group two shards with low traffic (cold shards)
- Old shards are closed and will be deleted once the data is expired
- Can’t merge more than two shards in a single operation
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/cbe5ab62-862b-4c4a-9773-ce7088a0272f)  

**Kinesis Data Firehose**
- delivering real-time streaming data to multiple destinations
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/d9e62658-5e93-4a8b-8992-40b336b8e4fb)
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/24c359c6-3364-41f1-848e-4267caaf31c8)
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/e5db53fa-3e4a-4046-8a03-974cb5125289)
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/6a3162c1-8188-45d4-8735-631a7e11b10d)
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/8c6521ba-ac59-4e83-ba38-2ab0d9bc511d)  

![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/29d06431-3af5-400b-8d8b-9844baad83e3)  

**Kinesis Data analytics (SQL applications)**
- Real-time analytics on Kinesis Data Streams & Firehose using SQL
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/a476e414-bf40-42ca-be3d-4d4167789172)  

**Kinesis Data analytics (For Apache Flink application)**
- Use Flink (Java, Scala or SQL) to process and analyze streaming data
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/1ee718a6-64f3-454e-a7f1-3d5c3166b998)   

**SQS VS SNS VS KINESIS**
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/14b8216d-e0d9-4e1c-9677-a84f178b900b)   


# Security

## IAM 
- AWS Identity and Access Management (IAM) is a web service that helps you securely control access to AWS resources.
- You use IAM to control who is authenticated (signed in) and authorized (has permissions) to use resources.
- IAM doesn't requires region selection (global)
- IAM, like many other AWS services, is eventually consistent. IAM achieves high availability by replicating data across multiple servers within Amazon's data centers around the world. If a request to change some data is successful, the change is committed and safely stored. However, the change must be replicated across IAM, which can take some time.

![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/d00d9c94-18c8-4919-9cc0-d77e48b3a4e4)  

- When principal makes a request to AWS for authn and authz, AWS gathers the request information into a request context, which is used to evaluate and authorize the request.
- AWS checks each policy that applies to the context of your request. If a single permissions policy includes a denied action, AWS denies the entire request and stops evaluating. This is called an explicit deny. Because requests are denied by default, AWS authorizes your request only if every part of your request is allowed by the applicable permissions policies.
- IAM users are granted long-term credentials to your AWS resources. In contrast, users in AWS IAM Identity Center (successor to AWS Single Sign-On) are granted short-term credentials to your AWS resources.
- User Federation in usecases like:
  - Your users already exist in a corporate directory: Corporate directory, Microsoft Azure AD, external IDP's like Okta etc..
  - Your users already have Internet identities: Internet identity provider like Login with Amazon, Facebook, Google, or any OpenID Connect (OIDC) compatible identity provider
 
**ACCESS CONTROL METHODS/WAYS:**
- Single sign-on access for human users
- Federated access for human users,
- Cross-account access between AWS accounts
- Long-term credentials for designated IAM users in your AWS account

#######################```TASKS REQUIRING ROOT USER CREDENTIALS```#######################   
- Change your account settings. This includes the account name, email address, root user password, and root user access keys. 
- Restore IAM user permissions. If the only IAM administrator accidentally revokes their own permissions, you can sign in as the root user to edit policies and restore those permissions.
- Activate IAM access to the Billing and Cost Management console.
- View certain tax invoices. An IAM user with the aws-portal:ViewBilling permission can view and download VAT invoices from AWS Europe, but not AWS Inc. or Amazon Internet Services Private Limited (AISPL).
- Close your AWS account.
- Register as a seller in the Reserved Instance Marketplace.
- Configure an Amazon S3 bucket to enable MFA (multi-factor authentication).
- Edit or delete an Amazon Simple Queue Service (Amazon SQS) resource policy that denies all principals.
- Edit or delete an Amazon Simple Storage Service (Amazon S3) bucket policy that denies all principals.
- Sign up for AWS GovCloud (US).
- Request AWS GovCloud (US) account root user access keys from AWS Support.


#######################```IAM USER```#######################    

- An IAM user is an identity within your AWS account that has specific permissions for a single person or application
- An IAM group is an identity that specifies a collection of IAM users. You can't sign in as a group. You can use groups to specify permissions for multiple users at a time. 
- Every User can be either alone or put into a group  i.e. policies can be individually assigned to IAM user (single) or to a group.

**While creating IAM User Two options ->** 
- Specify a user in Identity Center - Recommended
We recommend that you use Identity Center to provide console access to a person. With Identity Center, you can centrally manage user access to their AWS accounts and cloud applications.
- I want to create an IAM user
We recommend that you create IAM users only if you need to enable programmatic access through access keys, service-specific credentials for AWS CodeCommit or Amazon Keyspaces, or a backup credential for emergency account access.
- Control maximum permissions using IAM boundary:
  - An entity's permissions boundary allows it to perform only the actions that are allowed by both its identity-based policies and its permissions boundaries.
  - The permissions boundary for an IAM entity (user or role) sets the maximum permissions that the entity can have.
  - If any one of these policy types explicitly denies access for an operation, then the request is denied. 

- Administrative access to IAM user group (group name is admin here)
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/3bb8415f-823f-4726-88ab-a28640aa1494)

- Now, this user can also have its own alias set after which its own custom URL will be generated for Logon.

#######################```IAM POLICIES```#######################  

**Identity-based and resource-based policies**
- Identity-based policies are permissions policies that you attach to an IAM identity, such as an IAM user, group, or role.
  - AWS Managed policies, Customer managed policies, Inline policies 
- Resource-based policies are permissions policies that you attach to a resource such as an Amazon S3 bucket or an IAM role trust policy.
  - Resource-based policies are inline policies, and there are no managed resource-based policies.
  - The IAM service supports only one type of resource-based policy called a role trust policy, which is attached to an IAM role.
  - Trust policies define which principal entities (accounts, users, roles, and federated users) can assume the role. 

- For ex. in below, identity based policies given to users defines what actions can they perform on specific resources whereas resource based policies defines which principals (users) have access to them.
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/0386d74c-f8b0-49bb-acba-25eff9c5b4ed)   
- For requests made from one account to another, the requester in Account A must have an identity-based policy that allows them to make a request to the resource in Account B. Also, the resource-based policy in Account B must allow the requester in Account A to access the resource. There must be policies in both accounts that allow the operation, otherwise the request fails.
- In addition, Amazon S3 supports a permission mechanism known as an access control list (ACL) that is independent of IAM policies and permissions. You can use IAM policies in combination with Amazon S3 ACLs.
- ACL(ACCESS CONTROL LIST):
  - enable you to manage access to buckets and objects.
  - When you create a bucket or an object, Amazon S3 creates a default ACL that grants the resource owner full control over the resource.
  - ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/b71a231f-6e5c-42bf-94ea-9b97407af266)  


**AWS MANAGED POLICY VS CUSTOMER MANAGED POLICY**
- Managed policies that are created and managed by AWS (AWS MANAGED POLICIES)
- AWS managed policies make it convenient for you to assign appropriate permissions to users, groups, and roles. It is faster than writing the policies yourself
- Managed policies that you create and manage in your AWS account.
- You cannot change the permissions defined in AWS managed policies. AWS occasionally updates the permissions defined in an AWS managed policy.   
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/baa8855f-4321-4b05-accf-cce7167c558e)   

  
- Customer managed policies provide more precise control over your policies than AWS managed policies. You can create, edit, and validate an IAM policy in the visual editor or by creating the JSON policy document directly.   

- IAM Policy inheritance   
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/99800cc5-9184-4095-8b2a-59fbc71f949a)   

- IAM policy structure and meaning of JSON documents   
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/0f61aa3e-c15e-4a73-9fb4-1384479a7b99)  
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/d6d1ddbe-8947-4970-8cac-bc28f0bdc7e7)   


- IAM policy can be created using policy visual editor   
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/93b8242a-d731-4f5b-93be-fcb97829e8ae)  

- Overall for ex. Below shows User which has policies attached via different mechanisms   
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/6e7a6b17-7588-47f3-a35d-62036962c697)   

- Permission evaluation 
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/ad3f8995-1fc6-4ae5-8551-ada681ea12c8)   
- When evaluating if an IAM Principal can perform an operation X on a
bucket, the union of its assigned IAM Policies and S3 Bucket Policies will
be evaluated
- Few examples of how permission are evaluated
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/b7bb2b82-25c3-4acf-8f22-d3194952d8c9)   
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/a940fcf6-05e3-4ec0-bdf5-900c946d1751)
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/553f6f1b-7e62-46fb-a61a-a4a866ac2541)
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/53861e7a-c8db-43aa-ae9f-7227bdc4bb63)  



#######################```PASSWORD POLICY IAM```#######################   
- IAM password policy can be managed and user can be required to change their password at certain time or their first logon etc...   
- Password policy can be either chosen as AWS default or it can be new custom policy as defined by admin user.    

![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/9f082128-6eeb-4f96-9a0f-cce471281413)   


#######################```MFA```#######################   
- Multi factor authentication
- Types of MFA devices
  - Virtual MFA device (google authenticator, Authy)
  - Universal 2nd Factor U2F key ex. YubiKey by Yubico (3rd party)
  - Hardware Key Fob MFA device (Gemalto 3rd party)
  - Hardware Key Fob MFA device for AWS GovCloud (surePassID 3rd party)

- You can register up to 8 MFA devices of any combination with your AWS account root and IAM user.   
 
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/b91a99e8-877b-4efc-9e10-fcf5c34a2485)   

#######################```LOGON WITH ACCESS KEYS```#######################  
- ACCESS KEY ID (USERNAME)
- SECRET ACCESS KEYS (PASSWORD)

- According to purpose of access keys, AWS recommends multiple options like AWS CLI V2, CLOUDSHELL ETC...

#######################```IAM ROLES```#######################  

- A role is an IAM identity that you can create in your account that has specific permissions.
- However, instead of being uniquely associated with one person, a role can be assumed by anyone who needs it. A role does not have standard long-term credentials such as a password or access keys associated with it. Instead, when you assume a role, it provides you with temporary security credentials for your role session.
- Roles are meant to be depending on various use cases, for ex. Assigned directly to the aws services instead of users.
- Few examples shown below:    
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/fd2b5ed5-4f5e-4d72-a72d-4e43466e1969)
- When you create a role, you create two policies:
  - A role ```trust policy``` that specifies who can assume the role and a ```permissions policy``` that specifies what can be done with the role.
  - You specify the trusted principal who is allowed to assume the role in the role trust policy.  
- For ex. Role creation for EC2 instance   
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/1234becc-443e-4fa5-a067-837e098ff897)
- Role chaining:
  - Role chaining is when you use a role to assume a second role through the AWS CLI
  - AWS does not treat using roles to grant permissions to applications that run on EC2 instances as role chaining.

**SCENARIOS FOR ROLES**
- Providing access to an IAM user in another AWS account that you own  
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/8e074f0b-8f9f-4608-abe9-2444c2861c72)
- Providing access for non AWS workloads
- Providing access to AWS accounts owned by third parties
- Providing access to an AWS service
- Providing access to externally authenticated users (identity federation)   
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/0e8a366e-3b74-4e7d-a880-fd828d6e7b7d)   

**Using IAM Roles**
- AWS Management Console (by switching roles)
- assume-role CLI or AssumeRole API operation
- assume-role-with-saml CLI or AssumeRoleWithSAML API operation
- assume-role-with-web-identity CLI or AssumeRoleWithWebIdentity API operation
- Console URL constructed with AssumeRole, AssumeRoleWithSAML, AssumeRoleWithWebIdentity (broker constructs the URL and calls STS for assuming the roles)

**The confused deputy problem**
- The confused deputy problem is a security issue where an entity that doesn't have permission to perform an action can coerce a more-privileged entity to perform the action.
- Prevention: ```aws:SourceArn``` and ```aws:SourceAccount``` global condition context keys in resource-based policies to limit the permissions that a service has to a specific resource.

#######################```IAM POLICY SIMULATOR```#######################  
- One can choose and evaluate the roles and policies attached in real time using this simulator.   
 
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/11dbc126-c328-4225-bf62-d2d25ff816e2)   


#######################```ABAC```#######################   
- Attribute-based access control (ABAC) is an authorization strategy that defines permissions based on attributes. In AWS, these attributes are called tags. You can attach tags to IAM resources, including IAM entities (users or roles) and to AWS resources.
- These ABAC policies can be designed to allow operations when the principal's tag matches the resource tag.
- ABAC is helpful in environments that are growing rapidly and helps with situations where policy management becomes cumbersome.
- The disadvantage to using the traditional RBAC model is that when employees add new resources, you must update policies to allow access to those resources.
- RBAC
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/6c593575-9a2e-4482-ae0f-34c1fc501c34)    
- ABAC
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/5e0c31ef-ddb0-49ad-a38e-d4dbf3e45751)  

#######################```SECURITY TOKEN SERVICE (STS)```#######################   
- You can use the AWS Security Token Service (AWS STS) to create and provide trusted users with temporary security credentials that can control access to your AWS resources.
- Temporary security credentials are not stored with the user but are generated dynamically and provided to the user when requested.
- By default, AWS STS is a global service with a single endpoint at https://sts.amazonaws.com. However, you can also choose to make AWS STS API calls to endpoints in any other supported Region.
- This is used in Identity federation usecases, cross account accesses
- The AWS STS API operations create a new session with temporary security credentials that include an access key pair and a session token. The access key pair consists of an access key ID and a secret key. Users (or an application that the user runs) can use these credentials to access your resources.
- TO Have user call STS, User should be assigned in-line policy with STS assumeRole (depending on usecase there are 3 options)
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/868fa142-b2d2-4622-be23-8d488f888c20)    
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/1f78aa93-d980-4860-9bf7-ebada1995d94)   

- Bearer tokens:
  - AWS STS can help in getting bearer tokens which are required for accessing some services programmatically. For ex. AWS CodeArtifact etc..
  - The token's access key ID begins with the ABIA prefix (can help in cloudtrail logs)
  - The bearer token can be used only for calls to the service that generates it and in the Region where it was generated.
- All the STS calls can be traced by cloudtrail logs for ex. as shown below :  
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/e8e7e18e-1c0b-49a6-9434-2992c60c5f1d)   
- Calls made from another account to access cross-account services which assumes a role : ```sts:SourceIdentity``` condition key in the role trust policy to require users to specify an identity when they assume a role. For ex. shown below :   
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/14be993f-ac99-44ae-b237-9ee065e1fbd9)   
Now, For this same request one entry will be there in the another account (assumed role account log).
- When performing role chaining, tags are passed on from first assumed role as "transitive tags" as shown below:
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/50429340-5926-463b-9e80-607fd2813c05)
- Web Identity provider - includes the tags passed through identity provider as shown below :
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/3614606a-409c-4215-b014-8878362a6cc8)  
- Sign-in events are logged as well except the incorrect username whose information is then masked with ```HIDDEN_DUE_TO_SECURITY_REASONS```    
EXAMPLES OF STS API's :
- AssumeRole, AssumeRoleWithSAML, AssumeRoleWithWebIdentity, GetFederationToken, GetSessionToken
- The permissions policy of the role that is being assumed determines the permissions for the temporary security credentials that are returned by AssumeRole, AssumeRoleWithSAML, and AssumeRoleWithWebIdentity
- Optionally, one can pass inline or managed session policies as parameters which filters only the passed permissions returned.

* AWS STS WITH MFA
- aws:MultiFactorAuthPresent:true   
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/f9fdd359-12c3-475a-8bd8-bd6077140f94)
- GetSessionToken returns: • Access ID • Secret Key • Session Token • Expiration date


#######################```IAM SECURITY TOOLS```#######################   
- IAM CREDENTIALS REPORT (ACCOUNT LEVEL)
  - report that lists all your account users and the status of their various credentials
 
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/dc27d454-ad21-44b4-981e-b575d4911462)    

- IAM ACCESS ADVISOR (USER LEVEL)
  - shows service permissions granted to a user and when were they last accessed
  - you can use this information to revise the policies, can help in reducing the permissions for least privelege.

![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/d79b24a5-b708-4890-96bf-2fc1596b97ba)     

#######################```IAM BEST PRACTICES```#######################   
- DONT'T user ever root user except for AWS account setup
- One physical user = AWS IAM user  
- Assign users to groups and assign permissions to groups
- create a strong password policy
- use and enforce MFA
- create and use Roles for giving permissions to AWS services
- Use Access keys for Programmatic access (CLI/SDK)  
- Audit permission of your account using IAM creds report and access advisor   
- Never share IAM user and access keys

#######################```AWS SHARED RESPONSIBILITY MODEL FOR IAM```#######################    
- AWS
  - INFRASTRUCTURE OF GLOBAL NETWORK SECURITY
  - CONFIGURATION AND VULN ANALYSIS
  - COMPLIANCE VALIDATION
 
- YOU
  - USERS, GROUPS, ROLES AND POLICIES MANAGEMENT AND MONITORING
  - ENABLE MFA ON ALL ACCOUNTS
  - ROTATE ALL YOUR KEYS OFTEN
  - USE IAM ROOLS TO APPLY APPROPRIATE PERMISSIONS
  - ANALYZE ACCESS PATTERNS AND REVIEW PERMISSIONS

#######################``` Identity providers and federation ```#######################      

- In case users are already managed outside of AWS like in corporate directory or any other identity providers, you can use IAM identity providers instead of creating IAM users in your AWS account. Ex. well-known IdP, such as Login with Amazon, Facebook, or Google.
- IAM supports IdPs that are compatible with OpenID Connect (OIDC) or SAML 2.0 (Security Assertion Markup Language 2.0)   

**OIDC**   
- OpenID Connect is an interoperable authentication protocol based on the OAuth 2.0 framework of specifications (IETF RFC 6749 and 6750). It simplifies the way to verify the identity of users based on the authentication performed by an Authorization Server and to obtain user profile information in an interoperable and REST-like manner.

![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/a286a5c3-fdd3-40d0-8f9f-78a390feae8a)   

**SAML**  
- Security Assertion Markup Language is an open standard for exchanging authentication and authorization data between parties, in particular, between an identity provider and a service provider using SOAP over HTTP.
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/d5d4f3d3-acf4-4a65-a725-157c1590c42f)     
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/583d89be-6d08-4abe-9ad6-fe9580bf8251)   
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/f1309a89-a805-4b6d-bab9-3f919236a144)     
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/f639a8f3-3a0c-4d10-b7fe-0936e3776d82)
- A SAML Request, also known as an authentication request, is generated by the Service Provider to "request" an authentication.
- A SAML Response is generated by the Identity Provider. It contains the actual assertion of the authenticated user. In addition, a SAML Response may contain additional information, such as user profile information and group/role information, depending on what the Service Provider can support.
- The Service Provider never directly interacts with the Identity Provider. A browser acts as the agent to carry out all the redirections.

- The preferred way to use web identity federation is to use Amazon Cognito.
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/6c922032-fbad-4d27-be1f-17698bc16f4a)  
- Using SAML-based federation for API access to AWS
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/2119d497-dee5-4be7-9fc7-2d0e35e6b398)    

-------------------------   
- IAM OIDC identity providers are entities in IAM that describe an external identity provider (IdP) service that supports the OpenID Connect (OIDC) standard, such as Google or Salesforce. You use an IAM OIDC identity provider when you want to establish trust between an OIDC-compatible IdP and your AWS account.
- If you are using an OIDC identity provider from either Google, Facebook, or Amazon Cognito, do not create a separate IAM identity provider using this procedure. These OIDC identity providers are already built-in to AWS and are available for your use.    
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/9bec80a7-c6a4-46b5-84da-711d986aa372)

- Assigning roles to federated identity :
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/86ae1fb5-a4b3-4bab-be80-e234341be7b9)     

![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/780e6c3b-70c1-4317-86ea-950b5c1fac33)  

Note: 
- Github OIDC provider: Best practice is to limit the to a specific GitHub organization, repository, or branch using the conditions section defined in the permission policies.

- For trusting the external IDP, you must supply a thumbprint. IAM requires the thumbprint for the top intermediate certificate authority (CA) that signed the certificate used by the external identity provider (IdP).   

- SAML OIDC identity provider configuration requires metadata document to be uploaded. This document includes the issuer's name, expiration information, and keys that can be used to validate the SAML authentication response (assertions) that are received from the IdP.   
- After you have verified a user's identity in your organization, the external identity provider (IdP) sends an authentication response to the AWS SAML endpoint at https://region-code.signin.aws.amazon.com/saml


- Custom IDP broker: You can write and run code to create a URL that lets users who sign in to your organization's network securely access the AWS Management Console. The URL includes a sign-in token that you get from AWS and that authenticates the user to AWS.

#######################``` Tagging IAM resources ```#######################      
- A tag is a custom attribute label that you can assign to an AWS resource. Each tag has two parts: A tag key, An optional field known as a tag value
- Names for AWS tags are case sensitive so ensure that they are used consistently. 

**When to use IAM policies vs S3 policies**
- If question is What can this user do in AWS? -> choose IAM policies 
- If question is Who can access this S3 bucket?? -> choose S3 bucket policies

#######################``` DIRECTORY SERVICES ```#######################      
**LDAP**
- Lightweight Directory Access Protocol (LDAP) is a vendor-neutral software protocol used to lookup information or devices within a network
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/d56cb79e-f31f-4ab3-adad-fb3bafbc9563)
- users will go through one of two possible user authentication methods: simple authentication, like SSO with login credentials, or SASL authentication, which binds the LDAP server to a program like Kerberos.


**ACTIVE DIRECTORY, AWS DIRECTORY SERVICES**
- LDAP is the core protocol used in–but not exclusive to–Microsoft’s Active Directory (AD) directory service, a large directory service database that contains information spanning every user account in a network
- ADDS: Active Directory stores information about objects on the network and makes this information easy for administrators and users to find and use.
- ADFS: Active Directory Federation Service (AD FS) enables Federated Identity and Access Management by securely sharing digital identity and entitlements rights across security and enterprise boundaries. AD FS extends the ability to use single sign-on functionality that is available within a single security or enterprise boundary to Internet-facing applications to enable customers, partners, and suppliers a streamlined user experience while accessing the web-based applications of an organization.
- Four options in AWS:
  - AWS MANAGED AD: AWS Directory Service for Microsoft Active Directory is powered by an actual Microsoft Windows Server Active Directory (AD), managed by AWS in the AWS Cloud.
  - AD Connector: AD Connector is a proxy service that provides an easy way to connect compatible AWS applications. When you add users to AWS applications such as Amazon QuickSight, AD Connector reads your existing Active Directory to create lists of users and groups to select from
  - Simple AD is a Microsoft Active Directory–compatible directory from AWS Directory Service that is powered by Samba 4.
  - Amazon Cognito is a user directory that adds sign-up and sign-in to your mobile app or web application using Amazon Cognito User Pools.

#######################``` IAM IDENTITY CENTER ```#######################    

- IAM Identity Center provides one place where you can create or connect workforce users and centrally manage their access across all their AWS accounts and applications.
- With application assignments, you can grant your workforce users in IAM Identity Center single sign-on access to SAML 2.0 applications, such as Salesforce and Microsoft 365
- With multi-account permissions you can plan for and centrally implement IAM permissions across multiple AWS accounts at one time without needing to configure each of your accounts manually.

* STEPS TO START USING IDENTITY CENTER:
  - Enable identity center (also should be using AWS organizations otherwise it will create one in the process)
  - Choose your identity source:
    - Identity Center directory default
    - Active Directory
    - External identity provider
  - After you enable IAM Identity Center, you must choose your identity source. The identity source that you choose determines where IAM Identity Center searches for users and groups that need single sign-on access.
  - Create an administrative permission set: Permission sets are stored in IAM Identity Center and define the level of access that users and groups have to an AWS account.
  - To set up AWS account access for an administrative user in IAM Identity Center, you must assign the user to the AdministratorAccess permission set.
  - Similarly, for different other uses, least privelege sets can be created and accordingly assigned when new users/groups are synced from other directories.
 
- When working in IAM Identity Center, users must be uniquely identifiable. IAM Identity Center implements a user name that is the primary identifier for your users. For most of SAML based integration, it's the user's email address. IAM Identity Center allows you to specify something other than an email address for user sign-in.
- Identity Center enabled applications can work with users and groups for which IAM Identity Center is aware. Provisioning is the process of making user and group information available for use by IAM Identity Center and Identity Center enabled applications.
- There are two types of authentication sessions maintained by IAM Identity Center: one to represent the users’ sign in to IAM Identity Center, and another to represent the users’ access to IAM Identity Center enabled applications, such as Amazon SageMaker Studio or Amazon Managed Grafana. Sessions are cached for 1 hr refreshable, so if user is disabled/deleted, then upto 1 hr, it can still perform or login or create another sessions.
- A permission set is a template that you create and maintain that defines a collection of one or more IAM policies. One can use predefined permission sets or custom permission sets.
- Although IAM Identity Center determines access from the Region in which you enable the service, AWS accounts are global. This means that after users sign in to IAM Identity Center, they can operate in any Region when they access AWS accounts through IAM Identity Center
- IAM service-linked roles: A service-linked role is a unique type of IAM role that is linked directly to IAM Identity Center. It is predefined by IAM Identity Center and includes all the permissions that the service requires to call other AWS services on your behalf

#######################``` AMAZON COGNITO ```#######################    

- Amazon Cognito is an identity platform for web and mobile apps. It’s a user directory, an authentication server, and an authorization service for OAuth 2.0 access tokens and AWS credentials.
- With Amazon Cognito, you can authenticate and authorize users from the built-in user directory, from your enterprise directory, and from consumer identity providers like Google and Facebook.

**User pools**  
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/5456ba5e-d0ff-4c94-8d40-21d0ff939325)  
- User pools are a user directory with both self-service and administrator-driven user creation, management, and authentication.
- Your organization's SAML 2.0 and OIDC IdPs bring workforce identities into Cognito and your app. The public OAuth 2.0 identity stores Amazon, Google, Apple and Facebook bring customer identities.
- From a user pool, you can issue authenticated JSON web tokens (JWTs) directly to an app, a web server, or an API.

OIDC IdP |	Issue ID tokens to authenticate users
Authorization server	| Issue access tokens to authorize user access to APIs
SAML 2.0 SP	| Transform SAML assertions into ID and access tokens
OIDC SP	| Transform OIDC tokens into ID and access tokens
OAuth 2.0 SP	| Transform ID tokens from Apple, Facebook, Amazon, or Google to your own ID and access tokens
Authentication frontend service	| Sign up, manage, and authenticate users with the hosted UI
API support for your own UI	| Create, manage and authenticate users through API requests in supported AWS SDKs¹
MFA	| Use SMS messages, TOTPs, or your user's device as an additional authentication factor¹
Security monitoring & response	| Secure against malicious activity and insecure passwords¹
Customize authentication flows	| Build your own authentication mechanism, or add custom steps to existing flows¹
Groups	| Create logical groupings of users, and a hierarchy of IAM role claims when you pass tokens to identity pools
Customize ID tokens	| Customize your ID tokens with new, modified, and suppressed claims
Customize user | attributes	Assign values to user attributes and add your own custom attributes

**Identity pools**  
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/9baf3149-1f11-45e6-b056-f8e01abeb8ee)   
- Set up an Amazon Cognito identity pool when you want to authorize authenticated or anonymous users to access your AWS resources.
- Identity pools use both role-based (RBAC) and attribute-based access control (ABAC) to manage your users’ authorization to access your AWS resources.
- An identity pool can accept authenticated claims directly from both workforce and consumer identity providers.
- The token that your identity pool creates for the identity can retrieve temporary session credentials from AWS Security Token Service (AWS STS).

Amazon Cognito user pool SP	| Exchange an ID token from your user pool for web identity credentials from AWS STS
SAML 2.0 SP	| Exchange SAML assertions for web identity credentials from AWS STS
OIDC SP	| Exchange OIDC tokens for web identity credentials from AWS STS
OAuth 2.0 SP	| Exchange OAuth tokens from Amazon, Facebook, Google, Apple, and Twitter for web identity credentials from AWS STS
Custom SP	| With AWS credentials, exchange claims in any format for web identity credentials from AWS STS
Unauthenticated access	| Issue limited-access web identity credentials from AWS STS without authentication
Role-based access control	| Choose an IAM role for your authenticated user based on their claims, and configure your roles to only be assumed in the context of your identity pool
Attribute-based access control	| Convert claims into principal tags for your AWS STS temporary session, and use IAM policies to filter resource access based on principal tags

- An Amazon Cognito user pool can also fulfill a dual role as a service provider (SP) to your IdPs, and an IdP to your app.
- When to choose what ?

**Usecases**
- Authenticate with a user pool   
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/f8657b51-ec3e-41b3-b844-a91181f45c67)   
- Access your server-side resources with a user pool
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/ebc22418-984a-4a8c-a503-feeca4a4d4bc)
- Access resources with API Gateway and Lambda with a user pool
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/6766c44a-b632-4410-9dfb-00bd0752f79c)
- Access AWS services with a user pool and an identity pool
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/7fd3590f-f86c-4555-ad79-0775c7693cee)
- Authenticate with a third party and access AWS services with an identity pool
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/eefe922e-e753-4e5a-a078-045dc7dca4aa)   
- Access AWS AppSync resources with Amazon Cognito
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/9b3ba223-8652-46fb-88f5-b16136a0060b)   


**Configuring User pools in Cognito** 
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/ab0b2cfb-8bbd-4b31-9893-899ccd56c05c)  
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/fb5f69d4-344b-40e8-9c21-e9ae4a922d3e)   
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/90c96aa1-879d-4626-80d4-2e8ae5b99296)  
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/c85878a3-185f-4345-a612-027cc4c9fdd6)   
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/bc89fba9-60d1-46eb-a5f2-f22659b61e15)    
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/f62e3f7e-8286-4023-82ff-6b530b95172e)

**Configuring Identity pools in Cognito** 
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/09ada152-e41a-4168-b613-2059c10ac17c)   
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/9ad67ec5-3aae-468c-b6d9-8f1d994831b0)    
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/e948aa05-8ae4-4611-aa64-4545330df7bc)  
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/08e536da-388b-4b1f-b91b-2101f6fed754)  
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/d29ae56a-8eb5-4600-92dc-fc58dac218d5)  
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/bd248f73-76e9-4e31-b5cb-35fd6dec4c8c)  


**Lambda Triggers** 
- You can create a Lambda function and then activate that function during user pool operations such as user sign-up, confirmation, and sign-in (authentication) with a Lambda trigger. You can add authentication challenges, migrate users, and customize verification messages.
- When you have a Lambda trigger assigned to your user pool, Amazon Cognito interrupts its default flow to request information from your function. Amazon Cognito generates a JSON event and passes it to your function. The event contains information about your user's request to create a user account, sign in, reset a password, or update an attribute. Your function then has an opportunity to take action, or to send the event back unmodified.
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/81f90980-982d-4095-a19b-63a1dd888a7d)   
- Except for Custom Sender Lambda triggers, Amazon Cognito invokes Lambda functions synchronously. When Amazon Cognito calls your Lambda function, it must respond within 5 seconds. If it doesn't and if the call can be retried, Amazon Cognito retries the call. After three unsuccessful attempts, the function times out. You can't change this five-second timeout value.

**Cognito Hosted UI**  
- Cognito has a hosted authentication UI that you can add to your app to handle sign-up and sign-in workflows
- Using the hosted UI, you have a foundation for integration with social logins, OIDC or SAML
- Can customize with a custom logo and custom CSS
- The hosted UI sign-in webpage uses the following URL format. Note the response_type. In this case, response_type=code for the authorization code grant.
- When you navigate to the /oauth2/authorize endpoint with your custom parameters, Amazon Cognito either redirects you to the /oauth2/login endpoint or, if you have an identity_provider or idp_identifier parameter, silently redirects you to your IdP sign-in page.  
```https://<your_domain>/oauth2/authorize?response_type=code&client_id=<your_app_client_id>&redirect_uri=<your_call```  

- You can view the hosted UI sign-in webpage with the following URL for the implicit code grant where response_type=token. After a successful sign-in, Amazon Cognito returns user pool tokens to your web browser's address bar.    
```https://<your_domain>/login?response_type=token&client_id=<your_app_client_id>&redirect_uri=<your_callback_url>```   

- You can find the JSON web token (JWT) identity token after the #idtoken= parameter in the response.   
Here's a sample response from an implicit grant request. Your identity token string will be much longer.     
```https://www.example.com/#id_token=123456789tokens123456789&expires_in=3600&token_type=Bearer```  

- The Amazon Cognito hosted UI doesn't support custom cross-origin resource sharing (CORS) origin policies. A CORS policy in the hosted UI would prevent users from passing authentication parameters in their requests. Instead, implement a CORS policy in the web frontend of your app.

**Tokens** 
- After your app user successfully signs in, Amazon Cognito creates a session and returns an ID, access, and refresh token for the authenticated user.
- The ID token is a JSON Web Token (JWT) that contains claims about the identity of the authenticated user, such as name, email, and phone_number
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/5817e678-72ed-467f-9c36-40b4ba9f70e8)
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/87228a79-ca34-4a62-a810-3c21e884cef5)  

- The signature of the ID token is calculated based on the header and payload of the JWT token. Before you accept the claims in any ID token that your app receives, verify the signature of the token.
- The user pool access token contains claims about the authenticated user, a list of the user's groups, and a list of scopes. The purpose of the access token is to authorize API operations.
- You can use the refresh token to retrieve new ID and access tokens. By default, the refresh token expires 30 days after your application user signs into your user pool. When you create an application for your user pool, you can set the application's refresh token expiration to any value between 60 minutes and 10 years.
- With refresh tokens, you can persist users' sessions in your app for a long time. Over time, your users might want to deauthorize some devices where they have signed in, continually refreshing their session. To sign your user out from a single device, revoke their refresh token.
- ```GlobalSignOut``` accepts a user's valid–unaltered, unexpired, not-revoked–access token. Because this API is token-authorized, one user can't use it to initiate sign-out for another user.
- You can, however, generate an ```AdminUserGlobalSignOut``` API request that you authorize with your AWS credentials to sign out any user from all of their devices.
- Before you can revoke a token for an existing user pool client, you must enable token revocation.
- For verification of JWT tokens: Verifying the Token signature (from JWK url, public, private key pair) and Verifying the token claims: exp, aud, client_id, iss etc...
- You can cache the access tokens so that your app only requests a new access token if a cached token is expired. Otherwise, your caching endpoint returns a token from the cache. This prevents an additional call to an Amazon Cognito API endpoint.
- caching proxy with API Gateway: The cache key is a combination of the OAuth scopes that you request in the scope URL parameter and the Authorization header in the request. The Authorization header contains your app client ID and client secret.   

* ALB Flow with Cognito
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/65795aa9-a593-48f1-bff4-a25f17bf5e4c)  

* ALB Flow with any OIDC ID provider 
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/3dcd424d-bd8b-4279-8bed-67717107c0d5)   

* Cognito Identity pool with Social providers (user pool)
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/ff78356a-aa88-42d7-8355-bbd8b799899c)  

* Authentication + Authorization 
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/563fda90-37f0-4f2b-bfe4-9163c84f387e)   

**Cognito Sync/AppSync**
- Amazon Cognito Sync is an AWS service and client library that makes it possible to sync application-related user data across devices. Amazon Cognito Sync can synchronize user profile data across mobile devices and the web without using your own backend.

## KMS

### How SSL/TLS works and why encryption ?

**SSL/TLS**
  - An SSL/TLS certificate is a digital object that allows systems to verify the identity & subsequently establish an encrypted network connection to another system using the Secure Sockets Layer/Transport Layer Security (SSL/TLS) protocol.
  - PKI provides a way for one party to establish the identity of another party using certificates if they both trust a third-party - known as a certificate authority.
  - A certificate authority (CA) is an organization that sells SSL/TLS certificates to web owners, web hosting companies, or businesses. The CA validates the domain and owner details before issuing the SSL/TLS certificate.  EX.  Amazon Trust Services
  - An SSL/TLS certificate has a maximum validity period of 13 months.
  - A session key maintains encrypted communication between the browser and web server after the initial SSL/TLS authentication is completed. The session key is a cipher key for symmetric cryptography. Symmetric cryptography uses the same key for both encryption and decryption.
  - Encryption in flight ensures no MITM (man in the middle attack) can happen

  ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/241f559b-e0e4-4f69-bc16-0ef80fe7e17d)

**Client-side encryption**
  - Data is encrypted by the client and never decrypted by the server
  - Data will be decrypted by a receiving client
  - The server should not be able to decrypt the data
  - Could leverage Envelope Encryption
  ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/bb3dc228-6983-4043-a5a9-a3e53146c57b)  


**Server-side encryption**
  - Data is encrypted after being received by the server
  - Data is decrypted before being sent
  - It is stored in an encrypted form thanks to a key (usually a data key)
  - The encryption / decryption keys must be managed somewhere and the server must have access to it
  ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/e7033f00-7388-4a33-b837-4cf68b920698)  
  - Able to audit KMS Key usage using CloudTrail
  - Never ever store your secrets in plaintext, especially in your code!, Encrypted secrets can be stored in the code / environment variables

**AWS KMS KEYS**

  - An AWS KMS key is a logical representation of a cryptographic key. A KMS key contains metadata, such as the key ID, key spec, key usage, creation date, description, and key state. Most importantly, it contains a reference to the key material that is used when you perform cryptographic operations with the KMS key.
  - Key material is the string of bits used in a cryptographic algorithm. Secret key material must be kept secret to protect the cryptographic operations that use it. Public key material is designed to be shared.
  - AWS KEY MATERIAL TYPES: AWS_KMS (MANAGED BY AWS), EXTERNAL (IMPORTED KEY MATERIAL FROM OUTSIDE OF AWS), AWS_CLOUDHSM (MANAGED BY AWS IN AWSCLOUDHSM CLUSTER), EXTERNAL_KEY_STORE (EXTERNAL KEY MANAGED OUTSIDE OF AWS)

**Customer Managed KMS**
  
  - The KMS keys that you create are customer managed keys. Customer managed keys (CMK) are KMS keys in your AWS account that you create, own, and manage. You have full control over these KMS keys, including establishing and maintaining their key policies, IAM policies, and grants, enabling and disabling them, rotating their cryptographic material, adding tags, creating aliases that refer to the KMS keys, and scheduling the KMS keys for deletion.
  - For customer managed keys, the value of the KeyManager field of the DescribeKey response is CUSTOMER.
  - Customer managed keys incur a monthly fee and a fee for use in excess of the free tier.

**AWS Managed KMS**

  - AWS managed keys are KMS keys in your account that are created, managed, and used on your behalf by an AWS service
  - You don't have to create or maintain the key or its key policy, and there's never a monthly fee for an AWS managed key.
  - you cannot change any properties of AWS managed keys, rotate them, change their key policies, or schedule them for deletion.
  - You can also identify AWS managed keys by their aliases, which have the format aws/service-name, such as aws/redshift
  - For AWS managed keys, the value of the KeyManager field of the DescribeKey response is AWS.
  - All AWS managed keys are automatically rotated every year. You cannot change this rotation schedule.

**Identifying AWS KMS TYPES FROM AWS CONSOLE**

![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/5314df88-c880-442f-a50e-0df294b62ba2)


**Symmetric encryption KMS keys**

  - When you create an AWS KMS key, by default, you get a KMS key for symmetric encryption
  - a symmetric encryption KMS key represents a 256-bit AES-GCM encryption key, except in China Regions, where it represents a 128-bit SM4 encryption key.
  - Symmetric encryption keys are used in symmetric encryption, where the same key is used for encryption and decryption.

**Asymmetric KMS keys**

  - An asymmetric KMS key represents a mathematically related public key and private key pair.
  - The private key never leaves AWS KMS unencrypted. To use the private key, you must call AWS KMS. You can use the public key within AWS KMS by calling the AWS KMS API operations, or you can download the public key and use it outside of AWS KMS
  - You can create asymmetric KMS keys that represent RSA key pairs or SM2 key pairs (China Regions only) for public key encryption or signing and verification, or elliptic curve key pairs for signing and verification.

**HMAC KMS key (symmetric)**

  - Represents a symmetric key of varying length that is used to generate and verify hash-based message authentication codes. The key material in an HMAC KMS key never leaves AWS KMS unencrypted. To use your HMAC KMS key, you must call AWS KMS.

**Identifying types of keys from AWS console**

  ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/f3f78c4e-3918-4906-af28-3648cacde925)    
  ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/dd1e112c-9b7b-451b-a0d7-c0a959dd0bda)  

  ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/0b60a769-cfe0-4374-a5ac-b0c6aa6d63a5)  
  ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/df4bfbf5-0258-4864-ab7c-e331911ef7cd)  
  ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/0ed4c08a-4f29-4f82-8002-083bf17a6d0a)   
  ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/4f8facb3-6eb9-40c8-b673-5e8dbe8accc1)   
  ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/e8aece59-4156-4842-9d21-5975d922c799)

  ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/7774e03e-9168-4411-bd5b-210c308c6e36)     
  ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/8c13ed49-e161-4d96-9fe9-8b16e2cebbf3)  
  ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/ed86712a-1f58-47b5-aee3-808743e1e4ef)  

  - To determine whether a KMS key is symmetric or asymmetric, use the DescribeKey operation. The KeySpec field in the response contains the key spec of the KMS key. For a symmetric encryption KMS key, the value of KeySpec is SYMMETRIC_DEFAULT. Other values indicate an asymmetric KMS key or an HMAC KMS key.

**Use Cases for choosing types of Keys** 

  - Encrypt and decrypt data: If your use case requires encryption outside of AWS by users who cannot call AWS KMS, asymmetric KMS keys are a good choice. Otherwise Symmetric keys are good (fast, efficient, and assures the confidentiality and authenticity of data).  
  - Sign messages and verify signatures: To sign messages and verify signatures, you must use an asymmetric KMS key.  
  - Perform public key encryption: To perform public key encryption, you must use an asymmetric KMS key with an RSA key spec or an SM2 key spec (China Regions only). To encrypt data in AWS KMS with the public key of a KMS key pair, use the Encrypt operation. You can also download the public key and share it with the parties that need to encrypt data outside of AWS KMS.
  - Generate and verify HMAC codes: To generate and verify hash-based message authentication codes, use an HMAC KMS key.
  - Use with AWS services: AWS services that encrypt your data require a symmetric encryption KMS key..

**Rotating Keys**

  - ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/bba38650-bef0-45e0-b5f5-c3d42b9aeff0)
  - To create new cryptographic material for your customer managed keys, you can create new KMS keys, and then change your applications or aliases to use the new KMS keys. Or, you can enable automatic key rotation for an existing KMS key.
  - However, automatic key rotation has no effect on the data that the KMS key protects. It does not rotate the data keys that the KMS key generated or re-encrypt any data protected by the KMS key, and it will not mitigate the effect of a compromised data key.
  - AWS KMS supports automatic key rotation only for symmetric encryption KMS keys with key material that AWS KMS creates.
  ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/824d4f69-f11d-460d-9040-b427eae437a5)   

**Policies and Access control for AWS KMS**

  - Default KMS Key Policy: Complete access to the key to the root user = entire AWS account  
  ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/2fbb1b90-6ecb-4e00-8ff6-54e21cf998c5)   

  - No AWS principal has any permissions to a KMS key unless that permission is provided explicitly and never denied.
  - AWS KMS resource policies for KMS keys are called key policies. All KMS keys have a key policy.
  - Combination of all can be used: Key policy, IAM policy, grants
  - EX. ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/6ca48749-af37-4a6d-aeb8-1324edc7d9c7)  
  ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/059f6a29-1031-45dd-be09-fd19e110c256)
  - Above ex. description:   
  - Allows the example AWS account, 111122223333, full access to the KMS key. It allows the account and its administrators, including the account root user (for emergencies), to use IAM policies in the account to allow access to the KMS key.
  - Allows the ExampleAdminRole IAM role to administer the KMS key.
  - Allows the ExampleUserRole IAM role to use the KMS key.

  - You can allow users or roles in a different AWS account to use a KMS key in your account. Cross-account access requires permission in the key policy of the KMS key and in an IAM policy in the external user's account.
  - The key policy for the KMS key must give the external account (or users and roles in the external account) permission to use the KMS key. The key policy is in the account that owns the KMS key.
  ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/4af1be4e-81ee-4c15-ac86-3b13a3289aae)  

  - IAM policies in the external account must delegate the key policy permissions to its users and roles. These policies are set in the external account and give permissions to users and roles in that account.
  ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/e11ade5c-f04f-422d-b2fa-782f02e824ec)  

  - Use case example   
  ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/cb4939d5-48c3-4136-85a8-e5b7fd3a1030)  

**Using KMS with AWS services**

  - Amazon S3 integrates with AWS Key Management Service (AWS KMS) to provide server-side encryption of Amazon S3 objects. Amazon S3 uses AWS KMS keys to encrypt your Amazon S3 objects.
  - Secrets Manager integrates with AWS Key Management Service (AWS KMS) to encrypt every version of every secret value with a unique data key that is protected by an AWS KMS key. This integration protects your secrets under encryption keys that never leave AWS KMS unencrypted.
  - With encryption at rest, DynamoDB transparently encrypts all customer data in a DynamoDB table, including its primary key and local and global secondary indexes, whenever the table is persisted to disk. 

**Region Snapshots in KMS**
  - KMS Keys are region scoped, for ex. EBS volumes encrypted with KMS keys in a region if needs to be copied snapshots to another region, then following needs to be done
    - Copy the EBS volume encrypted to another region which means AWS will re-encrypt the new snapshot with a different key as same key can't be used in two different regions.  
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/30457b92-4c8f-45df-8008-761ecffdd7ae)   
  
**ENCRYPT AND DECRYPT API**
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/b50c31a4-ad61-46e2-a544-a38eb4173a15)   

```aws kms encrypt --key-id alias/tutorial --plaintext fileb://ExampleSecretFile.txt --output text --query CiphertextBlob  --region eu-west-2 > ExampleSecretFileEncrypted.base64```  
```cat ExampleSecretFileEncrypted.base64 | base64 --decode > ExampleSecretFileEncrypted```   
```aws kms decrypt --ciphertext-blob fileb://ExampleSecretFileEncrypted   --output text --query Plaintext > ExampleFileDecrypted.base64  --region eu-west-2```  
```cat ExampleFileDecrypted.base64 | base64 --decode > ExampleFileDecrypted.txt```   

**ENVELOPE ENCRYPTION**
- since KMS has upper limit of 4KB data for encrypt, anything over 4 KB of data that needs to be encrypted must use the Envelope Encryption
- The key used to encrypt data itself is called a data encryption key (DEK).
- The DEK is encrypted (also known as wrapped) by a key encryption key (KEK). The process of encrypting a key with another key is known as envelope encryption.
- Encryption and Decryption is done on client side with help of DEK and KEK.
- Flow of this encryption with new API
- ```GenerateDataKey``` API: This operation returns a plaintext copy of the data key and a copy that is encrypted under a symmetric encryption KMS key that you specify.
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/8ba97d87-5bbc-4f4b-b556-cc49fa9a3da3)
- ```Decrypt``` API: 
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/63471ed4-5638-4922-bac7-6fc477e495e0)
- ```GenerateDataKeyWithoutPlaintext``` API: GenerateDataKeyWithoutPlaintext is identical to the GenerateDataKey operation except that it does not return a plaintext copy of the data key. This operation is useful for systems that need to encrypt data at some point, but not immediately.
- ```GenerateRandom``` API : Returns a random byte string that is cryptographically secure.
You must use the NumberOfBytes parameter to specify the length of the random byte string. There is no default value for string length.

**Encryption SDK**
- The AWS Encryption SDK is a client-side encryption library designed to make it easy for everyone to encrypt and decrypt data
- Data key caching stores data keys and related cryptographic material in a cache. When you encrypt or decrypt data, the AWS Encryption SDK looks for a matching data key in the cache. If it finds a match, it uses the cached data key rather than generating a new one. Data key caching can improve performance, reduce cost, and help you stay within service limits as your application scales.
- TradeOff between security and cost/usage
- Uses LocalCryptoMaterialsCache(max age, max bytes, max number of messages)
- Once installed SDK, commands with ```aws-encryption-cli``` can be used to perform encryption and decryption on client-side.

**How to manage KMS Request Quotas**
- They vary based on region and type of CMK (like symmetric or assymetric) used in the request. It can be shared for one account across the regions.
- Use exponential backoff
- Use envelope encryption To reduce calls 
- Request a increase quota when experiencing ThrottlingException 400 bad requests, via API or Support Request to AWS.

**How to Encrypt secrets used in the code**
- For ex. DB passwords injected via environment variable can be encrypted
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/ef7a5bb0-9280-4657-9e6e-5f956937fd90)
- LAMBDA FUNCTION WITH KMS

**S3 Bucket SSE-KMS**
- Example of envelope encryption and how to avoid lot of KMS calls and high bills at scale -> S3 bucket keys which generates lot of data keys and encrypt the data , reducing the direct calls to KMS
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/19e9446b-4930-45bb-b5a6-60b137a3c4bd)
- less KMS CloudTrail events in CloudTrail
- server-side encryption
- request costs by up to 99 percent

**CloudWatch logs encryption with KMS**
- Encryption can be enabled at log-group level by associating a CMK with log-group level via cloudwatch logs API (can't be done from console).

## CloudHSM (hardware security modules)
- Generate and use cryptographic keys on dedicated FIPS 140-2 Level 3 single-tenant HSM instances.
- can be Integrated with KMS with option of custom key store
- Highly available via CLOUDHSM clusters deployed across the regions
- You do not use AWS Identity and Access Management (IAM) users or IAM policies to access resources within your cluster. Instead, you use HSM users directly on HSMs in your AWS CloudHSM cluster.
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/8f7455cd-14d4-462c-ab1e-d33ae950161c)  
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/55dbd00b-82ec-4704-9d33-c17c0838d68c)
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/7bbb31e2-1149-4d22-93e7-41475261bdc1)  

![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/0ea04f5b-c9df-4969-918c-baf72ef19893)
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/d003f129-8bde-4d20-989d-c2a6ffb231fb)

## SSM (simple systems manager) Parameter store 
- provides secure, hierarchical storage for configuration data management and secrets management 
- You can store data such as passwords, database strings, Amazon Machine Image (AMI) IDs, and license codes as parameter values. You can store values as plain text or encrypted data
- You can reference Systems Manager parameters in your scripts, commands, SSM documents, and configuration and automation workflows by using the unique name that you specified when you created the parameter.
- You can configure change notifications and invoke automated actions for both parameters and parameter policies. These events are recieved by EventBridge.
- Parameter Store is integrated with AWS Secrets Manager so that you can retrieve Secrets Manager secrets
- Parameter Store provides support for three types of parameters: String (any text data), StringList(comma separated list), and SecureString (ecnrypted confidential data such as passwords etc..) 
  ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/e306abf1-1fb1-4c53-93c1-af7767df3af5)
- You restrict access to AWS Systems Manager parameters by using AWS Identity and Access Management (IAM). More specifically, you create IAM policies that restrict access
- You can change a standard parameter to an advanced parameter at any time, but you can’t revert an advanced parameter to a standard parameter. This is because reverting an advanced parameter to a standard parameter would cause the system to truncate the size of the parameter from 8 KB to 4 KB, resulting in data loss.
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/325e1849-f858-4a59-87eb-70cf34226dec)
- EventBridge can be configured via EventBridge rule that invokes a target based on events that happen to one or more parameters in your AWS account
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/ba112f04-3d92-4979-b29c-3a44204d021d)

- For ex. When you create an advanced parameter, you specify when a parameter expires, when to receive notification before a parameter expires
- how long to wait before notification should be sent that a parameter hasn't changed

- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/1501a98e-e18f-4348-969a-4ab756400944)
- In the lambda functions, we can simply use ```boto3``` client library to use SSM and call its methods to read the secrets directly from SSM store and avoid hardcoding the credentials. Note: lambda function will also require permissions via IAM to read/update/delete parameters in parameter store.
- For ```SecureString``` string type, we can use flag ```withDecryption=True``` and permissions to access KMS keys, lambda function will be able to also decrypt the value stored in parameter store.

## Secrets manager 
- Best place to store secrets like DB credentials, Oauth Tokens, certificates etc.. similar to hashicorp Vault.
- Force rotation of secrets
- Generation of secrets can be done on rotation (via lambda)
- Ex. rotate AWS RDS DB credentials
- A secret has versions which hold copies of the encrypted secret value. When you change the secret value, or the secret is rotated, Secrets Manager creates a new version
- Secrets are encrypted with KMS (mandatory)
- Multi region replication for secrets for disaster recovery
- Since the credentials are no longer stored with the application, rotating credentials no longer requires updating your applications and deploying changes to application clients.
- A secret contains JSON key value pairs + metadata about the secret like ARN, a description, a resource policy, and tags etc...
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/495f8a7b-38e6-41de-b1f6-461ede00c9f0)  
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/11d57115-77b3-4c21-a6da-f7b5fa5d1c93)
- Code can directly access the secrets from secret manager by assuming the IAM role ```RoleToRetrieveSecretAtRuntime```
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/eac80c50-e9bd-4acb-8ffa-5fc91b4b98df)
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/33cf0ae5-e1a7-4448-b2f8-d92366a4d038)
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/fdb8e0af-c2f0-488f-8c85-6615c264214a)
- Can be integrated with CloudFormation templates where it can be entirely managed by for ex. RDS DB including rotation mechanism or it can be generated by us in template and dynamically referenced in RDS resource (very similar to helm charts).
  - ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/ee077bd6-2215-4b7b-b068-5c1c62f02972)
  - ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/fb1d280d-e66d-4658-9d15-2c59dd902d26)   
 
- From ```CodeBuild``` environment, we can configure environment variables including secrets and specify it to be fetched from secrets managed, SSM Parameter store etc...

## AWS Nitro Enclaves
- AWS Nitro Enclaves is an Amazon EC2 feature that allows you to create isolated execution environments, called enclaves, from Amazon EC2 instances. Enclaves are separate, hardened, and highly-constrained virtual machines.
- They provide only secure local socket connectivity with their parent instance. They have no persistent storage, interactive access, or external networking
- Process highly sensitive data in an isolated compute environment: Personally Identifiable Information (PII), healthcare, financial, secure MUlti party computations etc...
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/66d272cc-081a-4ca0-ac89-fb01485b88ec)
- Nitro Enclaves also supports an attestation feature, which allows you to verify an enclave's identity and ensure that only authorized code is running inside it. Nitro Enclaves is integrated with the AWS Key Management Service

## Sanitizing Sensitive data
- Data containing any PII (Personally identifiable information) should be sanitized i.e. encrypted which can be done at various levels.
- For ex. while entering the requests from cloudFront servers, lambda function can intercept the requests and perform encryption of sensitive fields or entire payload and then decrypt while returning back the same information (field level encryption).
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/9bddd570-c765-407c-97c0-540bd526ee60)
- ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/50314467-634e-4f4f-a50d-9a2d5a2fb707)


## AWS Certificate management**  
- AWS Certificate Manager (ACM) handles the complexity of creating, storing, and renewing public and private SSL/TLS X.509 certificates and keys that protect your AWS websites and applications.
- A certificate authority (CA) is an entity that issues digital certificates. The CA issues signed digital certificates that affirm the identity of the certificate subject and bind that identity to the public key contained in the certificate. A CA also typically manages certificate revocation.
- A public key infrastructure (PKI) consists of hardware, software, people, policies, documents, and procedures that are needed to create, issue, manage, distribute, use, store, and revoke digital certificates.
- A certificate authority (CA) typically exists within a hierarchical structure that contains multiple other CAs with clearly defined parent-child relationships between them. Child or subordinate CAs are certified by their parent CAs, creating a certificate chain. The CA at the top of the hierarchy is referred to as the root CA, and its certificate is called the root certificate. This certificate is typically self-signed.

**AWS Public certificates**
- This service is for enterprise customers who need a secure web presence using TLS. ACM certificates are deployed through Elastic Load Balancing, Amazon CloudFront, Amazon API Gateway
- ACM certificates are X.509 SSL/TLS certificates that bind the identity of your website and the details of your organization to the public key that is contained in the certificate. ACM uses your AWS KMS key to encrypt the private key.

**AWS PRIVATE CA**
- This service is for enterprise customers building a public key infrastructure (PKI) inside the AWS cloud and intended for private use within an organization.
- you can create your own certificate authority (CA) hierarchy and issue certificates with it for authenticating users, computers, applications, services, servers, and other devices.
- Certificates issued by a private CA cannot be used on the internet.

![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/0a7c3a07-c61d-4831-8f48-ff0ab5331181)


**To generate an SSH key pair, run the command ssh-keygen.**
```ssh-keygen```
  - Generate a CSR: ```openssl req –out certificatesigningrequest.csr -new -newkey rsa:2048 -nodes -keyout privatekey.key```
  - Decode CSR: ```openssl req -in server.csr -noout –text```
  - Generate CSR For existing private key: ```openssl req -out CSR.csr -key privateKey.key -new```
  - Generate a CSR for an Existing Certificate and Private Key: ```openssl x509 -x509toreq -in certificate.crt -out CSR.csr -signkey privateKey.key```
  - Generate Self signed certificate: ```openssl req -newkey rsa:2048 -nodes -keyout domain.key-x509 -days 365 -out domain.crt```


# Deployment

## ELASTIC BEANSTALK

## CLOUFORMATION 

## AWS CI/CD 


# Troubleshooting and Optimization

## CLOUDWATCH

## X-RAY

## CLOUTRAIL 
