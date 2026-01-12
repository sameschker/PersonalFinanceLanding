# Security, Privacy, and Compliance Policy

**Project Type:** Personal, single-user application
**Data Scope:** Personal financial data belonging exclusively to the project owner

---

## 1. Scope and Project Model

This project is a personal, single-user application maintained and operated solely by the project owner. The application only accesses and processes the project owner’s own financial account data via Plaid. No third-party users, employees, contractors, or external administrators have access to the system or its data.

All data is stored locally on the project owner’s personal laptop in encrypted form.

---

## 2. Identity and Access Management (IAM)

### 2.1 Centralized Identity and Access Management

Access to the project is centrally managed through:

* The operating system user account on the personal laptop
* GitHub account controls for source code access
* Local encryption key management tied to the device user account

Only a single identity (the project owner) has access to the system. No shared or secondary accounts exist.

**Attestation:** The organization has implemented centralized identity and access management solutions appropriate to its single-user model.

---

### 2.2 Access Control Policy

The project enforces strict access controls:

* Only the project owner can authenticate to the system
* Local operating system permissions restrict access to encrypted data
* Secrets, tokens, and credentials are stored securely and not committed to source control

The principle of least privilege is applied by limiting all access exclusively to the single authorized user.

**Attestation:** The organization has implemented a defined and documented access control policy.

---

### 2.3 Periodic Access Reviews and Audits

Because the project has a single authorized user, access reviews consist of:

* Periodic verification that no additional user accounts, credentials, or access paths exist
* Review of GitHub and system access settings at least quarterly

**Attestation:** The organization performs periodic access reviews and audits appropriate to its operational scope.

---

### 2.4 Access De-Provisioning

There are no employees, contractors, or transferred users. If access credentials are compromised or rotated:

* Tokens and secrets are immediately revoked and regenerated
* Local encryption keys can be rotated by re-encrypting stored data

**Attestation:** The organization has implemented access de-provisioning and modification controls appropriate for a single-user environment.

---

## 3. Zero Trust Architecture

The project follows Zero Trust principles within its scope:

* No implicit trust is granted based on device or location
* Access requires successful authentication to the operating system and application
* All external API access (including Plaid) is authenticated using scoped credentials
* Data is encrypted at rest and in transit

**Attestation:** The organization has implemented a zero trust access architecture appropriate for a personal application.

---

## 4. Authentication and MFA

### 4.1 Multi-Factor Authentication (MFA)

Multi-factor authentication (MFA) is enforced where supported:

* MFA is enabled on the GitHub account
* MFA is enabled on the Plaid dashboard account
* MFA is enabled on the operating system or device login, where available

Because the application is single-user and does not support external consumer accounts, authentication applies only to the project owner.

**Attestation:** The organization has implemented MFA on the application and supporting services where Plaid Link is deployed and managed.

---

### 4.2 Secure Tokens and Certificates

The project uses:

* Secure API tokens for Plaid access
* Encrypted storage for credentials and secrets
* TLS for all network communication

Plaintext secrets are not stored in source code or public repositories.

**Attestation:** The organization uses secure tokens and certificates for authentication.

---

## 5. Vulnerability and Patch Management

### 5.1 Vulnerability Remediation SLA

Identified vulnerabilities are addressed according to the following remediation targets:

| Severity | Target Resolution         |
| -------- | ------------------------- |
| Critical | Within 7 days             |
| High     | Within 14 days            |
| Medium   | Within 30 days            |
| Low      | As reasonably practicable |

The project owner monitors security advisories for dependencies and development tools.

**Attestation:** The organization patches identified vulnerabilities within a defined SLA.

---

### 5.2 End-of-Life (EOL) Software Management

The project monitors software components for end-of-life (EOL) status by:

* Tracking dependency updates
* Reviewing deprecation and security notices
* Updating or replacing unsupported software in a timely manner

**Attestation:** The organization monitors EOL software and maintains EOL management practices.

---

## 6. Data Encryption, Retention, and Deletion

### 6.1 Data Encryption

All locally stored data is encrypted at rest using operating system–level encryption and/or application-level encryption. Data in transit is protected using TLS.

---

### 6.2 Data Retention and Deletion Policy

* Only the project owner’s personal financial data is stored
* Data is retained solely for personal use and functionality
* Data can be deleted at any time by the project owner
* Upon deletion, encrypted files are securely removed from the system

**Attestation:** The organization has implemented a data retention and deletion policy.

---

## 7. Privacy Policy

A public Privacy Policy is published that discloses:

* The collection of personal financial data belonging solely to the project owner
* The use of Plaid for account connectivity
* Data storage, encryption, and deletion practices

**Attestation:** The organization has published a privacy policy.

---

## 8. Information Security Policy (ISP)

This document constitutes the project’s Information Security Policy and defines the security controls governing access, encryption, vulnerability management, and data protection.

The policy is reviewed periodically and updated as the project evolves.

**Attestation:** The organization has created and maintains an Information Security Policy.

---

## 9. Compliance Statement

As of the date listed above, the project owner attests that the controls described in this policy are implemented in good faith and are appropriate for a single-user, personal application integrating with Plaid.

