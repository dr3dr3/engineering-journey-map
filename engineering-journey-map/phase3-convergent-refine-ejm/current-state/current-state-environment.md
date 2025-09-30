# Current State

These notes describe the "current state" of our organization. 

This one specifically details the technical environment, including:

* The type of software products being created and maintained by Engineering teams
* The source code repositories
* The enivornments used and their purposes (e.g. Development, Staging, Production)

## Current code bases that form product

### A total of 60 code repositories
* One primary legacy solution based on forms builder that runs on windows server
* Around 40x micro-services
* Around 5x code repositories for platform engineering (i.e. terraform)

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
