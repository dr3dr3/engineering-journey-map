# Engineering Journey Map: Step 3 - Local Development Setup

## 1. Step Overview

### Purpose Statement
This step enables engineers to establish a productive local development environment that aligns with our organizational goals of reducing manual testing, improving code quality, and supporting automation initiatives. Given our challenges with environment parity and the need to transition from legacy Windows-based development to modern cloud-native approaches, this setup phase is critical for establishing practices that support our improvement roadmap.

### Entry Criteria
- Learning & Exploration step completed with understanding of services and patterns
- Knowledge of organizational challenges and target automation approaches
- Access to all required development tools and systems
- Understanding of squad-specific development practices and constraints
- Clear project assignment or development objective

### Exit Criteria
- Fully functional local development environment with quality tooling
- Ability to run and test services locally with minimal environment parity issues
- Integration with CI/CD pipelines and quality gates
- Understanding of debugging and troubleshooting approaches within our constraints
- Capability to contribute to automation and quality improvement initiatives
- Successful completion of "hello world" deployment through our pipeline

## 2. Personas & Context

### Primary Users

**Microservices Developers**
- Working with subset of our 40+ microservices locally
- Need Docker/containerization for service dependencies
- Must understand service communication testing approaches
- Focus on unit and integration testing automation
- Typical setup time: 2-3 days

**Legacy System Developers**
- Working with Windows-based legacy systems
- Need Visual Studio 2022 configuration for .NET development
- Understanding migration patterns toward cloud-native approaches
- Balance between legacy constraints and modern practices
- Typical setup time: 1-2 days

**Full-Stack Developers**
- Need both frontend and backend development capabilities
- Understanding of end-to-end testing with Playwright
- Integration with multiple environment configurations
- Typical setup time: 3-4 days

### Use Case Scenarios

**Common Scenarios (80%)**
- New squad member setting up for assigned project work
- Engineer configuring environment for automation testing contributions
- Developer preparing for technical debt remediation work
- Team member updating setup for new tooling (SonarQube, feature flags)

**Edge Cases**
- Emergency environment setup for critical production issue debugging
- Contractor setup with limited access and specific tool requirements
- Cross-squad collaboration requiring additional service access

### Frequency & Duration
- Frequency: 10-15 environment setups per month
- Initial setup time: 2-4 days depending on complexity
- Environment updates: 2-3 hours monthly as tooling evolves
- Time to first meaningful contribution: 3-5 days post-setup

## 3. Activities & Tasks

### Core Activities

1. **Development Environment Configuration**
   - Install and configure Visual Studio 2022 and/or VS Code
   - Set up local Docker environment for containerized services
   - Configure AWS CLI and local credentials for development access
   - Install Node.js, .NET, and other runtime dependencies

2. **Source Code and Repository Setup**
   - Clone relevant repositories from BitBucket (subset of 60 total)
   - Configure Git settings and commit signing
   - Set up repository-specific development configurations
   - Understand branching strategies and squad-specific workflows

3. **Quality and Testing Tool Configuration**
   - Install and configure Playwright for end-to-end testing
   - Set up SonarQube integration for local code analysis
   - Configure unit testing frameworks and coverage tools
   - Install linting and code formatting tools

4. **Local Service and Database Setup**
   - Configure local databases and data management
   - Set up service dependencies and mock services
   - Configure environment variables for different testing scenarios
   - Establish local testing data management practices

5. **Monitoring and Debugging Setup**
   - Configure local logging and debugging tools
   - Set up Datadog local development agent (if applicable)
   - Configure performance profiling and monitoring tools
   - Establish troubleshooting and diagnostic approaches

### Sub-tasks Checklist
- [ ] Install Visual Studio 2022 with relevant extensions and configurations
- [ ] Install VS Code with recommended extensions for your technology stack
- [ ] Set up Docker Desktop and configure container networking
- [ ] Configure AWS CLI with appropriate development credentials
- [ ] Clone squad-specific repositories and verify build processes
- [ ] Install Playwright and run sample end-to-end tests
- [ ] Configure SonarQube integration for local code analysis
- [ ] Set up local database instances and test data
- [ ] Configure environment variables for different testing scenarios
- [ ] Install and configure linting tools and code formatters
- [ ] Set up unit testing frameworks and verify test execution
- [ ] Configure debugging tools and profilers
- [ ] Establish local build and deployment verification process
- [ ] Test integration with BitBucket Pipelines from local environment
- [ ] Verify access to all required external services and APIs
- [ ] Complete local environment validation checklist
- [ ] Document any squad-specific customizations or workarounds

