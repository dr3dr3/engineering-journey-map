# Engineering Journey Map: Step 2 - Learning & Exploration

## 1. Step Overview

### Purpose Statement
This step transforms engineers from having basic platform access to developing comprehensive working knowledge of platform capabilities, architectural patterns, and quality-focused best practices. Given our organization's transition from manual testing to automation, complex multi-environment setup, and significant technical debt challenges, this exploration phase is crucial for helping engineers make informed decisions that align with our improvement initiatives and avoid perpetuating current organizational challenges.

### Entry Criteria
- Discovery & Onboarding step completed successfully
- Access to all required systems (BitBucket, Jira, Confluence, Datadog, etc.)
- Understanding of organizational challenges and improvement roadmap
- Basic familiarity with squad-specific practices and constraints
- Support relationships established (buddy, platform team)

### Exit Criteria
- Understanding of platform services and their appropriate use cases within our constraints
- Familiarity with both current practices and target automation approaches
- Knowledge of technical debt patterns to avoid in new development
- Ability to identify which services and patterns support our improvement initiatives
- Understanding of environment-specific considerations and testing strategies
- Clear path forward for contributing to quality and automation goals

## 2. Personas & Context

### Primary Users

**Backend Engineers (Microservices Focus)**
- Working with ~40 microservices in our ecosystem
- Need understanding of service communication patterns and data management
- Must learn environment parity challenges and workarounds
- Focus on automation patterns that reduce manual testing burden
- Typical duration: 4-6 days

**Frontend Engineers**
- Working with legacy Windows-based systems and modern web technologies
- Need understanding of our customer customization challenges
- Focus on end-to-end testing with Playwright
- Understanding of deployment patterns across multiple customer instances
- Typical duration: 3-4 days

**Full-Stack Engineers**
- Broad understanding across microservices and frontend systems
- Need to understand complete testing pyramid approach
- Balance current constraints with target automation practices
- Typical duration: 5-7 days

### Use Case Scenarios

**Common Scenarios (80%)**
- Engineer exploring platform for work within one of our 5 squads
- Team member learning automation approaches to reduce manual testing
- Developer understanding environment differences and deployment challenges
- Engineer evaluating technical debt remediation approaches

**Edge Cases**
- Platform team member (1 of 3) deepening expertise in specific services
- Architect (1 of 2) evaluating patterns for broader organizational adoption
- IT Operations team member (1 of 10) learning development perspectives

### Frequency & Duration
- Frequency: 15-20 engineers per month across all squads
- Typical duration: 4-6 days of dedicated learning
- Ongoing exploration: 3-4 hours per week for first 6 weeks
- Time to confident decision-making: 3-4 weeks

## 3. Activities & Tasks

### Core Activities

1. **Service Architecture Review**
   - Study our 40+ microservices architecture and service catalog
   - Understand service communication patterns and dependencies
   - Review environment-specific configurations and their impacts
   - Learn about customer customization patterns and their challenges

2. **Quality and Testing Pattern Study**
   - Review current manual testing practices and their limitations
   - Study Playwright implementation for end-to-end testing
   - Understand TestRail integration and test case management
   - Learn about SonarQube implementation and static analysis benefits
   - Explore unit and integration testing patterns within our constraints

3. **Environment and Infrastructure Learning**
   - Understand our multi-environment structure (Production, Staging, UAT, ENG 1-7)
   - Learn about environment parity challenges and workarounds
   - Study AWS infrastructure patterns and upcoming Terraform initiatives
   - Review deployment challenges across customer-specific instances

4. **Technical Debt and Code Quality**
   - Review technical debt inventory and prioritization approaches
   - Study SonarQube findings and common code quality issues
   - Learn about security vulnerability management
   - Understand refactoring strategies that support automation goals

5. **Monitoring and Observability**
   - Explore Datadog dashboards and monitoring patterns
   - Understand current observability gaps and improvement initiatives
   - Learn about logging standards and debugging approaches
   - Study incident response and troubleshooting patterns

### Sub-tasks Checklist
- [ ] Review complete service catalog with 40+ microservices
- [ ] Study 5 services most relevant to your squad's work
- [ ] Complete hands-on Playwright tutorial and sample test creation
- [ ] Review technical debt items related to your area of focus
- [ ] Explore Datadog dashboards for services you'll work with
- [ ] Understand environment differences and their testing implications
- [ ] Learn about customer customization patterns and challenges
- [ ] Study SonarQube reports and quality metrics
- [ ] Review recent incident post-mortems and lessons learned
- [ ] Understand deployment processes across different environments
- [ ] Practice with BitBucket Pipelines and CI/CD patterns
- [ ] Learn about feature flag strategies and implementation approaches
- [ ] Study AWS infrastructure patterns and cost considerations
- [ ] Complete squad-specific architecture deep-dive session
- [ ] Document questions and insights for knowledge sharing

