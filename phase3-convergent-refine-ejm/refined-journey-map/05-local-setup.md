# 05. Local Setup

**Objective:** Setting up optimized local development environments with standardized tooling and automated configuration management  
**Duration:** 30-60 minutes per project (Target: down from current 2-8 hours)  
**Frequency:** Once per project or when switching technology stacks

## Engineer Perspective

### Goals
- Provision a complete, standardized development environment that mirrors production through Infrastructure as Code
- Achieve instant environment startup with all dependencies, services, and configurations working correctly
- Access unified tooling with single sign-on that works consistently across all technology stacks
- Complete first code contribution within one hour of environment setup through streamlined workflows
- Validate environment health through automated testing and monitoring integration

### Actions
1. Execute single-command environment provisioning using standardized Infrastructure as Code templates
2. Access pre-configured development environment with automatic dependency management and version synchronization
3. Verify environment health through automated validation scripts and comprehensive system checks
4. Connect to shared development services (databases, APIs, message queues) through secure, automated configuration
5. Configure IDE integration with automatic code quality, security scanning, and debugging tool setup
6. Execute initial code build and test suite to validate complete environment functionality
7. Access unified monitoring and observability tools pre-configured for the specific project context

### Touchpoints
- **Platform Services:** Internal Developer Portal with environment templates, automated infrastructure provisioning, unified SSO across all tools
- **Tools & Systems:** Standardized container runtimes (Docker/Podman), cloud-based development environments, automated IDE configuration, centralized secrets management
- **People & Teams:** Platform engineering team for environment template maintenance, development teams for project-specific customizations, automated support through chatbots and documentation

### Emotions & Experience
- **Positive Moments:** One-command setup completion, instant environment startup, seamless tool integration, immediate productivity
- **Eliminated Frustrations:** Zero dependency conflicts, no platform-specific issues, eliminated manual configuration, consistent experience across projects
- **Confidence Factors:** Automated environment validation, comprehensive documentation, proactive health monitoring, self-healing capabilities

## Current State Analysis (Based on Organizational Context)

### Pain Points (From Survey and Retrospective Feedback)
- **Environment Inconsistency:** Local development environments significantly different from production AWS infrastructure, causing "deployment surprises"
- **Resource Intensity:** Local environments require substantial CPU and memory, with laptops "sounding like jet engines" affecting developer experience
- **Setup Complexity:** Current setup ranges from 2-8 hours per project with high failure rates, requiring manual intervention and "15 different tools"
- **Dependency Hell:** Complex dependency management with .NET Core, Node.js version conflicts, and package manager inconsistencies across 60+ repositories
- **Technology Stack Fragmentation:** Different setup procedures for microservices vs. legacy Windows applications, mobile development, and data engineering workloads
- **Documentation Lag:** Setup instructions become outdated as projects evolve, leading to failed attempts and debugging sessions

### Current Workarounds (From Team Feedback)
- **Personal Scripts:** Engineers create custom automation to work around standard setup procedures
- **Shared Development:** Use of staging environments when local setup fails or is too resource-intensive
- **Slack Support Channels:** Dedicated channels like "#frontend-help-setup" for peer support and shared troubleshooting
- **Senior Developer Dependency:** Heavy reliance on experienced team members for setup assistance and screen-sharing sessions

### Effort & Complexity (Current Metrics)
- **Time Investment:** 4-8 hours per project for most engineers, extending to multiple days for complex environments
- **Success Rate:** Only 70% of engineers complete setup without requiring help, indicating high complexity barriers
- **Support Burden:** High volume of environment-related support tickets affecting platform team productivity

## Platform Engineering Opportunities (Based on Future State Vision)

### Automation Potential
- **Infrastructure as Code Templates:** Standardized Terraform-based environment definitions for all project types and technology stacks
- **One-Command Provisioning:** Single CLI command that provisions complete environments with all dependencies and configurations
- **Cloud-Based Development:** Remote development environments for resource-intensive workloads and specialized tools
- **Automated Health Monitoring:** Continuous environment validation with self-healing capabilities for common configuration drift

### Tooling Improvements (Aligned with Current Tools)
- **Unified Developer Portal:** Integration with Atlassian Compass for consistent environment access and management
- **Container Standardization:** Consistent Docker/container patterns across all 60+ repositories and microservices
- **IDE Integration:** Automated VS Code and Visual Studio 2022 configuration with project-specific extensions and settings
- **Secrets Management:** Integration with AWS Secrets Manager for secure, automated credential management

### Process Optimization (Supporting Current Practices)
- **Technology Stack Templates:** Pre-configured environments for .NET Core, Node.js, React Native, and data engineering workflows
- **Environment Lifecycle Management:** Automated start/stop scheduling for cost optimization and resource management
- **Progressive Setup:** Layered approach allowing minimal setup for quick tasks and full setup for comprehensive development
- **Cross-Platform Consistency:** Standardized development experience across Windows, macOS, and Linux platforms

### Knowledge & Support (Enhanced Documentation Strategy)
- **Interactive Setup Guides:** Step-by-step guided setup within the developer portal with real-time validation
- **Automated Troubleshooting:** Diagnostic tools that identify and resolve common environment issues automatically
- **Version-Controlled Documentation:** Environment documentation that stays synchronized with infrastructure changes

## Success Metrics

### Current State Metrics (Baseline)
- **Setup Success Rate:** 70% complete without help
- **Time to First Code:** 4-8 hours average from project clone to working environment
- **Environment Consistency:** 60% parity between local and production configurations
- **Support Ticket Volume:** High volume of environment-related tickets affecting team productivity

### Target Metrics (Platform Engineering Goals)
- **Setup Success Rate:** 95% automated setup completion without manual intervention
- **Time to First Code:** 30-60 minutes from project selection to productive development environment
- **Environment Consistency:** 90% configuration parity with production AWS infrastructure
- **Resource Efficiency:** 50% reduction in local resource consumption through optimized containerization and cloud alternatives

### Platform Impact Metrics (Organizational Benefits)
- **Developer Satisfaction:** 90% satisfaction score for environment setup experience (up from current poor ratings)
- **Productivity Improvement:** 75% reduction in environment-related context switching and troubleshooting time
- **Support Reduction:** 70% reduction in environment setup support tickets and manual intervention requirements
- **Onboarding Acceleration:** New engineers productive within first day instead of current 1-2 weeks for complex projects

## Technology-Specific Considerations

### Microservices Development (40+ repositories)
- **Service Orchestration:** Automated Docker Compose or Kubernetes setups for multi-service development
- **Dependency Management:** Automated service dependency mapping and startup orchestration
- **API Integration:** Pre-configured local API gateways and service mesh integration

### Legacy Windows Applications
- **Containerization Strategy:** Gradual containerization path for Windows-based legacy systems
- **Hybrid Development:** Bridge between legacy Windows environments and modern containerized workflows
- **Migration Support:** Tools and documentation for transitioning legacy applications to cloud-native patterns

### Data Engineering Workflows
- **Specialized Environments:** Data-specific development environments with appropriate scale and tools
- **Data Pipeline Testing:** Local data pipeline testing with synthetic data and validation frameworks
- **Analytics Integration:** Pre-configured connections to Redshift, data lakes, and analytical tools

### Mobile Development (React Native)
- **Cross-Platform Tooling:** Consistent development setup for iOS and Android development
- **Device Simulation:** Comprehensive simulator and emulator management
- **Native Bridge Development:** Tools for developing and testing native module integrations