# CI/CD pipeline

CI/CD pipeline automates the process of building, testing and deploying the code so that the final software is delivered quickly and safely to the production. Below is the breakdown of the key stages of the CI/CD pipeline.


## 1. Source Stage

- What it does: Monitors the source code repository (like GitHub).
- Trigger: Changes such as a new commit, PR, or merge.
- Tools: GitHub, GitLab, Bitbucket.


## 2. Build Stage

- Purpose: Converts source code into executable artifacts.
- Includes:
  - Dependency installation
  - Compilation (if needed)
  - Packaging the application
- Tools: Maven, Gradle, npm, Docker.


## 3. Test Stage

- Objective: Ensure code quality and functionality through automated tests.
- Types of Tests:
  - Unit tests
  - Integration tests
  - End-to-end tests
- Tools: JUnit, PyTest, Selenium, Cypress.


## 4. Artifact Storage
- Why it's important: Stores build outputs for consistent deployments.
- Tools: Nexus, Artifactory, GitHub Packages, AWS S3.


## 5. Deployment Stage
- Job: Deploys code to staging or production environments.
- Can be:
  - Manual approval based
  - Fully automated (in CD)
- Tools: GitHub Actions, Jenkins, CircleCI, ArgoCD, Helm.


## 6. Monitoring and Feedback
- Goal: Track app performance and catch issues early.
- Metrics Tracked:
  - Downtime
  - Error rates
  - Performance lags
- Tools: Prometheus, Grafana, ELK Stack, Sentry.

A strong CI/CD pipeline ensures the code is error free, team collaboration, deployment confidence.