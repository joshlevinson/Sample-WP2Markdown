---
title: 'Data Security in eMarketing Suite'
subject: 'Resources, Security'
old_url: 'http://emarsys.dev/old/resources/data-security/suite-security/'
---

The eMarketing Suite handles data related to the email recipients which is generated and sent by the platform, and is referred to as Personally Identifiable Information (PII). This page describes the flow of recipient-related data within Suite, with the focus on information security.

Data Flow
---------

 This section describes the flow of PII data within Suite in a step by step manner, the following diagrams are intended to provide a holistic view of the system architecture and the related processes.

### Suite System Architecture Overview

 The image below shows the architecture of the Suite application.

<div class="center"><div class="floatnone">[![Suite System Architecture - Layer Diagram](/assets/images/2014/04/Infosec-016-025.jpg)](/assets/images/2014/04/Infosec-016-025.jpg)</div></div><div class="center"><div class="floatnone">[![Suite System Architecture - Block Diagram](/assets/images/2014/04/Infosec-017-027.jpg)](/assets/images/2014/04/Infosec-017-027.jpg)</div></div>### Data Exchange

 Suite, as a database product, allows synchronization of recipient data with customer systems. Demographic information can be synchronized into standard fields while custom fields allow any information to be stored along recipients. The following sub-chapters describe methods to import recipient information into the system.

##### Importing into Suite Databases

<div class="center"> CSV files may be placed on WebDAV folders independently set up for each customer. By setting up automatic imports, files stored here are automatically processed by the system and the changes are propagated into the Suite database. Auto-import can also be configured to retrieve data from the FTP/SFTP/FTPS/Web server of a customer. ##### Contact API

 Suite provides a RESTful API to retrieve recipient information and update it. Customers can set up automated synchronization processes that work via the API. ##### Registration Forms

 Registration forms can be created in order to easily integrate with the database. Registration forms can be embedded into customer’s web sites, allowing the creation and update of contacts directly from the website. ##### Export

 Contact data, as well as response data, can be exported from Suite. The exported file is either placed on the Suite web server or automatically uploaded to the customer’s FTP/SFTP/FTPS server. ### Generation and Sending of Emails

 In order to generate personalized emails, the Mail Generators are accessing the main database. The generated emails are then queued on the Mail Transfer Agents for final delivery into the corresponding mailboxes. ### Tracking of Recipient Responses and Mail Reports

 Mail Reports describing whether an email has been delivered, bounced or marked as spam are collected. Suite also tracks whether an email has been opened by its Recipient and if they have clicked on any links in the email or used the unsubscribe function. This Response Data, which is associated with the recipients, is then stored in the Suite database. Visual reports are also available in the Campaign Analysis. Data Security
-------------

 Emarsys' Data Security Policies guarantee a strict separation of all customer data, especially PII data. This section describes how the PII data is secured in each stage as it is processed by Suite, and focuses on the data retention time. ### Storage of Recipient Data

 Each customer receives their own set of tables in the database that hold information on recipients and actual launches. Since the data is physically separated, customers are not able to access the data of each other. The database is only accessible from inside our server farm protected by our firewall, so the only means to access from the outside is through the application itself. The application implements password authentication, IP restriction, and two-phase authentication with SMS in order to protect customer data. The application runs on secure HTTPS channel. ### Data Import

 Data is imported into the system via WebDAV or via the FTP or web server infrastructure provided by the customer. WebDAV is accessed through HTTPS and customers are assigned their own folders, which protects their data from other customers. The WebDAV folders are password-protected. Customers may optionally encrypt their files with PGP for added security. When data is provided on a customer’s FTP/FTPS/SFTP or Web Server (HTTP/HTTPS), the application checks for new files at regular intervals and downloads them with the credentials provided by the customer. ##### Generation and Sending of Emails

 The generation of the personalized emails as well queuing for delivery is taken care of in Suite backend. ##### Tracking of Recipient Responses and Mail Reports

 The tracked Recipient Response and Mail Report data is stored in the main database. Again there are distinct tables per customer to guarantee a logical and physical separation of data. ### Data Export

 Authorized administrators of a customer may export recipient and response data from the system. Delivery of the exported CSV files is done through Suite Web servers or a customer’s FTP/FTPS/SFTP server. When Suite provides the files on the web server, the link is emailed to an email address authorized by the customer and credentials must be provided when accessing the files. Optionally files can automatically be uploaded to the FTP/FTPS/SFTP server of the customer. ##### Data Retention Period

- The data stored on Suite WebDAV is automatically deleted by Suite’s Maintenance Process after a pre-defined retention time. The maintenance process runs every day, where a check is performed to identify data needing deletion.
- By default the data retention periods are: - 7 days for the WebDAV Import folder
- Data may be optionally removed by Suite from the customer’s FTP server after processing, otherwise it is the customer’s responsibility to remove them
- All PII data which is stored in Suite databases is kept permanently in the main database and safeguarded by the mechanisms described above.

</div>