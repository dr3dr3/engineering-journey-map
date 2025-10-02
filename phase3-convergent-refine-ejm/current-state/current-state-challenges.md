# Current State - Challenges

These notes describe the "current state" of our organization. 

This document specifically focuses on the current challenges the organization is experiencing. 

The goal of the organization is to:

* Eliminate these challenges where possible
* Mitigate the negative impacts being experienced from these challenges, or
* Reduce the negative impacts of these challenges

## Current challenges

### High reliance on manual testing

**Why this is a problem:**
Manual testing creates significant bottlenecks in the development process and introduces human error factors that can compromise quality and consistency. It requires dedicated human resources for repetitive tasks that could be automated, leading to inefficient resource allocation.

**Current situation:**
* Every feature developed requires some level of manual testing
* Every sprint has a lot of testing effort at the end to get everything completed
* Releasing changes to production is difficult due to all this manual testing effort
* This encourages changes to be batched into bigger change sets
* Which increases the risk for each deployment to production
* There is a lot of effort (and time) to do manual regression testing

**Impact on the organization:**
* **Slower time-to-market:** Manual testing delays feature releases and reduces competitive advantage
* **Higher operational costs:** Significant human resources dedicated to repetitive testing tasks
* **Increased deployment risk:** Large batched releases have higher probability of failures and more complex rollback scenarios
* **Team burnout:** Testing teams experience stress from repetitive work and pressure to complete testing within sprint timelines
* **Reduced innovation capacity:** Development teams spend less time on new features due to testing bottlenecks
* **Quality inconsistency:** Human error in manual testing can lead to missed defects reaching production

### Non-production environments are not like production environment

**Why this is a problem:**
Environment parity is crucial for accurate testing and reliable deployments. When non-production environments don't mirror production, testing becomes less effective and issues emerge in production that were not caught during development and testing phases.

**Current situation:**
* Data in non-production environments is not similar enough to what is in production
* This means testing does not reflect production scenarios
* There is a lot of effort (and time) to manually create data needed for testing
* Configuration tested does not cover all the various configurations in production
* Intermittent issues are proving to be difficult to replicate and resolve

**Impact on the organization:**
* **False confidence in releases:** Testing in unrealistic environments provides misleading assurance about production readiness
* **Production-only defects:** Issues that only manifest with production data volumes, types, or configurations
* **Delayed issue resolution:** Inability to reproduce production issues in lower environments extends debugging time
* **Wasted testing effort:** Time spent testing scenarios that don't reflect real-world usage patterns
* **Customer impact:** Production issues that weren't caught in testing directly affect end users
* **Increased support burden:** More production issues lead to higher support ticket volumes and customer dissatisfaction

### Triaging issues is difficult

**Why this is a problem:**
Effective issue triage is essential for maintaining system reliability and customer satisfaction. When teams cannot quickly identify, reproduce, and resolve issues, it leads to prolonged system outages, frustrated customers, and inefficient use of engineering resources.

**Current situation:**
* Reproducing production issues is difficult in lower environments
* Especially when non-production environments are not the same as production
* A lot of effort and time is spent on analyzing and finding causes for issues

**Impact on the organization:**
* **Extended resolution times:** Longer mean time to resolution (MTTR) directly impacts customer experience and system availability
* **Resource inefficiency:** Engineers spend disproportionate time on investigation rather than development work
* **Customer churn risk:** Unresolved or slowly resolved issues can lead to customer dissatisfaction and loss of business
* **Reduced system reliability:** Poor issue triage contributes to lower overall system uptime and performance
* **Team frustration:** Engineers become demotivated when they cannot effectively debug and fix problems
* **Compounding technical debt:** Unresolved root causes lead to workarounds that create additional technical debt

### Too much customisation for customers

**Why this is a problem:**
Excessive customization creates architectural complexity that multiplies testing, deployment, and maintenance overhead. It fragments the codebase and makes it difficult to maintain consistency across different customer environments, leading to scalability and reliability issues.

