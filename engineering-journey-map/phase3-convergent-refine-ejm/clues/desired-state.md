# Desired State

These notes describe the "desired state" being the current priorities and work in flight for improvements to business processes, tooling, and capabilities. These must be reflected in the engineering journey map under the Opportunities section.

## Environments

* Want to be able to provision environments from scratch fully using Terraform
* Want to prove this in the Staging environment first, by fully destroying all resources and setting them up fresh solely by using Terraform
* Thereafter want to setup fresh environments for UAT and Development (replacing ENG environments)
* Want to explore the potential for have ephemeral environments, that are spun up for each engineering squad (so can test in isolation) and destroyed after testing is complete once code is merged to trunk
* Want to only have environments running when needed and scaled down when not needed, to save infrastructure costs


## Automated Testing

* Want to eliminate manual testing effort, except for some limited exploratory testing
* Want 100% of our regression test cases automated using Playwright for end-to-end testing and other test automation for integration/contract testing and for unit testing
* Want the ability to run the automated testing frequently and have them complete quickly, so that feedback is fast for Engineers
* Expect test automation will help improve test coverage and overall quality of code deployed

## Test Data Management

* Want to automate the process of taking data from Production environment into lower environments, like Staging and Development
* Want to automate the generation of new data needed for automated test cases
* Want non-prod environments to be more reflective of production environment
* Want sufficient test data to cover various configurations used by various customers

## Monitoring

* Want Engineers involved in helping create application/service observability monitoring and dashboards
* Want Engineering and IT Operations to be using the same observability monitoring and dashboards
* Want the level of logging done consistently across all applications and services
* Want the level of logging for errors to be limited only to errors that must be resolved

## Technical Debt ("Tech Debt")

* Want tech debt items identified and managed in Jira
* Want to maintain an inventory of tech debt items to highlight the volume and importance of them
* Want to way to prioritize tech debt so we can focus on eliminating those with most impact
* Want to be able to escalate the importance/value of tech debt as compared to new feature development

## Better alignment between Engineering and IT Operations teams

* Want IT OPS teams to be more familiar with code changes being deployed
* Want Engineerring teams to be more responsible for production performance
* Want faster feedback to Engineering teams on production issues
* Want to have better collaboration between Engineering and IT Ops in preventing production issues

## Smaller work items that are more clearly defined

* Want to breakdown work into smaller items that can be completed in a few days
* Want to improve the capababilities of Engineering teams to slice stories/work into smaller items
* Want better architecture guidance on how to break work down whilst ensuring overall alignment

## Static code analysis and security scanning

* Want to implement SonarQube for code analysis, code quality, and security/vulnerability scanning
* Want to use SonarQube to identify and prioritize technical debt
    * Example: Identify critical security vulnerabilities that engineering teams must addrress
    * Example: Identify out-dated components that should be updated to later versions
    * Example: Measure code quality including test coverage and adherence to coding standards

## Adopt and use feature flags for safer deployments

* Want to adopt the practice of using feature flags to have more control over production deployments
* Want to be able to do canary releases of new features to some customers, before enabling for all customers
* Want to be able to contain legacy customizations using feature flags, so can still deploy a single package (rather than numerous customized packages)
* Want to be able to use feature flags to turn-off new features if issues are found in production (to avoid doing rollbacks)

## Internal Developer Portal (IDP)

* Want to use Atlassian Compass as the internal developer portal used by all Engineers and IT Operations
* Want the IDP to be the "single pane of glass" that shows recent deployments, changes in progress, links to observability, and various scorecards for code quality / security / adherence to coding standards.