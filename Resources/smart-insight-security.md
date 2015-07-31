---
title: 'Data Security in Smart Insight'
subject: 'Resources, Security, SmartInsight'
old_url: 'http://emarsys.dev/old/resources/data-security/smart-insight-security/'
---

Emarsys Smart Insight handles data related to the ecommerce activities of our customers. This appendix describes the flow and handling of data within Smart Insight, with the focus on information security. By default, Smart Insight does *not* store any Personally Identifiable Information (PII). The product uses an anonymous external key (= a number) to associate ecommerce data with Suite contacts. Exceptions to this setup can be made upon specific customer request.

Data Exchange
-------------

### Application Access/Secure Sign-On

 Our customers access Emarsys eMarketing Suite ("Suite") via HTTPS, which is a protocol secured by SSL. For reporting purposes, Smart Insight accesses the business intelligence tool embedded into Suite via HTTPS. For this, it uses trusted host-based authentication to make ensure access is only possible from Suite front-end servers. Access to the internal network is done through VPN (Virtual Private Network). VPN accounts are always associated to individual employees, and every access is logged and can be blocked if necessary. ### API Web Service

 Smart Insight also has a Segmentation API web service, which is accessible through HTTP. However, this access is limited to the internal network. It cannot be accessed directly from external hosts. ### File Transfer

 Smart Insight uses FTPS (FTP over SSL) as the protocol for uploading eCommerce data. Once the data is uploaded, we transfer it to our load server (over FTPS) which is only accessible from the internal network. ### Data Security

 Emarsys' Data Security Policies guarantee a strict separation of all customer data, especially PII data. This section describes how the data is secured in each stage as it is processed by Smart Insight, and focuses on the data retention time. ##### Monitoring and Logging

 All file uploads and all internal processes (loads, segmentation, reports) are constantly monitored and logged. The monitoring interface is only accessible from the internal network. ##### Storage of Ecommerce Data

 Each customer receives their own database that holds ecommerce data. Since the data is physically separated, customers are not able to access each other's data. Our database servers use local disks (dedicated storage). No customer data is stored on an external or network drive. The servers for the business intelligence tool and the Segmentation API use a NetApp storage but store no customer data. As all data transfer and storage is secured, the files themselves are not encrypted. In order to ensure redundancy and high availability, the Smart Insight Greenplum database is split between two data centers in two separate physical locations, which minimizes the risk of any data loss resulting from, for example, a natural disaster. ##### Backup and Restore

 All files uploaded by customers are backed up on our load server which is only accessible from the internal network. All segment definitions created by customers are backed up daily. Customer databases are not backed up; in case of failure, all data can be restored from the eCommerce files, which are backed up. ### Data Import

 File uploads are protected by the FTPS protocol. Files are stored on the FTPS server for only a brief period of time and are then copied by an automated process to a secure, inaccessible storage. Both the transfer and the FTPS server are secured, so no additional file encryption is applied. ### Data Export

 Smart Insight does not export any data. ### Data Retention Period

- All eCommerce data files uploaded by customers are deleted from the outside-facing server within one day.
- Besides that, Smart Insight does not automatically delete any data, even if it was previously deleted from Suite.
- Data can selectively be deleted upon customer request. However, to ensure data consistency, Emarsys suggests to start from scratch and do a full upload with the corrected data.