**Current situation:**
* We have multiple customized instances in production for specific customers
* This makes testing more challenging, as those customizations also need to be tested
* It makes deployments more difficult, as we need to deploy code changes to multiple targets
* Has resulted in rollbacks due to incorrect deployments and issues not covered in testing

**Impact on the organization:**
* **Exponential complexity growth:** Each customization multiplies the testing and deployment scenarios required
* **Reduced development velocity:** Features take longer to develop when they must work across multiple customized environments
* **Higher maintenance costs:** Multiple codebases or configuration variants require more resources to maintain
* **Increased risk of failures:** More deployment targets mean more opportunities for environment-specific issues
* **Technical debt accumulation:** Customizations often bypass standard architectural patterns, creating maintenance burden
* **Customer experience inconsistency:** Different customers receive different experiences, making it harder to provide consistent support
* **Scalability limitations:** Customization-heavy architecture makes it difficult to scale the platform efficiently

### Stories in Jira are too large

**Why this is a problem:**
Large user stories violate agile principles and create significant planning and delivery challenges. They make it difficult to estimate effort accurately, track progress effectively, and deliver value incrementally. This leads to poor sprint planning and unpredictable delivery timelines.

**Current situation:**
* The engineering teams are finding stories (features) are too large to complete in a sprint
* They are struggling with how to slice stories into smaller ones
* They are finding hidden complexity once they begin work on features

**Impact on the organization:**
* **Poor sprint predictability:** Teams cannot reliably commit to sprint goals when story sizes are unpredictable
* **Delayed feedback loops:** Large stories delay the delivery of value and customer feedback
* **Increased risk of scope creep:** Large stories are more likely to expand beyond original estimates
* **Difficult progress tracking:** It's harder to measure progress on large, monolithic work items
* **Team frustration:** Developers struggle with overwhelming work items that don't provide clear completion criteria
* **Stakeholder dissatisfaction:** Business stakeholders see delayed delivery of promised features
* **Planning inefficiency:** Sprint planning becomes less effective when story sizes are inconsistent and unpredictable
* **Quality risks:** Large stories are harder to test comprehensively and more likely to contain defects

### A lot of capacity is allocated to bug issues

**Why this is a problem:**
When the majority of engineering capacity is consumed by bug fixes rather than new feature development, it indicates systemic quality issues and creates a vicious cycle. This reactive approach prevents teams from building robust solutions and improving the underlying system quality.

**Current situation:**
* Over half the capacity of engineering teams is used on fixing bugs and issues
* The quality of code released is not sufficient to prevent new issues
* There is too much effort required to ensure quality due to the manual effort and time needed for testing
* Urgent issues (considered reactive work) are disrupting the teams' planned work

**Impact on the organization:**
* **Innovation stagnation:** Limited capacity for new features and improvements reduces competitive advantage
* **Technical debt spiral:** Focus on quick fixes rather than root cause resolution creates more problems over time
* **Team morale decline:** Engineers become frustrated working primarily on fixes rather than creative development
* **Customer dissatisfaction:** Frequent bugs erode customer confidence and trust in the product
* **Opportunity cost:** Resources spent on bug fixes could be invested in preventive measures and new capabilities
* **Unpredictable delivery:** Reactive work makes it impossible to maintain consistent development velocity
* **Increased support costs:** High bug volumes require more customer support resources
* **Reputation damage:** Quality issues can harm the organization's market reputation and customer retention

### Technical debt is accumulating and not being prioritized

**Why this is a problem:**
Technical debt represents shortcuts and compromises made during development that require future refactoring. When not addressed systematically, it compounds over time, making the system increasingly difficult to maintain, extend, and secure. This creates a compounding interest effect that eventually overwhelms development capacity.

**Current situation:**
* Engineers feel that feature development always takes priority over tech debt
* Recent static code analysis and security scanning have identified many tech debt items
* The amount of tech debt is intimidating and it is unclear how or where to start reducing it
* It is suspected that tech debt is leading to many bugs being found in production and poor system performance

