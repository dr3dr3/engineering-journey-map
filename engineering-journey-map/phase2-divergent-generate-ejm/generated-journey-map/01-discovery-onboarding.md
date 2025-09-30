# Engineering Journey Map: Step 1 - Discovery & Onboarding

## 1. Step Overview

### Purpose Statement
This initial step introduces software engineers to the platform ecosystem, establishing their foundational understanding of available capabilities, resources, and support structures. It transforms new platform users from having zero knowledge to being equipped with the essential context and access needed to begin their platform journey. This critical first impression sets the tone for the entire developer experience and directly impacts long-term adoption success.

### Entry Criteria
- Engineer has been assigned to a project requiring platform usage
- Management approval for platform access has been obtained
- Corporate identity/authentication credentials are active
- Basic development machine setup is complete (OS, corporate VPN, etc.)
- Engineer has received welcome email or onboarding notification

### Exit Criteria
- All required platform accounts and access permissions are provisioned
- Engineer can successfully authenticate to platform services
- Core documentation has been reviewed and bookmarked
- Development environment prerequisites are understood
- Engineer knows where to get help and has joined support channels
- Initial platform orientation is complete

## 2. Personas & Context

### Primary Users

**New Hires**
- No prior platform exposure
- Need comprehensive orientation
- Require cultural context alongside technical information
- Typical duration: 2-3 days

**Internal Transfers**
- Familiar with company but new to platform
- May have preconceptions from previous tools
- Need platform-specific training
- Typical duration: 1-2 days

**Experienced Platform Users (New Project)**
- Need project-specific access and context
- Skip general orientation
- Focus on new services or patterns
- Typical duration: 2-4 hours

### Use Case Scenarios

**Common Scenarios (80%)**
- New engineer joining an existing team using the platform
- Team adopting platform for the first time
- Engineer transitioning from monolith to microservices

**Edge Cases**
- Contractor or vendor requiring limited access
- Emergency onboarding for incident response
- Cross-team temporary access for collaboration
- Re-onboarding after extended absence

### Frequency & Duration
- Frequency: 10-15 new engineers per month (varies by organization size)
- Typical duration: 1-3 days for full onboarding
- Fast-track option: 4 hours for experienced engineers
- Time to productivity: 1-2 weeks post-onboarding

## 3. Activities & Tasks

### Core Activities

1. **Platform Introduction**
   - Watch platform overview video (30 minutes)
   - Review platform architecture diagram
   - Understand platform value proposition and principles

2. **Account Provisioning**
   - Submit access request through IT portal
   - Await approval workflow completion
   - Receive credentials and initial permissions

3. **Documentation Discovery**
   - Access platform documentation portal
   - Navigate information architecture
   - Bookmark essential resources

4. **Tool Installation**
   - Download platform CLI tools
   - Install IDE extensions
   - Configure authentication tokens

5. **Support Channel Setup**
   - Join platform Slack workspace
   - Subscribe to platform newsletter
   - Register for office hours calendar

### Sub-tasks Checklist
- [ ] Read platform principles and philosophy document
- [ ] Complete access request form with manager approval
- [ ] Verify email for account activation links
- [ ] Set up multi-factor authentication
- [ ] Download and install platform CLI
- [ ] Configure CLI authentication
- [ ] Join #platform-support Slack channel
- [ ] Join #platform-announcements Slack channel
- [ ] Add platform documentation site to bookmarks
- [ ] Review getting started guide
- [ ] Identify team-specific platform resources
- [ ] Schedule 1:1 with platform buddy (if assigned)
- [ ] Complete platform basics self-assessment

### Interaction Points
- IT Service Desk (access provisioning)
- Platform team (orientation and support)
- Direct manager (approval and context)
- Team members (peer support and guidance)
- Security team (compliance requirements)

## 4. Tools & Resources

### Required Tools
- **Platform Portal**: https://platform.internal/portal
- **Documentation Hub**: https://docs.platform.internal
- **Access Request System**: https://it.internal/access
- **CLI Installer**: https://platform.internal/cli
- **IDE Extensions**: Available in VS Code/IntelliJ marketplaces

### Documentation & Guides
- Platform Overview Deck (20 slides)
- Getting Started Guide (step-by-step walkthrough)
- Platform Principles & Best Practices
- Architecture Decision Records (ADRs)
- Video Library:
  - "Platform in 10 Minutes" overview
  - "Your First Day with Platform" tutorial
  - "Platform Architecture Deep Dive" (optional)

### Templates & Examples
- Sample onboarding checklist (Confluence template)
- Access request form pre-filled examples
- .bashrc/.zshrc configuration snippets
- IDE configuration templates
- "Hello World" platform application

## 5. Pain Points & Friction

### Known Issues

**Access Delays**
- Access provisioning takes 24-48 hours
- Manual approval bottlenecks
- Unclear permission requirements

**Information Overload**
- Documentation is extensive but poorly organized
- No clear learning path for beginners
- Conflicting information between old and new docs

**Tool Confusion**
- Multiple CLI versions in circulation
- Unclear which IDE extensions are official
- Configuration varies by operating system

