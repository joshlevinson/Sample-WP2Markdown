---
title: 'Data Security and Infrastructure Redundancy'
tags: 'Resources, Security'
old_url: 'http://emarsys.dev/resources/data-security/'
---

OverviewISO 27001 Information Security Accreditation
--------------------------------------------

[![Infosec-004-004.jpg](/assets/images/Infosec-004-004.jpg)](/assets/images/Infosec-004-004.jpg)
=================================================================================================================================================================================================================================================

 Emarsys has undergone a comprehensive third-party assessment of its data security risks including all the processes for managing information security. Emarsys has met the requirements for ISO 27001 (the international standard for Information Security Management) and is now certified as ISO 27001 compliant. This certification should inspire confidence in our customers as it demonstrates our commitment to protecting their valuable information assets, and that their data is safe in our hands. As part of this certification, Emarsys is regularly audited to ensure that these international standards are continuously met and adhered to, ensuring peace of mind for our customers.

#### What is ISO 27001?

 ISO 27001 is an internationally-recognized standard defining how corporate information security should be organized and is the foundation of all information security management. ISO 27001 describes itself as specifying the requirements for "establishing, implementing, operating, monitoring, reviewing, maintaining and improving a documented Information Security Management System within the context of the organization's overall business risks." Certification is performed by an independent body which will only issue a certificate of compliance when all the relevant requirements are met. Being certified as ISO 27001 compliant reassures partners and customers that Emarsys meets the very highest standards of security, as laid out by the governing body. You can read more about ISO 27001 at: <http://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.htm?csnumber=42103>. A copy of our ISO certificate is available on demand from Emarsys Support.

Emarsys Security Overview
-------------------------

 The highest priority for Emarsys is system security: guaranteeing the safety of customer data while offering a stable and responsive application that can be accessed by customers at any time. When working with suppliers, Emarsys pays particular attention to ensuring that the security policies of these third parties (measures and implementation) meet Emarsys' own standards and are implemented accordingly. Security at Emarsys eMarketing Systems AG can be categorized as follows:

- Application security
- Infrastructure security
- Email security
- Access security
- Disaster recovery & Business Continuity Planning

### Application security

 Our software development process follows a strict and secure coding principle. Application security at Emarsys is dealt with by a Secure Coding Committee (which consists of the heads of software development, testing, and software security officers) which defines and implements principles and procedures that adhere to industry-standard secure development.

<div class="center"><div class="floatnone">[![Internal software development process](/assets/images/Infosec-004-0042.jpg)](/assets/images/Infosec-004-0042.jpg)</div></div> The development team has a thorough understanding of existing infrastructure components, which is necessary to ensure that the deployment of the software is, firstly, operationally functional and, secondly, will not weaken the security of any existing environment. Development teams also participate in regular security trainings. All of our software development goes through internal security testing by Emarsys before undergoing independent assessment by external IT security firms that specialize in software and system security.

### Infrastructure security

##### Physical security

 Emarsys production environments are hosted at high-security data centres that conform to ISO 27001 Information Security standards. To ensure continuity of service the data centres provide the following:

- secured electricity through uninterrupted power supply units and backup generators
- 24/7/365 access control and surveillance
- automatic fire detection system and sprinklers
- redundant climate control and cooling systems
- high availability and guaranteed SLAs

##### Firewall

 Emarsys operates high-performance redundant firewall clusters which are kept up to date with automated security updates, and have regular performance tuning performed on them.

<div class="center"><div class="floatnone">[![Firewall stack: Crossbeam Checkpoint Firewall with redundancy](/assets/images/Infosec-006-008.jpg)](/assets/images/Infosec-006-008.jpg)</div></div>##### Operating system security

 Emarsys exclusively uses a managed environment built of UNIX operating systems which offer the highest levels of performance and stability. System updates are implemented regularly to ensure that all our systems always have the latest security patches, and all accounts are secured using strong passwords. As an additional security measure direct root access has been disabled, and is not possible.

##### Database security

 Each database server cluster is located in its own local subnet, all of which have access severely restricted so that only personnel with the correct authorization can access them.

