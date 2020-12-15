## Services:
#### Compute
* `EC2` (Elastic Compute Cloud) - Virtual private servers (VPS)
    * `EC2 Spot Instances` - huge discount, but EC2 can reclaim the capacity at any moment. Anything you run here - should be fault-tolerant
    * `EBS` (Elastic Block Store) - Storage for EC2
    * `AMI` (Amazon Machine Images) - OS + installed software
    * `ELB` (Elastic Load Balancing) - distributes incoming application traffic across multiple targets (e.g. EC2 instances), performs health checks
* `Elastic Beanstalk` (`PaaS`, runs on `EC2`) - installed runtime, configured reverse proxy (80 -> 8080), load balancer, monitoring
* `Lambda` - takes care of everything required to run and scale your code, you pay only when code is executing
* `Amplify` - hosting for fullstack SPA with CI/CD
* `ECS` (Elastic Container Service) - containers orchestration, simple version of `EKS`
    * `Fargate` - Serverless compute for containers
* `EKS` (Elastic Kubernetes Service) - Kubernetes as a Service, complex and flexible version of `EKS`
* `Lightsail` - Servers with sane defaults, fixed price per month
#### Storage
* `S3` (Simple Storage Service) - File storage
    * `S3 Glacier` - low cost file storage with very slow retrieval (usable for backups)
* `RDS` (Relational Database Service) - Set up, operate, and scale a relational database (Postgres/MySQL)
    * `Aurora` - fully managed alternative (you don't have to admin it)
    * `Aurora Serverless` - only runs when you need it, like Lambda (for bursty workloads that spike frequently)
* `DynamoDB` - Key-value storage (NoSQL)
    * `DocumentDB` - same thing, but with more complexity/control
* `Elasticache` - in-memory data store (Memcached/Redis)
#### Devops
* `CloudFormation` - Infrastructure as Code (declarative, high level of abstraction)
    * `Quick Starts` - gold-standard deployment templates
    * Alternatives:
        * `CDK` (Cloud Development Kit) - abstraction on top of CloudFormation
        * `CLI` - imperative, low level of abstraction
        * `Terraform`
* `OpsWorks` - use code to automate the configurations of your `EC2` servers (via Chef/Puppet)
* `Marketplace` - pre-packaged images with installed software (e.g. SonarQube, Grafana)
* `CloudWatch` - Application and Infrastructure Monitoring (Logs, Metrics, Alarms, Dashboards, KPIs)
* `CloudTrail` - monitor actions across your AWS infrastructure (e.g. who created that `EC2` instance? who deleted DB?)
* `CodeCommit` - hosted version control (github/gitlab)
* `CodeDeploy` - deploy code from git to `EC2` instances
* `CodePipeline` - CI/CD (CircleCI, Travis)
#### Networking
* `Route 53` - DNS + Domains
* `CloudFront` - CDN (Content Delivery Network)
* `VPC` (Virtual Private Cloud) - logical network which you can provision resources into
* `API Gateway` - versioning and routing, rate limiting, API keys
#### Analytics
* `AWS Cost Explorer` - Visualize, understand, and manage your AWS costs and usage
* `AWS Cost & Usage Report` - In depth AWS costs and usage
* `Trusted Advisor` - scans AWS infrastructure, compares it to best practices, and provides recommendations
#### Messages
* `SQS` (Simple Queue Service) - Message queue (RabbitMQ)
* `SNS` (Simple Notifications Service) - send notifications to subscribers (e.g. via email/sms/http)
#### Security, identity
* `IAM` (Identity and Access Management) - AWS Account management (users, groups, permissions)
    * `ARN` (Amazon Resource Names) - identifiers for resources
* `KMS` (Key Management Service) - create, store, audit usage of cryptographic keys
* `Cognito` - Add Sign-up/Sign-in functionality to the app
* `Inspector` - security audit for `EC2` instances
* `WAF` (Web Application Firewall) - Blocks incoming requests, based on rules (e.g. by ip, by content)
    * Stands in front of API Gateway/ELB/CloudFront
* `Shield` - DDoS protection. `Route53`/`CloudFront` -> `Shield` -> `VPC`
* `GuardDuty` - IDS/IPS (Intrusion Detection System / Intrusion Protection System)
    * e.g. detects when somebody bruteforces password for your `EC2` instance
#### Cost management
* `Budgets` - Before costs incurred. Alerts, limits, forecasting
* `Cost Explorer` - After costs incurred. Reports, visualization
* `Pricing Calculator` - Estimate the cost for your architecture solution
* `Resource Groups` - check all your resources (EC2 instances, Lambda functions, DynamoDB tables etc)
#### Development
* `Cloud9` - Online IDE
* `Honeycode` - Create apps without programming
* `SDK` - Access AWS services from your app (e.g. write data to DynamoDB)