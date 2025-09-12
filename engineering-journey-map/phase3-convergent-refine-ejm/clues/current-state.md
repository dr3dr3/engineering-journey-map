# Current State

These notes describe the "current state" being the current business processes, tools and applications in use, and the "work to do" that has already been identified as needed. 

To progress from the current state to the desired future state requires a series of iterative steps to be taken, as opposed to a giant leap. Therefore, they act as a constraint on getting to the desired state, by limiting the actions that are feasible and realistic to take now.

## Current teams

### An engineering team comprised of 25 people
* The engineering team is comprised of 5 "squads" or teams
* Four of these teams are focused on feature development for our products
* The fifth team is focused on reactive work such as urgent bugs and production issues

### A platform team comprised of 3 people
* Focus on platform engineering and enabling devops practices
* Wanting to adopt platform-as-a-product approach (product management approach in creaing platform services to be used by engineering and IT operations teams)
* Skilled in CI/CD pipelines, Terraform, and AWS cloud engineering

### An IT operations team comprised of 10 people
* Focused on supporting production systems
* Also focused on supporting internal users (i.e. tech support for the employees)
* Very little software engineering or cloud engineering skills

### An architecture team comprised of 2 people
* 1x lead architect
* 1x solutions architect

## Current code bases that form product

### A total of 60 code repositories
* One primary legacy solution based on forms builder that runs on windows server
* Around 40x micro-services
* Around 5x code repositories for platform engineering (i.e. terraform)

## Current tools used

* BitBucket - For source code repositories
* BitBucket pipelines - For CI/CD pipelines
* Jira - For managing engineering work and sprints
* Jira - For issue tracking
* Aha - For product management and prioritization
* Confluence - For documentation and knowledge repository
* Azure Entra - Identity and access management
* AWS IAM - Access to AWS resources
* AWS - Cloud infrastructure, used for the product tech stack resources
* Playwright - End-to-end testing
* TestRail - Test case management
* Microsoft Teams - Collaboration tool
* Microsoft Outlook - Calendar and meetings
* Fellow.app - AI meeting notes, meeting recordings, and transcripts
* Datadog  - Application and infrastructure monitoring and observability
* Visual Studio 2022 - IDE for local development
* VS Code - IDE used by some Engineers in addition to Visual Studio 2022

### New tools currently being implemented and adopted

* Atlassian Compass - Service catalog and internal developer portal
* Sonarqube - Static analysis, coding standards, and security scanning

## Current environment setup

* All environments are setup using AWS Cloud
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


## Current challenges

### High reliance on manual testing
* Every feature developed requires some level of manual testing
* Every sprint has a lot of testing effort at the end to get everything completed
* Releasing changes to production is difficult due this all this manual testing effort
* This encourages changes to be batched into bigger change sets
* Which increases the risk for each deployment to production
* There is a lot of effort (and time) to do manual regression testing

### Non-production environments are not like production environment
* Data in non-production environments is not similar enough to what is in production
* This means testing does not reflect production scenarios
* There is a lot of effort (and time) to manually create data needed for testing
* Configuration tested does not cover all the various configurations in production
* Intermittent issues are proving to be difficult to replicate and resolve

### Triaging issues is difficult
* Reproducing production issues is difficult in lower environments
* Especially when non-production environments are not the same as production
* A lot of effort and time is spend on analysing and finding causes for issues

### Too much customisation for customers
* We have multiple customised instances in production for specific customers
* This makes testing more challenging, as those customisation also need to be tested
* It makes deployments more difficult, as need to deploy code changes to multiple targets
* Has resulted in rollbacks due to incorrect deployments and issues not covered in testing

### Stories in Jira are too large
* The engineering teams are finding stories (features) are too large to complete in a sprint
* They are struggling with how to slice stories into smaller ones
* They are finding hidden complexity once the begin work on features

### A lot of capacity is allocated to bug issues
* Over half the capacity of engineering teams is used on fixing bugs and issues
* The quality of code released is not enough to prevent new issues
* There is too much effort to ensure quality due to the manual effort and time to do testing
* Urgent issues (considered reactive work) is disrupting the teams planned work