# Desired State

These notes describe the "desired state" representing the current priorities and work in progress for improvements to business processes, tooling, and capabilities. These initiatives must be reflected in the engineering journey map under the Opportunities section and serve as the foundation for our organizational transformation roadmap.

## Environments

**Strategic Goal:** Achieve infrastructure-as-code maturity with scalable, cost-effective, and consistent environment management.

**Infrastructure as Code (IaC):**
* Provision environments from scratch fully using Terraform with complete reproducibility
* Prove this approach in the Staging environment first, by fully destroying all resources and setting them up fresh solely using Terraform
* Subsequently set up fresh environments for UAT and Development (replacing existing ENG environments)
* Establish version control for infrastructure configurations to enable rollback capabilities

**Ephemeral Environments:**
* Explore the potential for ephemeral environments that are spun up for each engineering squad (enabling isolated testing) and destroyed after testing is complete once code is merged to trunk
* Implement automated environment lifecycle management to reduce manual overhead
* Enable developers to create feature-branch environments for testing complex changes

**Cost Optimization:**
* Implement environments that only run when needed and scale down when not in use to save infrastructure costs
* Establish automated scheduling for non-production environments (e.g., shut down overnight and weekends)
* Monitor and report on infrastructure cost savings achieved through optimization initiatives

## Automated Testing

**Strategic Goal:** Transform from manual-heavy testing to a comprehensive automated testing strategy that enables fast feedback and continuous delivery.

**Test Automation Coverage:**
* Eliminate manual testing effort, except for some limited exploratory testing and usability validation
* Achieve 100% automation of regression test cases using Playwright for end-to-end testing and comprehensive test automation for integration/contract testing and unit testing
* Implement the testing pyramid approach: extensive unit tests, focused integration tests, and targeted end-to-end tests
* Establish automated accessibility testing to ensure compliance with web standards

**Performance and Feedback:**
* Enable frequent automated test execution with fast completion times to provide rapid feedback to engineers
* Implement parallel test execution to reduce overall test suite runtime
* Establish clear test failure reporting and remediation processes
* Integrate automated testing into CI/CD pipelines for immediate feedback on code changes

**Quality Outcomes:**
* Improve test coverage and overall quality of code deployed through comprehensive automation
* Reduce time-to-market by eliminating manual testing bottlenecks
* Enable confidence in more frequent deployments through reliable automated validation

## Test Data Management

**Strategic Goal:** Establish comprehensive test data management practices that ensure realistic testing scenarios while maintaining data privacy and security.

**Data Provisioning:**
* Automate the process of safely migrating data from Production environment into lower environments, including Staging and Development
* Implement data masking and anonymization techniques to protect sensitive customer information
* Establish automated data refresh schedules to keep non-production environments current

**Synthetic Data Generation:**
* Automate the generation of synthetic test data needed for automated test cases
* Create data generation patterns that reflect real-world usage scenarios and edge cases
* Develop reusable data templates for common testing scenarios

**Environment Parity:**
* Ensure non-production environments are more reflective of the production environment in terms of data volume, variety, and complexity
* Maintain sufficient test data to cover various configurations used by different customer segments
* Implement data validation processes to ensure test data quality and consistency

## Monitoring

**Strategic Goal:** Implement comprehensive observability practices that enable proactive issue detection and foster collaboration between Engineering and Operations teams.

**Observability Strategy:**
* Involve Engineers in creating application/service observability monitoring and dashboards to ensure developer-friendly tooling
* Establish unified observability platforms where Engineering and IT Operations use the same monitoring and dashboards
* Implement the three pillars of observability: metrics, logs, and traces for comprehensive system visibility

**Logging Standards:**
* Standardize logging levels and formats consistently across all applications and services
* Implement structured logging to enable better searchability and analysis
* Limit error-level logging to only errors that require immediate resolution, reducing noise and alert fatigue
* Establish log retention policies and cost-effective log storage strategies

**Proactive Monitoring:**
* Implement Service Level Indicators (SLIs) and Service Level Objectives (SLOs) for critical business functions
* Establish automated alerting based on business impact rather than just technical metrics
* Create runbooks and automated remediation for common issues

## Technical Debt ("Tech Debt")

**Strategic Goal:** Systematically manage and reduce technical debt to improve development velocity and system maintainability.

**Debt Management:**
* Identify and manage tech debt items in Jira with standardized templates and categorization
* Maintain a comprehensive inventory of tech debt items to highlight their volume and business impact
* Implement a scoring system that considers factors like risk, effort, and business value

**Prioritization Framework:**
* Establish a systematic way to prioritize tech debt so we can focus on eliminating items with the most impact
* Create decision-making frameworks that balance tech debt remediation against new feature development
* Develop business cases that clearly articulate the value proposition of tech debt reduction

**Organizational Alignment:**
* Establish processes to escalate the importance and value of tech debt remediation compared to new feature development
* Allocate dedicated capacity (e.g., 20% of sprint capacity) for tech debt reduction
* Create visibility dashboards that show tech debt trends and remediation progress to stakeholders

## Better Alignment Between Engineering and IT Operations Teams

**Strategic Goal:** Foster a DevOps culture that breaks down silos and enables shared responsibility for system reliability and performance.

**Cross-Team Knowledge Sharing:**
* Enable IT Operations teams to be more familiar with code changes being deployed through improved documentation and communication processes
* Implement regular cross-team meetings and knowledge transfer sessions
* Establish shared documentation and runbooks accessible to both teams