### Interaction Points
- Platform team (3 people) - tooling configuration and environment setup
- Squad senior developer - squad-specific practices and configurations
- IT Operations team - network access and security configurations
- Other squad members - shared configuration practices and troubleshooting
- Architecture team - standards compliance and pattern validation

## 4. Tools & Resources

### Required Development Tools
- **IDEs**: Visual Studio 2022, VS Code with extensions
- **Containerization**: Docker Desktop, Docker Compose
- **Cloud Tools**: AWS CLI, Azure CLI for identity management
- **Version Control**: Git with BitBucket integration
- **Testing**: Playwright, NUnit/.NET testing frameworks, Jest (for JavaScript)
- **Quality**: SonarQube Scanner, ESLint, StyleCop

### Development Services
- **Databases**: Local SQL Server, PostgreSQL, or containerized alternatives
- **Message Queues**: Local RabbitMQ or AWS LocalStack for SQS/SNS
- **API Testing**: Postman, Insomnia, or similar tools
- **Performance**: Application performance monitoring tools
- **Documentation**: Local documentation servers and API documentation tools

### Configuration Resources
- **Environment Templates**: Squad-specific environment configuration templates
- **Docker Compose Files**: Service dependency management configurations
- **Testing Data**: Anonymized data sets for local development and testing
- **Configuration Guides**: Step-by-step setup guides with troubleshooting
- **Video Tutorials**: Screen recordings of common setup procedures

## 5. Pain Points & Friction

### Environment Complexity Challenges

**Service Dependency Management**
- Local setup of microservice dependencies can be complex and resource-intensive
- Version compatibility issues between services developed by different squads
- Network configuration challenges for inter-service communication
- Database setup and data seeding for realistic testing scenarios

**Environment Parity Issues**
- Local environments may not accurately reflect production configurations
- Customer-specific customizations difficult to replicate locally
- Environment-specific configurations create testing and debugging challenges
- Infrastructure differences between local and cloud environments

**Legacy System Integration**
- Windows-based development requirements conflict with cloud-native tooling
- Legacy database and service dependencies difficult to containerize
- Mixed technology stacks require complex local environment management
- Performance differences between local and production Windows environments

### Current Impact Assessment
- **Setup complexity**: Average 16 hours for complete environment setup
- **Maintenance overhead**: 3-4 hours monthly for environment updates and fixes
- **Productivity impact**: 20% reduction in development velocity due to environment issues
- **Support burden**: 40% of platform team support time related to local environment issues

### Feedback from Recent Environment Setups
- "Getting all the services running locally takes forever and uses all my laptop resources" - Backend Developer
- "I can't reproduce the production issue locally because the data is so different" - Senior Engineer
- "Every time someone updates a shared service, my local environment breaks" - Frontend Developer

## 6. Support & Enablement

### Self-Service Options
- **Automated Setup Scripts**: PowerShell and Bash scripts for common configurations
- **Environment Health Checks**: Automated validation of local environment setup
- **Container Orchestration**: Docker Compose files for common service combinations
- **Configuration Management**: Infrastructure-as-code templates for local environments
- **Troubleshooting Guides**: Common issues and resolution steps

### Human Support
- **Teams Channels**:
  - Local development support (<4 hours response during business hours)
  - Squad-specific channels for environment questions
  - Platform engineering support for tooling issues
- **Pair Programming**: Senior developers available for setup assistance
- **Office Hours**: Platform team available for complex environment issues
- **Escalation**: Architecture team for standards and complex configuration issues

### Community Resources
- **Squad Documentation**: Shared setup experiences and optimizations
- **Cross-Squad Knowledge Sharing**: Best practices for environment management
- **Tool-Specific Communities**: Internal communities for Docker, testing, and quality tools
- **Configuration Repository**: Shared configurations and environment templates

## 7. Metrics & Measurement

### Quantitative Metrics
- **Setup time**: P50: 12 hours, P90: 24 hours for complete environment
- **Environment reliability**: 78% success rate for first-attempt setup
- **Support requests**: Average 2.1 requests per environment setup
- **Time to first build**: Average 3 hours after initial setup
- **Environment update frequency**: 2.3 updates per month per developer

### Qualitative Metrics
- **Environment satisfaction**: 3.1/5 (improvement opportunity identified)
- **Confidence in local testing**: 65% feel local tests represent production scenarios
- **Productivity impact rating**: 3.4/5
- **Tool effectiveness**: 3.7/5 for development productivity
- **Knowledge sharing effectiveness**: 3.2/5

