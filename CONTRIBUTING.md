# Contributing to Qubit Data Innovations Projects

Thank you for contributing to Qubit Data Innovations.

This document defines the baseline engineering and collaboration practices for repositories within the organization. Individual repositories may define additional requirements when necessary.

## 1. General Principles

All contributions should prioritize:

* Security
* Code quality
* Maintainability
* Clear documentation
* Automated testing
* Traceability of changes
* Minimal and focused changes

Do not include credentials, API keys, tokens, certificates, passwords, personal data, production data, or other sensitive information in source code, commits, issues, or pull requests.

## 2. Branching Strategy

The `main` branch represents the stable version of the project.

Development work should be performed in dedicated branches.

Use the following naming conventions:

```text
feature/<short-description>
fix/<short-description>
hotfix/<short-description>
refactor/<short-description>
chore/<short-description>
docs/<short-description>
test/<short-description>
```

Examples:

```text
feature/user-authentication
fix/invoice-calculation
hotfix/login-production
refactor/customer-service
chore/update-dependencies
docs/api-documentation
test/payment-service
```

Branch names should:

* Use lowercase letters
* Use hyphens to separate words
* Be concise and descriptive
* Avoid personal names
* Avoid generic names such as `test`, `new`, `final`, or `changes`

## 3. Direct Changes to `main`

Direct development on `main` should be avoided.

The standard workflow is:

```text
Issue / Task
    ↓
Working Branch
    ↓
Development
    ↓
Commit
    ↓
Push
    ↓
Pull Request
    ↓
Code Review
    ↓
Validation / Tests
    ↓
Merge
    ↓
main
```

Changes should normally reach `main` through a Pull Request.

## 4. Commit Messages

Commit messages must clearly explain the purpose of the change.

Qubit Data Innovations follows a Conventional Commits-style format:

```text
<type>: <description>
```

Common types:

```text
feat:     New functionality
fix:      Bug fix
refactor: Code restructuring without changing behavior
docs:     Documentation changes
test:     Test-related changes
chore:    Maintenance or dependency changes
perf:     Performance improvements
build:    Build system or dependency changes
ci:       CI/CD configuration changes
```

Examples:

```text
feat: add customer authentication endpoint
fix: correct invoice total calculation
refactor: simplify payment validation service
docs: update API integration instructions
test: add authentication service tests
ci: add backend validation workflow
```

Commit messages should be concise, meaningful, and written in English.

Avoid messages such as:

```text
changes
fix
update
test
final
working
stuff
```

## 5. Pull Requests

Every significant change should be submitted through a Pull Request.

Pull Requests should:

* Have a clear title
* Explain what changed and why
* Reference the related issue or task when applicable
* Be focused on a single objective
* Include testing information
* Document configuration or deployment changes
* Identify breaking changes
* Include screenshots when UI changes are involved
* Avoid unrelated modifications

Use the organization Pull Request template when available.

## 6. Code Review

Pull Requests should be reviewed before merging whenever another qualified team member is available.

Reviewers should evaluate:

* Correctness
* Security
* Maintainability
* Architecture
* Error handling
* Test coverage
* Performance implications
* Documentation
* Backward compatibility
* Configuration changes

Review comments should be technical, respectful, and focused on improving the implementation.

## 7. Testing

Changes should be tested before requesting a merge.

Depending on the project, this may include:

* Unit tests
* Integration tests
* API tests
* UI tests
* Regression tests
* Security validation
* Manual functional testing

Existing tests should continue to pass.

New functionality should include appropriate tests whenever practical.

## 8. Security

Never commit:

* Passwords
* API keys
* Access tokens
* Private keys
* Certificates containing private material
* Database credentials
* Production connection strings
* Authentication secrets
* Personal or confidential information
* Sensitive environment files

Sensitive configuration must use approved mechanisms such as:

* GitHub Secrets
* Environment variables
* Secret management platforms
* Deployment environment configuration

Files such as `.env` containing real credentials must not be committed.

If sensitive information is accidentally committed, notify the repository administrator or security responsible immediately. Removing the file in a later commit does not automatically remove the secret from Git history.

## 9. Configuration and Environments

Environment-specific configuration should remain separate from application source code.

Projects may define environments such as:

```text
Development
QA
Staging
Production
```

Production credentials and configuration must never be reused for local development.

Any new environment variable introduced by a change should be documented.

## 10. Dependencies

Before adding a new dependency:

* Confirm that it is necessary
* Prefer actively maintained projects
* Review known security concerns
* Avoid unnecessary duplication
* Evaluate licensing implications when applicable

Dependency updates should be tested before merging.

## 11. Documentation

Update documentation when a contribution changes:

* API behavior
* Configuration
* Environment variables
* Installation procedures
* Deployment procedures
* Database requirements
* User-facing behavior
* Public interfaces
* Architecture decisions

Code should be self-explanatory whenever possible, with comments used to explain important decisions rather than obvious implementation details.

## 12. Database Changes

Database changes should be versioned and traceable.

Schema changes, migrations, stored procedures, indexes, or data transformations should include:

* Purpose of the change
* Migration instructions when required
* Rollback considerations
* Compatibility considerations
* Required deployment order when applicable

Destructive database operations require additional review.

## 13. CI/CD

Changes to CI/CD pipelines, deployment workflows, infrastructure, secrets, runners, or production environments should receive additional review when possible.

The `devops` team should be involved in changes that affect:

* GitHub Actions
* CI/CD workflows
* Infrastructure
* Deployment automation
* Environment configuration
* Runners
* Secrets and variables
* Production releases

## 14. Team Responsibilities

Qubit Data Innovations currently organizes engineering work through the following teams:

* `backend` — Backend development and API services
* `frontend` — Frontend development and user interface applications
* `apps` — Application development for mobile, desktop and other client platforms
* `devops` — Infrastructure, CI/CD, deployments, environments and platform operations
* `qa` — Quality assurance, software testing, validation and regression testing

Repository-specific ownership and permissions may vary depending on the project.

## 15. Issues

Use the appropriate Issue template when reporting work.

### Bug Reports

A bug report should include:

* Severity
* Affected component
* Environment
* Steps to reproduce
* Expected behavior
* Actual behavior
* Relevant sanitized logs
* Additional context

### Feature Requests

A feature request should explain:

* The problem or business need
* Proposed solution
* Acceptance criteria
* Alternatives considered
* Relevant technical or business context

## 16. Breaking Changes

Breaking changes must be clearly identified in the Pull Request.

Include:

* What will break
* Who or what is affected
* Migration requirements
* Deployment considerations
* Compatibility implications

Breaking changes should not be introduced silently.

## 17. Repository-Specific Rules

Individual repositories may contain their own `CONTRIBUTING.md`.

When repository-specific guidance exists, it takes precedence over this organization-wide baseline for that repository.

---

**Qubit Data Innovations, S.A.**
Software engineering, data and digital solutions.