**Impact on the organization:**
* **Exponentially increasing maintenance costs:** Technical debt compounds over time, making future changes more expensive
* **Reduced development velocity:** Poor code quality slows down all development activities
* **Security vulnerabilities:** Outdated dependencies and poor code practices create security risks
* **System instability:** Technical debt often manifests as production bugs and performance issues
* **Developer productivity decline:** Engineers spend more time navigating poor code quality and working around limitations
* **Knowledge transfer difficulties:** Complex, poorly documented code makes onboarding new team members harder
* **Business agility reduction:** Technical constraints limit the organization's ability to respond quickly to market changes
* **Competitive disadvantage:** Slower development cycles due to technical debt can result in missed market opportunities

### Testing resourcing, effort, and time are too high

**Why this is a problem:**
Excessive reliance on manual testing and high QA-to-developer ratios indicate inefficient quality assurance processes. This approach is not scalable and creates bottlenecks that slow down delivery while consuming significant resources that could be better allocated to development and automation efforts.

**Current situation:**
* Engineering teams currently have a ratio of 1x QA role per 1x Engineer, which is too high
* Testing efforts are mostly manual and time-consuming
* There is little test automation, with automation only focused on end-to-end testing
* Test coverage is not sufficient, especially when doing regression testing (due to manual effort)

**Impact on the organization:**
* **High operational costs:** Excessive QA staffing represents a significant ongoing expense
* **Scalability constraints:** Manual testing approaches don't scale effectively with product growth
* **Development bottlenecks:** High dependency on manual QA creates constraints on development team productivity
* **Quality gaps:** Insufficient test coverage due to manual effort limitations leads to defects reaching production
* **Slower release cycles:** Manual testing processes extend the time required to release new features
* **Resource allocation inefficiency:** Over-investment in manual testing reduces capacity for development and automation
* **Team dependencies:** Strong coupling between development and QA teams creates coordination overhead
* **Competitive disadvantage:** Slower delivery cycles due to testing bottlenecks can impact time-to-market for new features

### Lack of testing maturity and strategy

**Why this is a problem:**
The absence of a comprehensive testing strategy and low testing maturity creates significant quality risks and inefficiencies. Without unit tests, integration tests, and documented testing approaches, teams cannot ensure code quality at multiple levels, leading to defects being discovered late in the development cycle when they are most expensive to fix.

**Current situation:**
* Little to no unit tests are written across the codebase
* No integration tests are implemented to verify component interactions
* Low maturity in how testing is approached and managed across teams
* No documented testing strategy or testing plans exist
* Absence of clear guidelines on what types of testing should be performed for different scenarios
* Teams lack understanding of testing best practices and when to apply different testing approaches

**Impact on the organization:**
* **Late defect discovery:** Bugs found in later stages of development are exponentially more expensive to fix
* **Poor code quality confidence:** Without unit tests, developers cannot safely refactor or modify existing code
* **System integration risks:** Lack of integration tests means component interactions are not validated until system testing
* **Inconsistent quality practices:** Teams apply testing inconsistently without documented standards and strategies
* **Higher regression risk:** Changes to existing code cannot be confidently validated without comprehensive test coverage
* **Knowledge gaps:** Teams miss opportunities to improve testing skills and adopt industry best practices
* **Reduced development velocity:** Fear of breaking existing functionality slows down development when test coverage is inadequate
* **Customer impact:** Poor testing practices lead to more production defects affecting end users

### Test data creation challenges

**Why this is a problem:**
Effective testing requires realistic test data that represents production scenarios. When test data creation is manual, time-consuming, and dependent on business stakeholders, it creates significant bottlenecks in the testing process and reduces the effectiveness of quality assurance efforts.