### Leading Indicators
- Time spent on environment troubleshooting vs. development
- Frequency of "works on my machine" issues in code reviews
- Adoption rate of recommended tools and configurations
- Participation in environment optimization initiatives

## 8. Automation & Opportunities

### Current Automation
- **Setup Scripts**: Partially automated installation and configuration
- **Container Images**: Pre-built development environment containers
- **Configuration Templates**: Standardized environment variable and connection templates
- **Health Checks**: Automated validation of environment setup completeness

### Improvement Opportunities Aligned with Desired State

**Quick Wins (Supporting IDP and Infrastructure Initiatives)**
- **One-click environment setup** through Atlassian Compass integration
- **Automated dependency management** using Infrastructure-as-Code patterns
- **Environment synchronization** with production configurations
- **Quality gate integration** in local development workflow

**Strategic Improvements (Supporting Multiple Initiatives)**
- **Ephemeral development environments** aligned with infrastructure goals
- **Automated test data provisioning** supporting data management initiatives
- **Integrated quality feedback** with SonarQube and testing automation
- **Environment-as-code** supporting reproducible development setups

### Expected ROI
- 60% reduction in environment setup time through automation
- 40% reduction in environment-related support requests
- 25% improvement in development velocity through reliable environments
- $100,000 annually in reduced setup and maintenance costs

## 9. Dependencies & Integrations

### Upstream Dependencies
- Completed learning phase with understanding of required services and tools
- Access provisioning to all required development systems and services
- Hardware/laptop specifications adequate for development requirements
- Network access and security configurations from IT Operations

### Downstream Impact
- **Inadequate environment setup** significantly impacts all subsequent development activities
- **Environment parity issues** reduce effectiveness of local testing and debugging
- **Complex setup processes** discourage automation and quality practice adoption
- **Unreliable environments** reduce developer productivity and satisfaction

### System Integrations
- **BitBucket integration** for source code management and CI/CD
- **AWS integration** for cloud service development and testing
- **SonarQube integration** for code quality analysis
- **Datadog integration** for monitoring and observability
- **Testing framework integration** for automated quality assurance

## 10. Best Practices & Anti-patterns

### Recommended Practices

**Do's**
- **Use containerization** for service dependencies to improve consistency and portability
- **Follow Infrastructure-as-Code principles** for environment configuration
- **Integrate quality tools** into development workflow from the beginning
- **Maintain environment documentation** and share configuration improvements
- **Participate in environment standardization** initiatives across squads
- **Practice local testing** that mirrors production scenarios as closely as possible

**Success Accelerators**
- **Pair with experienced developers** during initial environment setup
- **Contribute environment improvements** back to shared templates and documentation
- **Participate in platform team initiatives** for environment standardization
- **Use squad-specific optimizations** while maintaining compatibility with broader initiatives

### Common Anti-patterns

**Avoid**
- **Custom local configurations** that deviate significantly from production patterns
- **Skipping quality tool integration** to speed up initial setup
- **Working around environment issues** rather than documenting and fixing them
- **Ignoring containerization opportunities** in favor of local installation complexity
- **Maintaining private environment configurations** rather than contributing improvements
- **Accepting poor environment parity** without seeking improvement opportunities

### Success Stories
- "Squad Echo's containerized development environment reduced setup time from 2 days to 4 hours"
- "The shared environment templates eliminated 70% of setup-related support requests"
- "Integrating SonarQube locally helped identify technical debt before code review"

---

## Review & Maintenance

**Owner**: Platform Team Lead

**Review Schedule**:
- Monthly: Environment setup metrics and common issues review
- Quarterly: Tool effectiveness and infrastructure alignment assessment
- As-needed: Updates for new tooling rollouts and infrastructure initiatives

**Last Updated**: December 2024

**Next Review**: February 2025

**Feedback Channel**: Local development support Teams channel

---

## Success Validation Checklist

By the end of Local Development Setup, engineers should:
- [ ] Have fully functional development environment with all required tools
- [ ] Successfully build and run relevant services locally
- [ ] Execute automated tests locally with reliable results
- [ ] Integrate with quality tools (SonarQube, linting, testing frameworks)
- [ ] Understand debugging and troubleshooting approaches for their technology stack
- [ ] Contribute to environment standardization and improvement initiatives
- [ ] Feel confident in local development productivity and quality practices
- [ ] Be prepared to begin effective development work with minimal environment-related barriers
- [ ] Have documented and shared any environment optimizations or improvements
- [ ] Successfully complete validation deployment through CI/CD pipeline

This refined Local Development Setup step addresses organizational challenges around environment complexity while supporting automation, quality, and infrastructure improvement initiatives.