# Current State - Technical Environment

These notes describe the "current state" of our organization. 

This one specifically details the technical environment, including:

* The type of software products being created and maintained by Engineering teams
* The source code repositories
* The enivornments used and their purposes (e.g. Development, Staging, Production)

## Current code bases that form product

### A total of 60 code repositories
* One primary legacy solution based on forms builder that runs on windows server
* Around 40x micro-services
* Around 15x repos for "toolbox plugins" that extend the toolbox microservice
* Around 5x code repositories for platform engineering (i.e. terraform)

## Current environment setup

* All environments are setup on AWS Cloud
* Each environment is setup under its own AWS Account

### Production Environment

* Managed via click-ops (no Terraform or automated provisioning of resources)

### Staging Environment

* Relatively new and not yet fully utilised by Engineering squads
* Has the latest patterns for setting up resources using Terraform

### UAT Environment

* Used for conducting user acceptance testing by customers during onboarding projects
* Requires specific data setup to support UAT test cases and scenarios
* Delays deployments to production UNTIL testing has passed and signed off by customers

### ENG Environment

* The primary development environment
* Has 7x different sub-environments
* ENG-1 is the primary integrated environment
* Others used for performance/load testing

Based on the content of the CPAISPP Confluence space and related documentation, the following AWS resources and services are in use:

---

## Core AWS Resources and Services

**1. Compute & Containerization**
- **EC2 (Elastic Compute Cloud)**
- **ECS (Elastic Container Service) / Fargate**: Used for running containerized applications without server management.

**2. Databases & Storage**
- **Amazon RDS (PostgreSQL)**
- **Amazon Aurora (PostgreSQL-compatible)**
- **Amazon Redshift**
- **Amazon S3 (Simple Storage Service)**
- **Amazon DynamoDB**
- **Amazon EFS (Elastic File System)**

**3. Networking & Security**
- **Application Load Balancer (ALB)**
- **AWS WAF (Web Application Firewall)**
- **VPC (Virtual Private Cloud)**
- **Security Groups**
- **Route 53 (DNS management)**

**4. Data & Analytics**
- **AWS Glue**: For ETL jobs, data cataloging, and data discovery.
- **Amazon Kinesis**: For real-time data streaming.

**5. Caching & Messaging**
- **Amazon ElastiCache (Redis)**

**6. Identity & Secrets Management**
- **AWS Secrets Manager**: For secure storage and retrieval of secrets.
- **Microsoft Entra ID (via SAML 2.0 for SSO)**

**7. Monitoring & Observability**
- **Datadog**: For monitoring, APM, and logging.

**8. Infrastructure as Code**
- **Terraform**: Used to provision and manage AWS resources.

### Account Structure & Environments

- **Three AWS Accounts**: Engineering (Master), UAT, and Production, with resources distributed across Singapore and Sydney regions.
- **Shared Resources**: Some resources (e.g., mail, Redshift, Aurora, logging databases) are shared across accounts.

### Additional AWS-Related Components

- **CloudMap/Mesh**: For service discovery (in some environments).
- **AWS Glue Resource Types**: Catalog databases, tables, partitions, classifiers, jobs, triggers, workflows, crawlers, connections, security configurations, dev endpoints.
