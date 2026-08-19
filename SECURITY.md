# Security Policy

Security is an important part of the software development lifecycle at Qubit Data Innovations.

We appreciate responsible disclosure of security vulnerabilities and encourage researchers, customers, developers, and users to report potential security issues privately.

## Reporting a Vulnerability

**Do not report security vulnerabilities through public GitHub Issues, Discussions, or Pull Requests.**

If the repository has GitHub Private Vulnerability Reporting enabled, use the **Report a vulnerability** option available in the repository's **Security** section.

Otherwise, report the vulnerability privately by email:

**[develop@qubitdi.com](mailto:develop@qubitdi.com)**

Please include as much relevant information as possible.

## Information to Include

A security report should contain, when applicable:

* Repository or application affected
* Vulnerability description
* Potential impact
* Steps to reproduce
* Proof of concept
* Affected versions
* Environment where the vulnerability was identified
* Relevant logs or screenshots
* Suggested remediation, if known

Do not include credentials, passwords, API keys, access tokens, private keys, personal data, or production data unless specifically requested through an approved secure communication channel.

## Responsible Disclosure

We ask security researchers and reporters to:

* Report vulnerabilities privately
* Avoid accessing, modifying, deleting, or downloading data that is not necessary to demonstrate the vulnerability
* Avoid disrupting production systems or services
* Avoid social engineering, phishing, or attacks against employees, customers, or third parties
* Allow reasonable time for investigation and remediation before public disclosure
* Act in good faith and minimize potential impact

## Response Process

When a vulnerability report is received, Qubit Data Innovations will aim to:

1. Acknowledge receipt of the report.
2. Review and validate the reported vulnerability.
3. Determine severity and potential impact.
4. Develop and test an appropriate remediation.
5. Coordinate deployment of the fix.
6. Communicate relevant updates to the reporter when appropriate.
7. Publish advisories or remediation information when necessary.

Response and remediation timelines may vary depending on severity, complexity, affected systems, and third-party dependencies.

## Security Severity

Security findings may be classified based on their potential impact.

### Critical

Issues that may result in severe compromise, such as:

* Remote code execution
* Authentication bypass affecting privileged accounts
* Exposure of highly sensitive information
* Compromise of production infrastructure
* Significant unauthorized access

### High

Issues with significant security impact that require prompt remediation.

### Medium

Issues with limited impact, requiring specific conditions or providing partial compromise.

### Low

Issues with minimal security impact or defense-in-depth improvements.

## Credentials and Secrets

Never commit sensitive information to a Qubit Data Innovations repository, including:

* Passwords
* API keys
* Access tokens
* Private keys
* Database credentials
* Authentication secrets
* Production connection strings
* Private certificates
* Sensitive `.env` files

Approved secret-management mechanisms must be used instead.

If a credential or secret is accidentally committed, consider it compromised and notify the appropriate repository administrator immediately.

Deleting the secret in a later commit is not sufficient because the value may remain in Git history.

## Dependency Vulnerabilities

Dependencies should be monitored for known vulnerabilities.

When a vulnerable dependency is identified:

* Assess whether the project is affected
* Determine the severity and exposure
* Upgrade or replace the dependency when appropriate
* Test the remediation
* Document significant compatibility or deployment considerations

## Supported Versions

Supported versions vary by repository and product.

Individual repositories may define specific supported versions in their own `SECURITY.md`. When repository-specific security guidance exists, it takes precedence over this organization-wide policy.

## Scope

This policy provides the baseline security reporting process for repositories owned by Qubit Data Innovations.

Individual projects may introduce additional security requirements based on:

* Application architecture
* Data sensitivity
* Customer requirements
* Regulatory requirements
* Infrastructure
* Deployment environment
* Risk classification

---

**Qubit Data Innovations, S.A.**
Software engineering, data and digital solutions.
