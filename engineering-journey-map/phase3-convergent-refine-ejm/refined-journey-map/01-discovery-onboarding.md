# Engineering Journey Map: Step 1 - Discovery & Onboarding

## 1. Step Overview

### Purpose Statement
This initial step introduces software engineers to the platform ecosystem, establishing their foundational understanding of available capabilities, resources, and support structures. Given our organization's current challenges with manual testing, technical debt, and environment parity issues, this onboarding phase is critical for setting engineers on the right path toward adopting platform best practices and avoiding common pitfalls that contribute to our existing challenges.

### Entry Criteria
- Engineer has been assigned to a project requiring platform usage
- Management approval for platform access has been obtained
- Corporate identity/authentication credentials are active (Azure Entra)
- Basic development machine setup is complete (OS, corporate VPN)
- Engineer has received welcome email or onboarding notification

### Exit Criteria
- All required platform accounts and access permissions are provisioned
- Engineer can successfully authenticate to platform services
- Core documentation has been reviewed and bookmarked in Confluence
- Understanding of organization's current challenges and improvement initiatives
- Engineer knows where to get help and has joined relevant Teams channels
- Initial platform orientation is complete with focus on quality practices

## 2. Personas & Context

### Primary Users

**New Hires to Engineering Teams**
- No prior platform exposure within our organization
- Need comprehensive orientation including our specific challenges and solutions
- Must understand our transition from manual to automated testing approaches
- Typical duration: 3-4 days (extended due to organizational context)

**Internal Transfers**
- Familiar with company tools (Teams, Confluence, Jira) but new to platform
- May need unlearning of manual testing habits
- Need platform-specific training with emphasis on automation
- Typical duration: 2-3 days

**Contractors and Consultants**
- Temporary access with focus on immediate productivity
- Need understanding of current constraints and workarounds
- Focus on tools and processes most relevant to their work
- Typical duration: 1 day focused orientation

### Use Case Scenarios

**Common Scenarios (80%)**
- New engineer joining one of our 5 engineering squads
- Engineer transitioning from legacy Windows-based development to cloud-native approaches
- Team member learning platform as part of our automation initiatives

**Edge Cases**
- Emergency access for critical production issue resolution
- Cross-team temporary access for incident response
- Re-onboarding after extended absence with significant tooling changes

### Frequency & Duration
- Frequency: 3-5 new engineers per month across 5 squads
- Typical duration: 2-4 days for full onboarding
- Time to basic productivity: 1 week
- Time to full effectiveness: 2-3 weeks (due to complexity of current environment)

## 3. Activities & Tasks

### Core Activities

1. **Organizational Context Introduction**
   - Review current state challenges and improvement initiatives
   - Understand the transition from manual to automated testing
   - Learn about technical debt management priorities
   - Review platform engineering team's role and services

2. **Tool Ecosystem Orientation**
   - Set up access to BitBucket repositories (60 repos)
   - Configure access to Jira for work management and issue tracking
   - Access Confluence for documentation and knowledge sharing
   - Set up Datadog access for monitoring and observability
   - Introduction to Atlassian Compass (new internal developer portal)

3. **Environment Understanding**
   - Learn about our multi-environment setup (Production, Staging, UAT, ENG with 7 sub-environments)
   - Understand current environment challenges and parity issues
   - Review access requirements for different environments
   - Learn about upcoming Infrastructure-as-Code initiatives

4. **Quality and Testing Awareness**
   - Understand current manual testing challenges
   - Learn about Playwright for end-to-end testing
   - Introduction to SonarQube (being implemented)
   - Review TestRail for test case management
   - Understand the push toward test automation

5. **Support Network Setup**
   - Join relevant Microsoft Teams channels
   - Connect with platform team (3 people)
   - Identify squad-specific contacts and mentors
   - Understand escalation paths for different types of issues

### Sub-tasks Checklist
- [ ] Read organizational challenges and improvement initiatives document
- [ ] Complete access request forms for all required systems
- [ ] Set up Azure Entra MFA authentication
- [ ] Configure BitBucket access and clone relevant repositories
- [ ] Join squad-specific Teams channels and platform support channels
- [ ] Review Confluence pages for your squad and platform documentation
- [ ] Set up Visual Studio 2022 and/or VS Code with required extensions
- [ ] Configure AWS access through corporate identity
- [ ] Review Datadog dashboards relevant to your squad's services
- [ ] Complete platform principles and quality practices training
- [ ] Schedule 1:1 with assigned buddy from your squad
- [ ] Review current technical debt inventory related to your area
- [ ] Understand feature flag strategy and tooling roadmap
- [ ] Complete onboarding self-assessment and feedback