### Interaction Points
- Platform team (3 people) - technical guidance and best practices
- Squad architect or senior engineer - domain-specific patterns
- IT Operations team members - environment and deployment insights
- Other squad members - shared experiences and lessons learned
- Architecture team (2 people) - design principles and standards

## 4. Tools & Resources

### Required Tools for Exploration
- **Service Documentation**: Confluence-based service catalog and ADRs
- **Code Exploration**: BitBucket repositories for all 40+ services
- **Quality Analysis**: SonarQube dashboards and reports
- **Testing Framework**: Playwright test suite and examples
- **Monitoring**: Datadog dashboards and log exploration
- **Environment Access**: AWS Console for infrastructure understanding

### Learning Resources
- **Architecture Documentation**: Service dependencies and communication patterns
- **Testing Strategy Guide**: Current practices and automation roadmap
- **Technical Debt Inventory**: Prioritized list with remediation strategies
- **Environment Guide**: Setup, differences, and deployment patterns
- **Quality Standards**: Coding standards, security practices, and review guidelines
- **Video Library**:
  - "Our Microservices Journey" - architecture evolution
  - "From Manual to Automated Testing" - transformation strategy
  - "Technical Debt Management Workshop" - prioritization and remediation

### Templates & Examples
- Service template with quality practices
- Test automation examples using Playwright
- Environment-specific deployment configurations
- Code quality improvement examples
- Monitoring and alerting configuration samples

## 5. Pain Points & Friction

### Organizational Challenge Integration

**Information Complexity**
- 40+ microservices with varying documentation quality
- Current vs. target state confusion across different practices
- Technical debt items can be overwhelming and discouraging
- Environment differences make learning patterns more complex

**Testing Transition Challenges**
- Existing manual testing processes conflict with automation learning
- TestRail integration with automated approaches is unclear
- Different squads have varying levels of automation adoption
- Resource allocation between feature work and automation learning

**Environment Parity Issues**
- Learning in non-production environments may not reflect production reality
- Customer customizations create additional complexity for learning
- Deployment pattern variations across environments confuse standard practices
- Infrastructure differences impact service behavior and testing approaches

### Current Impact Assessment
- **Time lost**: Average 20 hours exploring deprecated or problematic patterns
- **Frustration level**: Medium-High due to current state complexity
- **Business impact**: 1-2 week delay in confident architectural decisions
- **Support burden**: 70% of architecture questions relate to current state constraints vs. best practices

### Recent Feedback
- "I spent days learning a pattern only to find out it contributes to our technical debt" - Recent hire
- "The environment differences make it hard to trust what I'm learning" - Squad member
- "I don't know if I should follow what I see in the code or what the documentation says we should do" - Transfer engineer

## 6. Support & Enablement

### Self-Service Options
- **Service Decision Matrix**: Helps choose appropriate services for use cases
- **Technical Debt Assessment Tools**: Self-service analysis of code quality impact
- **Environment Comparison Guide**: Understanding differences and workarounds
- **Testing Strategy Decision Tree**: Choosing appropriate testing approaches
- **Quality Gate Checklist**: Self-assessment for meeting standards

### Human Support
- **Teams Channels**:
  - Platform architecture support (<6 hours response)
  - Squad-specific channels for domain questions
  - Testing automation community of practice
  - Technical debt remediation working group
- **Office Hours**: 
  - Platform team office hours (Tuesdays 2-3pm)
  - Architecture review sessions (Thursdays 3-4pm)
  - Testing automation workshops (bi-weekly)

### Community Resources
- **Squad Retrospectives**: Shared learnings about effective patterns
- **Cross-Squad Knowledge Sharing**: Monthly sessions on successful approaches
- **Architecture Decision Records**: Documented decisions with context and rationale
- **Testing Automation Champions**: Peer network for automation best practices

## 7. Metrics & Measurement

### Quantitative Metrics
- **Learning path completion rate**: 65% (lower due to organizational complexity)
- **Average services explored before confident decision**: 12.3
- **Testing automation workshop attendance**: 80% of engineers in learning phase
- **Technical debt awareness assessment score**: 7.2/10
- **Time spent on environment-specific learning**: 8 hours average

### Qualitative Metrics
- **Confidence in service selection within constraints**: 70%
- **Understanding of quality practices transition**: 75%
- **Ability to identify technical debt patterns**: 68%
- **Satisfaction with learning resources**: 3.5/5
- **Preparedness for contributing to automation initiatives**: 72%

### Leading Indicators
- Participation in testing automation workshops
- Questions asked about current vs. target state practices
- Technical debt pattern recognition in code reviews
- Proactive suggestions for quality improvements
- Cross-squad collaboration on learning initiatives

