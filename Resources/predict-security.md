---
title: 'Data Security in Predict'
subject: 'Resources, Security'
old_url: 'http://emarsys.dev/resources/data-security/predict-security/'
---

Emarsys Predict uses the Amazon Cloud to host its technology. For any additional queries regarding compliance and security beyond what is included here - please refer to their resources here: <https://aws.amazon.com/compliance/> <https://aws.amazon.com/security/>

Architectural Security
----------------------

 With Emarsys Predict we minimize exposure to security vulnerabilities at the architectural level as follows: 1. No Personally Identifiable Information (PII), such as email addresses, names, etc. is collected or used by the recommender. Predict relies on anonymous random identifiers (issued as cookies) to track individual visitors without knowing who they really “are”
2. The frontend serving infrastructure only retains a day’s worth of behavior logs (approx.), and then archives them by sending the data to be stored and processed in a separate, isolated system.

Infrastructure Security
-----------------------

 Our infrastructure is hosted on Amazon Web Services (AWS), which provides one of the most secure cloud computing environments in terms of both physical and logical security. ### Firewalls

 All our Predict servers are secured behind firewalls provided by the AWS infrastructure and ports are only opened for external services as required only once an explicit request has been made. ### Access Security

 Our server infrastructure is regularly updated with the latest updates and patches for security vulnerabilities. **Secure Access:**- Infrastructure changes are managed via secure HTTPS access
- Hosts are managed via encrypted SSH connections
 
**Unique users:**- All administrative access is tied to unique user accounts (as part of the security policy)
 
**Multi-factor authentication:**- Infrastructure administrative access is tied to MFA tokens.
 
**Change tracking:**- All infrastructure changes are logged via Amazon CloudTrail.

Disaster Recovery & Business Continuity Planning
------------------------------------------------

### High availability

 Our services are hosted, and run in multiple independent data centers (Availability Zones) to maximize availability and continuity of service. ### Backup Facilities

 Predict uses redundant and geographically replicated backups via Amazon S3 to ensure the safety of data, and continuity of service.