### Interaction Points
- Platform team (3 people) - orientation and support
- Squad lead - context and expectations
- IT Operations team - environment access and support
- Assigned buddy/mentor - ongoing guidance and questions
- Architecture team (2 people) - design principles and patterns

## 4. Tools & Resources

### Required Tools Access
- **BitBucket**: Source code repositories and CI/CD pipelines
- **Jira**: Work management, sprints, and issue tracking
- **Confluence**: Documentation hub and knowledge repository
- **Microsoft Teams**: Primary collaboration platform
- **Datadog**: Monitoring and observability platform
- **Azure Entra**: Identity and access management
- **AWS Console**: Cloud infrastructure access
- **Atlassian Compass**: Internal developer portal (being implemented)

### Development Environment
- **Visual Studio 2022**: Primary IDE for Windows development
- **VS Code**: Additional IDE option for various technologies
- **Playwright**: End-to-end testing framework
- **TestRail**: Test case management system
- **SonarQube**: Code quality and security scanning (being implemented)

### Documentation & Guides
- Organizational Context and Challenges Overview
- Platform Services Catalog (maintained in Confluence)
- Environment Setup and Access Guide
- Quality Practices and Testing Strategy
- Technical Debt Management Approach
- Architecture Decision Records (ADRs)
- Squad-specific onboarding supplements

## 5. Pain Points & Friction

### Known Organizational Issues

**Access Complexity**
- Multiple systems require separate access requests
- Environment access permissions are complex and often unclear
- Manual approval processes cause delays
- Connection between Azure Entra and AWS IAM can be confusing

**Information Overload with Context**
- Extensive documentation across 60 repositories
- Current state challenges can be overwhelming for new engineers
- Competing priorities between feature work and technical debt
- Unclear which practices to follow (current vs. desired state)

**Tool Integration Challenges**
- BitBucket Pipelines integration with various environments
- Datadog configuration varies across services
- Inconsistent practices across 5 different squads
- Legacy Windows-based tools mixing with cloud-native approaches

### Current Impact Assessment
- **Time lost**: Average 12 hours of productive time lost to access and orientation challenges
- **Frustration level**: High - complexity of current environment is challenging
- **Business impact**: $3,000 per engineer in lost productivity during extended onboarding
- **Support burden**: 50% of first-week support tickets are access and context-related

### Feedback Collected from Recent Hires
- "I didn't understand which testing approach I should follow" - Recent hire feedback
- "The number of environments and their differences is confusing" - New team member
- "I wish there was clearer guidance on what's changing vs. what's current" - Transfer from another team

## 6. Support & Enablement

### Self-Service Options
- Confluence-based onboarding wiki with organizational context
- Access request templates and examples
- Squad-specific onboarding checklists
- Video recordings of common setup procedures
- Automated status checking for access provisioning

### Human Support
- **Teams Channels**: 
  - Platform support channel (response time: <4 hours during business hours)
  - Squad-specific channels for immediate questions
  - General engineering support channel
- **Platform Team**: Direct support from 3-person platform engineering team
- **Buddy System**: Assigned squad member for first month guidance
- **Architecture Team**: Available for design questions and technical guidance

### Community Resources
- Squad retrospectives and learnings documentation
- Cross-squad knowledge sharing sessions
- Monthly "Platform Updates" meetings with improvement progress
- Internal wiki for common questions and solutions

## 7. Metrics & Measurement

### Quantitative Metrics
- **Time to first successful authentication across all systems**: P50: 6hrs, P90: 24hrs
- **Onboarding completion rate**: 85% (lower due to complexity)
- **Support tickets in first week**: Average 3.1 per engineer
- **Time to first commit**: Average 48 hours
- **Access-related delays**: 60% of engineers experience some access delay

### Qualitative Metrics
- **Onboarding satisfaction score**: 2.8/5 (improvement opportunity identified)
- **Confidence level post-onboarding**: 55% feel "ready to contribute"
- **Documentation usefulness rating**: 3.1/5
- **Understanding of organizational context**: 78% feel well-informed about challenges and initiatives

