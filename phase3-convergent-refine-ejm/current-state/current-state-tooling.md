# Current State - Tooling

These notes describe the "current state" of our organization. 

This one specifically details the current software, services, and tools used by the teams.

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
* Datadog - Application and infrastructure monitoring and observability
* Visual Studio 2022 - IDE for local development
* VS Code - IDE used by some Engineers in addition to Visual Studio 2022

### New tools currently being implemented and adopted

* Atlassian Compass - Service catalog and internal developer portal
* Sonarqube - Static analysis, coding standards, and security scanning

Based on the content from the ICT Confluence space, the following software tools are used or referenced across development, operations, communication, and project management:

### Development & Source Control
- **.NET Core & .NET Framework**: Core frameworks for application development.
- **Bitbucket**: Source control, code collaboration, and CI/CD (via Bitbucket Pipelines).
- **Jenkins**: Automation server for managing builds and CI/CD workflows.
- **Octopus Deploy**: Deployment automation tool for managing releases and deployments.
- **ECS Fargate**: Container orchestration for running containerized applications.

### Cloud & Infrastructure
- **AWS (Amazon Web Services)**: Primary cloud provider for scalable infrastructure.

### Monitoring & Observability
- **Datadog**: Monitoring and observability platform for application and infrastructure metrics.

### Project Management & Collaboration
- **Jira**: Project management, issue tracking, and backlog management.
- **Confluence**: Documentation, requirements gathering, and stakeholder communication.
- **Aha!**: Roadmapping and prioritization, especially for technology roadmaps and tech debt management.

### Testing Frameworks
- **Unit Testing**: xUnit
- **Integration Testing**: None currently
- **End-to-End Testing**: Playwright
- **Performance Testing**: Unknown
- **Security Testing**: SonarQube

### Code Quality Tools
- **Static Analysis**: SonarQube, want to use linting tools and check in CICD pipelines
- **Code Formatting**: Want to use Prettier or similar tools, not currently checked in CICD pipelines
- **Security Scanning**: SonarQube, formerly Snyk
- **Dependency Management**: None, want to adopt tooling for this

### Documentation Systems
- **Knowledge Management**: Confluence
  - **Organization**: Currently scattered across various Confluence spaces
  - **Search**: Search in Confluence is ok, now have Atlassian Rovo available
  - **Maintenance**: Generally well documented, but not organized well

- **API Documentation**: Swagger
  - **Accuracy**: Unknown
  - **Usability**: Each microservice has API endpoint using Swagger available
  - **Integration**: Can be better integrated into Integration testing

### Communication
- **Microsoft Communication Application**: Referenced for team and project communication.