<div class="center"><div class="floatnone">[![Database Cluster: Veritas Cluster Servers with redundancy](/assets/images/Infosec-007-010.jpg)](/assets/images/Infosec-007-010.jpg)</div></div>##### Maintenance and monitoring

 All systems are maintained and monitored in accordance with manufacturers’ recommendations on a 24/7/365 basis. Monitoring includes:

- Ensuring system availability (hardware, services, applications and connectivity)
- Performing regular log file analysis
- Performing regular firewall analysis
- Implementing security updates

### Email security

 Emarsys uses the Transport Layer Security (TLS) encryption protocol to encrypt all emails sent through its infrastructure. This is the industry standard for email security and ensures that messages cannot be read by third parties while in transit. In a recent [Transparency Report](http://www.google.com/transparencyreport/saferemail/?hl=en-US#region=150) by Google, Emarsys was listed as one of only two European providers to use such encryption technology.

### Access security

##### Data encryption

 Emarsys uses both a 128-bit SSL encryption, certified by VeriSign, and 2048-bit or longer RSA public keys in order to ensure the highest level of security of data transfers for our customers.

##### **Request validation and authentication**

 Escher is a stateless HTTP request-signing specification to provide secure authorization and request validation. It adds an additional security layer and an authentication layer over HTTPS. The algorithm is based on [Amazon’s AWS4 authentication](http://docs.aws.amazon.com/AmazonS3/latest/dev/RESTAuthentication.html). The protocol ensures the requests' integrity, and also provides a solution for pre-signing URLs with expiration time.

##### Access management

 User access requires authentication using a valid username and a strong password in accordance with our password policy. In addition, access to all Emarsys services may be restricted by IP so only users at authorized locations can use them. If a user tries to log in from an untrusted location with IP restriction enabled we offer two-factor authentication, so login is only possible after the user enters a one-time password generated by an authenticator application, or received via SMS or email. Every authentication attempt is recorded and an automatic procedure takes care of temporarily locking out accounts with too many failed password attempts. Our users are also required to change their password regularly. Our password policy will not let them change to a password they recently used.

##### Emarsys employee data access

 All customer data is owned solely by the respective customer, no one else. The only people at Emarsys that have access to that data are members of the Operations team tasked with maintaining and monitoring the application, as well as Client Services personnel who work with customers on optimizing their marketing campaigns. Confidentiality is ensured by non-disclosure agreements in Emarsys employee contracts, as well as the strict guidelines laid down in accordance with the ISO 27001 requirements with regards to how confidential information is stored and processed internally. Any information provided by our customers automatically falls under this confidentiality.

##### Geographical data regulations

 Emarsys' servers holding the customer data are all based within the EU, meaning that all laws and regulations relating to data handling on a national and federal level are observed in accordance with the EU regulations.

### Disaster Recovery & Business Continuity Planning

##### High availability

 Emarsys maximizes system stability across data centres by employing cross-site redundancy by design, as well as redundancy within each data centre for all network components including:

- Application servers
- Mail servers
- Database servers (Veritas cluster for DB failover; VMWare cluster)
- Load balancers
- Firewalls

<div class="center"><div class="floatnone">[![Storage Clusters with Synch Mirror and Redundancy](/assets/images/Infosec-008-012.jpg)](/assets/images/Infosec-008-012.jpg)</div></div> Provider-independent dedicated IP addresses with PGP routers allow Emarsys to switch traffic to an alternative data centre on the fly if the need arises without any significant impact on performance.

##### Backup

 All user data in our databases is backed up daily and archived using a dedicated file storage system where all backups are encrypted and then transferred to a fire-proof offsite storage location. These backups are also mirrored at an alternative data centre to ensure business continuity is maximized.

<div class="center"><div class="floatnone">[![Backup with Replication](/assets/images/Infosec-009-014.jpg)](/assets/images/Infosec-009-014.jpg)</div></div><div style="page-break-after: always;"></div>Emarsys Network Overview
------------------------

 The image below gives an overview of the Emarsys network.

<div class="center"><div class="floatnone">[![Emarsys Network Overview](/assets/images/Infosec-010-016.jpg)](/assets/images/Infosec-010-016.jpg)</div></div>