### Feedback Collected
- "I didn't know what I needed access to until I tried to build something" - Senior Engineer, Q3 Survey
- "The documentation assumes too much prior knowledge" - New Hire Feedback
- "It took me three days just to get all my access sorted out" - Team Lead Interview
- "I wish there was a single checklist I could follow" - Junior Developer

### Impact Assessment
- **Time lost**: Average 8 hours of productive time lost to access delays
- **Frustration level**: High - this is first impression of platform
- **Business impact**: $2,000 per engineer in lost productivity
- **Support burden**: 40% of week-one support tickets are access-related

## 6. Support & Enablement

### Self-Service Options
- Interactive onboarding wizard in platform portal
- FAQ section with 50+ common questions
- Automated access status checker
- Self-service password reset
- Video tutorial library

### Human Support
- **Slack**: #platform-support (response time: <2 hours)
- **Email**: platform-team@company.internal
- **Office Hours**: Tuesday/Thursday 2-3pm
- **Buddy System**: Optional platform buddy assignment
- **Escalation**: Platform on-call for blocking issues

### Community Resources
- Internal Wiki: "Platform Onboarding Experiences"
- Slack: #platform-newbies (peer support)
- Monthly "New to Platform" virtual meetup
- Platform Champions network (volunteer mentors)
- Onboarding retrospectives repository

## 7. Metrics & Measurement

### Quantitative Metrics
- **Time to first successful authentication**: P50: 4hrs, P90: 48hrs
- **Onboarding completion rate**: 87%
- **Support tickets in first week**: Average 2.3 per engineer
- **Documentation pages visited**: Average 15 in first week
- **Tool installation success rate**: 78% without support

### Qualitative Metrics
- **Onboarding satisfaction score**: 3.2/5
- **Confidence level post-onboarding**: 65% feel "ready to build"
- **Documentation usefulness rating**: 3.5/5
- **Would recommend platform**: 72% (NPS: 15)

### Leading Indicators
- Time from request to access granted
- Number of access request resubmissions
- Slack questions in first 48 hours
- CLI installation failures
- Documentation bounce rate

## 8. Automation & Optimization

### Current Automation
- Automated welcome email with links
- Self-service access request portal
- Automated CLI installation scripts
- Slack bot for common questions
- Calendar integration for office hours

### Automation Opportunities

**Quick Wins**
- Auto-provision basic access based on team membership
- Pre-configure IDE settings via managed profiles
- Generate personalized learning paths
- Automated progress tracking dashboard

**Strategic Improvements**
- Zero-touch provisioning for standard roles
- AI-powered documentation assistant
- Interactive platform sandbox for exploration
- Automated onboarding health checks

### Optimization Recommendations
- Investment needed: 2 sprints of platform team effort
- Potential time savings: 50% reduction in onboarding time
- Expected ROI: Break-even at 20 engineers onboarded

## 9. Dependencies & Integrations

### Upstream Dependencies
- HR system (employee data)
- IT identity management (authentication)
- Corporate email system (communication)
- Manager approval workflow
- Security clearance verification

### Downstream Impact
- Delays here cascade to all subsequent journey steps
- Team productivity affected until engineer is onboarded
- Project timelines may shift
- Mentor/buddy time allocation

### System Integrations
- Active Directory/LDAP for authentication
- ServiceNow for access requests
- Confluence for documentation
- Slack for communication
- GitHub for code access
- Datadog for monitoring access

## 10. Best Practices & Anti-patterns

### Recommended Practices

**Do's**
- Start the access request process before day one
- Assign a platform buddy for first-timers
- Book calendar time for focused onboarding
- Use the official CLI installer (not homebrew)
- Join Slack channels before you need help
- Complete onboarding checklist systematically

**Success Accelerators**
- Schedule orientation with platform team
- Review team-specific runbooks early
- Set up development environment in parallel with access
- Ask questions early and often

### Common Anti-patterns

**Avoid**
- Skipping documentation to "dive right in"
- Using outdated CLI versions from blog posts
- Requesting all possible permissions upfront
- Ignoring security and compliance training
- Working in isolation without joining support channels
- Copy-pasting configuration without understanding

### Success Stories
- "Team Alpha reduced onboarding time by 50% by creating a team-specific supplement to platform docs"
- "The mobile team's 'Platform Buddy' program increased new hire satisfaction scores by 40%"
- "Automated access provisioning pilot saved 20 hours per month of platform team time"

---

## Review & Maintenance

**Owner**: Platform Experience Team Lead

**Review Schedule**:
- Monthly: Metrics review and quick fixes
- Quarterly: Full pain point assessment
- Annually: Complete overhaul based on feedback

**Last Updated**: November 2024

**Next Review**: January 2025

**Feedback Channel**: #platform-onboarding-feedback

---

## Success Validation Checklist

By the end of Discovery & Onboarding, engineers should be able to:
- [ ] Successfully authenticate to the platform portal
- [ ] Access and navigate platform documentation
- [ ] Use platform CLI for basic commands
- [ ] Know where to get help when stuck
- [ ] Understand platform's value proposition
- [ ] Have all necessary permissions for their role
- [ ] Feel welcomed and supported by the platform community
- [ ] Have a clear path forward to next steps in their journey

This comprehensive documentation of the Discovery & Onboarding step provides Platform Engineering teams with actionable insights to optimize the critical first experience engineers have with their platform.