**Current situation:**
* Creating test data in testing environments is very difficult and time-consuming
* Testers spend significant time chasing data from business stakeholders to support test cases
* Teams resort to manually manufacturing test data, which is inefficient and error-prone
* Desire to copy production data to testing environments exists but is hampered by data anonymization requirements
* No tooling is in place to effectively manufacture test data or automate the process
* Lack of automated data generation capabilities leads to testing delays

**Impact on the organization:**
* **Testing bottlenecks:** Slow test data creation delays testing cycles and extends release timelines
* **Resource inefficiency:** Testers and business stakeholders spend valuable time on data preparation instead of core activities
* **Test coverage limitations:** Difficulty obtaining appropriate test data restricts the scenarios that can be tested
* **Quality assurance gaps:** Inadequate test data leads to incomplete testing and higher risk of production issues
* **Business stakeholder burden:** Frequent requests for test data disrupt business users' primary responsibilities
* **Compliance risks:** Manual data handling processes may not adequately protect sensitive information
* **Inconsistent testing conditions:** Manually created test data may not accurately represent real-world scenarios
* **Delayed feedback loops:** Time spent on data preparation delays the validation of new features and bug fixes

### Security scanning and secrets management implementation

**Why this is a problem:**
The recent adoption of static analysis and security scanning has revealed critical security vulnerabilities, particularly hardcoded secrets in repositories. This creates significant security risks and compliance issues that need immediate attention while implementing proper secrets management practices.

**Current situation:**
* Only recently adopted static analysis and security scanning using SonarQube
* High priority security hotspots identified include secrets stored in code in repositories
* Currently implementing AWS Secrets Manager to remove hard-coded secrets
* Working to improve secrets rotation and management processes
* Transitioning from insecure practices to secure secrets management

**Impact on the organization:**
* **Security vulnerabilities:** Hardcoded secrets in repositories create immediate security risks and potential data breaches
* **Compliance risks:** Insecure secrets management may violate regulatory requirements and industry standards
* **Implementation overhead:** Teams must invest time in retrofitting existing code to use proper secrets management
* **Operational complexity:** Transitioning to AWS Secrets Manager requires changes to deployment and operational processes
* **Knowledge gaps:** Teams need training on secure coding practices and proper secrets management
* **Audit findings:** Security scanning results may trigger compliance audits or customer security reviews
* **Technical debt creation:** Quick fixes for hardcoded secrets may create temporary technical debt during transition
* **Development workflow impact:** New secrets management requirements may initially slow down development velocity

### Inconsistent infrastructure management

**Why this is a problem:**
Inconsistent infrastructure management through a mix of Infrastructure as Code (IaC) and manual processes creates environment drift, reduces reliability, and makes it difficult to scale operations. When environments are not fully reproducible, it leads to configuration inconsistencies and deployment challenges.

**Current situation:**
* Environments are only partially reproducible via Infrastructure as Code using Terraform
* Only the new Staging environment is created mostly from Terraform
* UAT and various Dev environments are managed via ClickOps (manual console operations) and are not consistent
* Internal discussions highlight the desire to stand up new non-production environments via fully automated processes
* Teams want to use Terraform and automation to replace current legacy environments
* Lack of standardized environment provisioning leads to configuration drift

**Impact on the organization:**
* **Environment inconsistencies:** Manual environment management leads to configuration drift and unpredictable behavior
* **Slow environment provisioning:** Manual processes significantly delay the creation of new environments
* **Increased operational overhead:** ClickOps requires more human intervention and is prone to human error
* **Difficult troubleshooting:** Inconsistent environments make it harder to reproduce and resolve issues
* **Scalability limitations:** Manual processes don't scale effectively as the organization grows
* **Risk of human error:** Manual configuration changes introduce opportunities for mistakes and misconfigurations
* **Knowledge silos:** Manual processes create dependencies on specific individuals who know how to configure environments
* **Delayed development cycles:** Slow environment provisioning can block development teams from accessing needed resources
* **Technical debt accumulation:** Legacy environments managed manually become increasingly difficult to maintain and update