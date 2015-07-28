---
title: 'Data Security in Emarsys Broadcast'
tags: 'Resources, Security'
old_url: 'http://emarsys.dev/resources/data-security/broadcast-security/'
---

Emarsys Broadcast (referred to as Broadcast or Broadcast system) handles data related to the email recipients which is generated and sent by the platform, and is referred to as Personally Identifiable Information (PII). This appendix describes the flow of recipient related data within Emarsys Broadcast, with focus on information security.

Access Security
---------------

 In addition to the default level of access security, the Emarsys Broadcast web application also offers Two-Factor Authentication as a secure login mechanism.

### Two-Factor Authentication

 Two-Factor Authentication (2FA) in Emarsys Broadcast uses SMS sent to a dedicated mobile phone for authentication. If this feature is enabled, all users (including admins) are required to register their phone number upon their next login and immediately verify a 2FA code.

#### Safeguards

 In addition to the standard 2FA functionality, the following safeguards are also in place:

- The user may use each code received once only, guarding against replay attacks.
- The user only has a limited time window (a few minutes) to use the code, to invalidate codes left unused after abandoned login attempts.
- The login service tolerates a limited number of failures to provide the correct code, then fails hard and requires the user to log in again. This is to prevent brute force attacks against the code sent.
- To prevent denial of service and other brute force attacks against the login service, the number of login attempts and 2FA code texts sent per time and user is also limited.

Data Flow
---------

 This section describes the flow of PII data within Broadcast in a step by step manner, the following diagrams are intended to provide a holistic view of the system architecture and the related processes.

### Broadcast System Architecture Overview

 The image below shows the architecture of the Broadcast application.  

<div class="center"><div class="floatnone">[![Broadcast System Architecture - Layer Diagram](/assets/images/Infosec-011-018.jpg)](/assets/images/Infosec-011-018.jpg)</div></div>  

<div class="center"><div class="floatnone">[![Broadcast System Architecture - Block Diagram](/assets/images/Infosec-012-020.jpg)](/assets/images/Infosec-012-020.jpg)</div></div>### Data Upload

 In order for Recipient data to be used in Broadcast it needs to be uploaded to Emarsys Broadcast's File Exchange area, which is made up of several folders, such as Incoming, Invalids, etc.. Upload Recipient Data in CSV format (Comma Separated Values) to the folder called Incoming. The file exchange is handled by an OpenSSH daemon and supports the SFTP and SCP file transfer protocols.

### Importing into Broadcasting Databases

 The customer notifies the Broadcast system when an upload is finished either by placing a Control File on the File Exchange, or by making a corresponding import-call to the Broadcast Webservice API. The Broadcast system will copy the Recipient Data into the Broadcasting Databases, and after the Recipient Import has finished the CSV file is moved to either the Finished or Invalids.

### Generation and sending of emails

 In order to generate the personalized emails the Recipient Data is pushed from the Broadcasting Databases to the Mail Generator servers. The generated emails are then queued on the Mail Transfer Agents for final delivery into the corresponding mail boxes.

### Tracking of Recipient Responses and Mail Reports

 Mail Reports describing whether an email has been delivered, bounced or marked as spam are collected. The Broadcast system also tracks whether an email has been opened by its Recipient and if they have clicked on any links in the email, or used the unsubscribe function. This Response Data which is associated with the Recipients is then stored in the Broadcasting Databases.

### Export of Response Data

 At regular intervals the Broadcast's Reponse Data Export process dumps the Response Data into CSV files that are put in the Exports folder on the File Exchange.

### Download of Response Data

 The Response Data can be picked-up and downloaded by the customer from the File Exchange.

Data Security
-------------

 Emarsys' Data Security Policies guarantee a strict separation of all customer data, especially PII data. This section describes how the PII data is secured in each stage as it is processed by Emarsys Broadcast, and focuses on the data retention time.

### Data Import

 The only way to upload PII data to Emarsys Broadcast is by using the File Exchange which assures compliance through using secure file transfer protocols. The OpenSSH-based File Exchange uses Sandboxes, or Jails, which are areas within a Linux Kernel-Based Virtual Machine (KVM) on our web servers. These specific areas isolate each dataset so that it is virtually impossible for malicious users to break out of there are and then access the Broadcast web servers, or other customer data. Each customer has its own user account, and only this user account has access to their folders where data is being kept, with the only exception to this being Broadcast's system user account. File Exchange authentication is possible using either a password or a hashkey. In addition, imported Recipient Data can be encrypted using PGP as an optional extra level of security, in case the File Exchange would ever be compromised.

### Importing to Broadcasting Databases

 During the import process the CSV data is decrypted and copied to the Broadcasting Databases (DBs). These DBs are part of Broadcast's backend which is located in a different subnet and access is only possible through a firewall. Each Recipient Import process copies the data to a newly created DB table. This guarantees that Recipient Data from one email campaign is clearly separated from other campaigns and thus also from other customer’s data.

### Generation and sending of emails

 The generation of the personalized emails as well queuing for delivery is taken care of in Broadcast's backend.

### Tracking of Recipient Responses and Mail Reports

 The tracked Recipient Response and Mail Report data is stored in the Broadcasting DBs (Broadcast's backend). Again there are distinct tables per email campaign to guarantee a logical and physical separation of data.

### Export of Response Data

 The Response Data is saved as CSV files to the customer’s Export folder on the File Exchange and is only accessible through the customer's user account. As with the Data Import, the exported data can optionally be encrypted using PGP.

### Data Retention Period

 The data stored on the File Exchange is automatically deleted by Broadcast’s Maintenance Process after a pre-defined retention time (configurable per customer account, done during setup). The maintenance process takes place every five minutes, where a check is run to identify data needing deletion. By default the data retention periods are

- 2 days for the *Incoming* folder
- 1 day for the *Finished* folder
- 7 days for the *Invalids* folder
- 2 weeks for Response Data in the *Export* folder
- 4 weeks for data associated with an email campaign (lifetime data)
- All PII data which is stored in Broadcast's databases is: - only kept for the duration of the corresponding email campaign, and is referred to as its lifetime (can be configured per customer account).
- After this lifetime has expired, all PII data which has been imported and associated with a campaign will be deleted from the DBs.