### Leading Indicators
- Time from request to full access granted across all systems
- Number of clarifying questions about current vs. future state practices
- Squad-specific onboarding supplement quality scores
- Buddy system effectiveness ratings

## 8. Automation & Opportunities

### Current Automation
- Automated welcome email with comprehensive resource links
- Template-based access request forms
- Basic health checks for common access issues
- Automated Confluence page generation for new team members

### Improvement Opportunities Aligned with Desired State

**Quick Wins (Supporting IDP Initiative)**
- Integrate onboarding workflow with Atlassian Compass as it's implemented
- Create automated environment access based on squad membership
- Generate personalized learning paths based on role and squad
- Automated progress tracking dashboard

**Strategic Improvements (Supporting Multiple Initiatives)**
- **Zero-touch provisioning** for standard roles (supports automation goals)
- **Environment parity demonstration** in onboarding (addresses current challenges)
- **Integrated quality practices training** (supports testing automation transition)
- **Technical debt awareness integration** (supports debt management initiatives)

### Expected Outcomes
- 40% reduction in onboarding time through automation
- Improved understanding of organizational direction and priorities
- Better alignment with quality and automation initiatives from day one
- Reduced support burden on platform team and squad leads

## 9. Dependencies & Integrations

### Upstream Dependencies
- HR system integration for new hire notifications
- Azure Entra identity management
- Management approval workflows
- Squad capacity for buddy assignment
- Platform team availability for orientation

### Downstream Impact
- Delays cascade through all subsequent journey steps
- Poor onboarding affects squad velocity and quality practices adoption
- Misunderstanding of priorities can lead to working against improvement initiatives
- Inadequate context-setting impacts long-term employee satisfaction and retention

### System Integrations
- Azure Entra (identity management)
- BitBucket (code repository access)
- AWS IAM (cloud resource access)
- Jira (work management)
- Confluence (documentation)
- Microsoft Teams (communication)
- Datadog (monitoring access)

## 10. Best Practices & Anti-patterns

### Recommended Practices

**Do's**
- Start access requests before first day when possible
- Focus on understanding both current challenges and future direction
- Engage actively with assigned buddy and squad members
- Ask questions early about conflicting practices or unclear processes
- Document gaps or confusion to help improve onboarding for others
- Participate in squad retrospectives and knowledge sharing

**Success Accelerators**
- Schedule dedicated time with platform team for organizational context
- Review recent technical debt items relevant to your area
- Understand squad-specific adaptations to organizational challenges
- Connect with other recent hires for peer support

### Common Anti-patterns

**Avoid**
- Trying to solve organizational challenges independently without context
- Ignoring current state constraints in favor of ideal practices
- Skipping documentation review due to volume (use filtering strategies instead)
- Working in isolation without leveraging support networks
- Making assumptions about practices without confirming current squad approaches
- Dismissing legacy approaches without understanding transition plans

### Success Stories
- "Squad Delta's contextualized onboarding reduced new hire questions by 60%"
- "The platform team's 'challenges and opportunities' overview helped new engineers understand priorities"
- "Pairing new hires with engineers who experienced the transition improved satisfaction scores"

---

## Review & Maintenance

**Owner**: Platform Experience Lead (within 3-person platform team)

**Review Schedule**:
- Monthly: Metrics review and immediate improvements
- Quarterly: Full assessment including organizational context updates
- As-needed: Updates when major initiatives (IDP, automation) reach milestones

**Last Updated**: December 2024

**Next Review**: February 2025

**Feedback Channel**: Platform support Teams channel

---

## Success Validation Checklist

By the end of Discovery & Onboarding, engineers should:
- [ ] Successfully authenticate to all required systems
- [ ] Understand organizational challenges and improvement roadmap
- [ ] Access and navigate squad-specific and platform documentation
- [ ] Know current vs. desired state practices for their role
- [ ] Have established support relationships (buddy, platform team, squad)
- [ ] Understand environment structure and access patterns
- [ ] Feel confident in escalation paths and help-seeking
- [ ] Have context for quality practices and automation direction
- [ ] Be prepared to contribute to both delivery and improvement initiatives

This refined Discovery & Onboarding step addresses the specific organizational context while maintaining the comprehensive structure needed for effective platform adoption.