## 8. Automation & Opportunities

### Current Learning Support Automation
- **Personalized service recommendations** based on squad and role
- **Technical debt hotspot identification** for focused learning
- **Environment difference highlighting** in documentation
- **Quality metric dashboards** for self-assessment
- **Automated progress tracking** with gap identification

### Improvement Opportunities Aligned with Desired State

**Quick Wins (Supporting IDP and Testing Initiatives)**
- **AI-powered guidance** for choosing between current and target practices
- **Automated pattern analysis** to identify technical debt in learning examples
- **Interactive testing strategy advisor** based on organizational context
- **Environment-aware documentation** that shows relevant differences

**Strategic Improvements (Supporting Multiple Initiatives)**
- **Intelligent technical debt remediation recommendations** during learning
- **Automated quality impact assessment** for architectural decisions
- **Progressive testing automation guidance** based on current capabilities
- **Cost and quality impact modeling** for different architectural choices

### Expected ROI
- 50% reduction in exploration time through targeted guidance
- 30% improvement in architectural decision quality
- 40% reduction in patterns that contribute to technical debt
- $75,000 annually in reduced consultation and rework costs

## 9. Dependencies & Integrations

### Upstream Dependencies
- Completed onboarding with organizational context understanding
- Access to all required systems and environments
- Squad-specific context and current priorities
- Availability of platform team and architecture resources
- Time allocation that balances learning with delivery pressures

### Downstream Impact
- **Poor architectural decisions** perpetuate current challenges
- **Inadequate automation understanding** slows testing transformation
- **Technical debt pattern adoption** increases maintenance burden
- **Environment misunderstanding** leads to deployment and quality issues
- **Incomplete quality practice adoption** maintains manual testing dependencies

### System Integrations
- **Service catalog integration** with Confluence and Compass
- **SonarQube integration** for real-time quality feedback
- **Datadog integration** for observability learning
- **BitBucket integration** for code pattern exploration
- **TestRail integration** for understanding current testing approaches

## 10. Best Practices & Anti-patterns

### Recommended Practices

**Do's**
- **Focus on patterns that support automation initiatives** rather than perpetuating manual approaches
- **Ask questions about current vs. target state** when encountering conflicting practices
- **Prioritize learning that addresses organizational challenges** (technical debt, testing, environments)
- **Engage with multiple squads** to understand variation in practices and approaches
- **Document insights and questions** to contribute to organizational learning
- **Balance current constraints with future aspirations** in architectural decisions

**Success Accelerators**
- **Pair with engineers who've successfully adopted automation practices**
- **Participate in technical debt remediation efforts** as learning opportunities
- **Attend cross-squad knowledge sharing sessions** to understand broader context
- **Contribute to testing automation initiatives** during learning phase

### Common Anti-patterns

**Avoid**
- **Following existing code patterns without understanding their technical debt implications**
- **Ignoring environment differences when making architectural decisions**
- **Adopting manual testing approaches when automation alternatives exist**
- **Making decisions in isolation without considering organizational improvement goals**
- **Dismissing current practices without understanding their historical context**
- **Perpetuating customer customization patterns that increase deployment complexity**

### Organizational Success Stories
- "Squad Bravo's focused learning on automation reduced their testing effort by 40%"
- "The cross-squad architecture review identified 3 services that could be consolidated, reducing technical debt"
- "New engineers who focused on quality practices during learning contributed to automated testing from week 1"

---

## Review & Maintenance

**Owner**: Platform Team Lead (1 of 3 platform team members)

**Review Schedule**:
- Monthly: Learning effectiveness and organizational alignment review
- Quarterly: Content updates based on improvement initiative progress
- As-needed: Updates when major initiatives reach new milestones or constraints change

**Last Updated**: December 2024

**Next Review**: February 2025

**Feedback Channel**: Platform architecture Teams channel

---

## Success Validation Checklist

By the end of Learning & Exploration, engineers should:
- [ ] Identify appropriate services and patterns within current organizational constraints
- [ ] Understand both current practices and target automation approaches
- [ ] Recognize technical debt patterns and their organizational impact
- [ ] Make informed decisions that support quality and automation initiatives
- [ ] Navigate environment differences and their implications confidently
- [ ] Contribute to testing automation and quality improvement efforts
- [ ] Understand deployment challenges and customer customization impacts
- [ ] Feel prepared to make architectural decisions that align with organizational goals
- [ ] Have established learning relationships across squads and with platform team
- [ ] Be ready to proceed with informed local development setup and implementation

This refined Learning & Exploration step integrates organizational challenges and improvement initiatives while maintaining comprehensive platform education focused on quality, automation, and architectural excellence.