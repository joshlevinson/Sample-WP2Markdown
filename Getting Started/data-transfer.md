---
title: 'Suite Data Transfer - Overview'
tags: 'DataManagement, Getting Started, GettingStarted_Suite'
old_url: 'http://emarsys.dev/getstarted/contact-data/data-transfer/'
---

There are a number of ways to transfer data in and out of Suite. Click the links below to find out more (they are listed inÂ order of complexity):

- [Importing data](/Getting%20Started/import-data.md "Importing Data into Suite") via the Suite interface
- [Exporting data](/Getting%20Started/export-data.md "Exporting Data from Suite") via the Suite interface
- [Using web forms](/Getting%20Started/web-forms.md "Using Web Forms to Import Data") to import data
- [Using HTTPS requests](/Getting%20Started/http-requests.md "Using HTTPS Requests to Import Data") to import data
- [Using the Suite API](/Getting%20Started/api-transfer.md "Using the Suite API to Transfer Data") to transfer data
- [Synchronizing the Suite database](/Getting%20Started/connect.md "Integrating with External Applications") with an external database

 These are described in more detail below. When deciding on the most suitable transfer method, it is also important to consider which type of data will be transferred. This can be:

- **Contact properties** These are based on data fields and can be imported, exported and synchronized with an external application. The field names must be mapped between Suite and any external application to ensure that the values are transferred correctly. Furthermore, at least one field must be defined as an external key to ensure that the properties of the right contact are updated.
- **Email responses** Opens, clicks and other responses are collected by Suite and can only be exported or synchronized with another application.
- **External data sets** (such as web shop purchases) These can comprise any kind of information related to your eMarketing activities and are handled by the Smart Insight module.