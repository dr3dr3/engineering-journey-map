# Current State - Practices

These notes describe the "current state" of our organization. 

This one specifically focuses on describing:
* The engineering practices

## Current practices

Our branching strategy is clearly defined to streamline development, QA, staging, and production releases in Bitbucket and Octopus Deployment. Here’s a summary of the approach:

### 1. Branch Types & Naming Conventions

| Branch Type | Purpose | Naming Convention |
|-------------|---------|------------------|
| hotfix      | Urgent fixes applied to `master` and merged back to `develop` | hotfix/ISSUE-ID-description |
| feature     | Individual developer branch for new features                  | feature/ISSUE-ID-description |
| main        | Feature release branch for integrating new work               | version/main |
| develop     | Integration branch for QA testing                             | develop |
| staging     | Pre-production testing environment                            | staging |
| master      | Production-ready branch for UAT and release                   | master |

### 2. Workflow & Pull Request (PR) Strategy

**Feature Development Workflow**
1. Developers create a feature branch from `main`.
2. Work on the feature, commit, and push changes.
3. Create a pull request (PR) to `main` for review and approval.
4. Upon approval, merge `feature/*` into `main`.

**QA & Staging Workflow**
1. Merge `main` into `develop` for QA testing.
2. QA team verifies changes in `develop`.
3. Merge `develop` into `staging` for pre-production testing.

**Production Release Workflow**
1. Merge `staging` into `master` for UAT.
2. Create a release tag upon merging into `master`.
3. Deploy from `master` to production.

**Hotfix Workflow**
- Hotfixes go directly to `master` and are backported to `develop`.

### 3. Deployment Process

| Step                  | Source Branch | Target Branch | Purpose                  |
|-----------------------|--------------|--------------|--------------------------|
| Feature Development   | feature/*    | main         | Developer integration    |
| QA Testing            | main         | develop      | QA environment           |
| Staging               | develop      | staging      | Pre-production testing   |
| UAT Release           | staging      | master       | Final validation         |
| Production Deployment | master       | release tag  | Versioning               |

### 4. Automation & Best Practices

- Restrict direct pushes to `develop`, `staging`, and `master`.
- Require PRs for merging.
- At least 1 or 2 reviewers for PRs.
- CI/CD integration: run tests & linting before merging `main` to `develop`.
- Automate deployments to staging and production based on tags.

### 5. Release & Versioning Convention

- Uses semantic versioning: `{major}.{minor}.{patch}.{build}-{stage}`
- Alpha: `main` or `feature` branches (`1.2.0.xxx-alpha`)
- Beta: `develop` or `staging` branches (`1.2.0.xxx-beta`)
- Release Candidate: merging into `master` (`1.2.0.xxx-rc`)
- Production: after tagging from `master` (`1.2.0.xxx`)

### 6. Summary

- Developers create feature branches from `main`.
- PRs are merged into `main`, then `develop`, `staging`, and finally `master`.
- Releases are tagged only for production after merging into `master`.
- Hotfixes go directly to `master` and are backported to `develop`.
- Versioning follows alpha, beta, and rc stages before final production release.
- The deployment process is automated based on the branch to ensure seamless CI/CD integration.