**Shared Responsibility Model:**
* Encourage Engineering teams to take more responsibility for production performance and system reliability
* Implement "you build it, you run it" principles where appropriate
* Establish clear escalation paths and shared on-call responsibilities

**Communication and Feedback:**
* Establish faster feedback mechanisms to Engineering teams regarding production issues
* Implement automated notification systems for deployment-related incidents
* Create post-incident review processes that involve both Engineering and Operations

**Collaborative Prevention:**
* Improve collaboration between Engineering and IT Operations in preventing production issues
* Implement shared monitoring and alerting systems
* Establish joint capacity planning and performance optimization initiatives

## Smaller Work Items That Are More Clearly Defined

**Strategic Goal:** Improve development predictability and flow through better work decomposition and story slicing practices.

**Work Decomposition:**
* Break down work into smaller items that can be completed in a few days (ideally 1-3 days)
* Implement story mapping techniques to visualize user journeys and identify natural break points
* Establish clear definition-of-done criteria for all work items

**Team Capabilities:**
* Improve the capabilities of Engineering teams to slice stories and work into smaller, manageable items
* Provide training on story slicing techniques and vertical slice architecture patterns
* Establish peer review processes for story breakdown quality

**Architectural Guidance:**
* Provide better architecture guidance on how to break work down while ensuring overall system alignment
* Implement architectural decision records (ADRs) to document design choices
* Establish architecture review processes for larger initiatives to ensure proper decomposition
* Create reusable patterns and templates for common types of work breakdown

## Static Code Analysis and Security Scanning

**Strategic Goal:** Implement comprehensive code quality and security practices that provide continuous feedback and prevent issues from reaching production.

**Implementation Strategy:**
* Implement SonarQube for comprehensive code analysis, code quality assessment, and security/vulnerability scanning
* Integrate static analysis into CI/CD pipelines to provide immediate feedback on code changes
* Establish quality gates that prevent code with critical issues from being deployed

**Technical Debt Identification:**
* Use SonarQube to systematically identify and prioritize technical debt based on severity and impact
* Examples of critical areas to address:
    * Identify critical security vulnerabilities that engineering teams must address immediately
    * Identify outdated components that should be updated to later versions for security and performance
    * Measure code quality metrics including test coverage and adherence to coding standards
    * Detect code smells and maintainability issues that impact development velocity

**Secrets Management:**
* Adopt AWS Secrets Manager across all microservices to eliminate hard-coded secrets in code repositories
* Enable better automation and management of secrets, including automated rotation capabilities
* Implement secure secrets retrieval patterns in application code to replace hardcoded values
* Establish secrets lifecycle management processes including regular rotation schedules
* Create developer guidelines and tooling for secure secrets handling in development and deployment workflows

**Continuous Improvement:**
* Establish code quality metrics and trends tracking over time
* Implement developer training programs based on common issues identified through static analysis
* Create automated remediation suggestions where possible to accelerate issue resolution

## Adopt and Use Feature Flags for Safer Deployments

**Strategic Goal:** Implement feature flag capabilities that enable safer, more controlled deployments with the ability to rapidly respond to issues without rollbacks.

**Deployment Control:**
* Adopt the practice of using feature flags to have more granular control over production deployments
* Separate code deployment from feature release, enabling continuous delivery with controlled feature activation
* Implement progressive rollout strategies to minimize risk exposure

**Gradual Rollout Capabilities:**
* Enable canary releases of new features to specific customer segments before enabling for all customers
* Implement percentage-based rollouts to gradually increase feature exposure
* Establish monitoring and automated rollback triggers based on error rates and performance metrics

**Legacy Management:**
* Contain legacy customizations using feature flags, enabling deployment of a single package rather than numerous customized packages
* Gradually migrate customers from legacy customizations to standard features
* Reduce deployment complexity and testing overhead through unified codebase management

**Risk Mitigation:**
* Use feature flags to instantly disable new features if issues are discovered in production (avoiding the need for complete rollbacks)
* Implement kill switches for critical functionality to enable rapid response to incidents
* Establish automated monitoring that can trigger feature flag changes based on system health metrics

## Internal Developer Portal (IDP)

**Strategic Goal:** Establish a centralized platform that provides developers and operations teams with unified access to all tools, information, and metrics needed for effective software delivery.

**Platform Implementation:**
* Use Atlassian Compass as the internal developer portal utilized by all Engineers and IT Operations teams
* Integrate with existing Atlassian ecosystem (Jira, Confluence) to provide seamless workflow experiences
* Establish single sign-on (SSO) integration for frictionless access to all connected tools

**Unified Dashboard:**
* Create the IDP as the "single pane of glass" that displays:
    * Recent deployments and their status across all environments
    * Changes in progress with clear ownership and timeline information
    * Direct links to observability tools and dashboards for each service
    * Comprehensive scorecards for code quality, security, and adherence to coding standards
    * Service catalog with documentation, ownership, and dependency information

**Developer Experience:**
* Provide self-service capabilities for common development tasks (environment provisioning, database access, etc.)
* Implement developer onboarding workflows and documentation discovery
* Establish service templates and scaffolding tools to accelerate new project setup
* Create personalized dashboards based on developer roles and responsibilities

**Operational Insights:**
* Display real-time system health and performance metrics
* Provide incident management integration and status pages
* Show compliance and audit information in easily digestible formats