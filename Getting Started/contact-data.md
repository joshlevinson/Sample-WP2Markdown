---
title: 'Managing Your Contact Data'
subject: 'Getting Started, SuiteContacts'
old_url: 'http://emarsys.dev/getstarted/contact-data/'
---

The most important decision to make when starting with Suite is where and how you will be managing your contact data. By this we mean where you will collect new registrations, where you will store your contact data, and where you will create your launch lists and segments. Suite is flexible enough to perform these tasks on its own, or in combination with one or more external databases. Most of our customers use one of three scenarios:

### 1. Suite is your only CRM

 This is the simplest solution to implement and all the preparation can be configured via the Suite user interface. You will need to:

- Make sure that all the [contact data fields](/Resources/system-fields.md "The Suite System Fields") that you need exist, and [create them](/Suite/custom-fields.md "Creating Custom Fields") if they do not
- Make an initial, manual import of your existing contact list
- Configure all your registration methods (e.g. web forms) to [transfer data](/Getting%20Started/data-transfer.md "Suite Data Transfer – Overview") to Suite
- Set up the segments and contact lists you require

 Click here for an overview of how to [add new contacts to Suite](/Suite/contacts.md "Adding New Contacts in Suite").

###  2. You use an external CRM and want to keep this synchronized with Suite

 This is our most common scenario, where new registrations and updates to existing contacts are collected in an external database (e.g. from a web shop) and the changes (delta) are synchronized either in real time or once a day with the Suite database. For this you will need to:

- Ensure that the [data fields](/Resources/system-fields.md "The Suite System Fields") you use are consistent in both databases
- Make an initial, manual import of your existing contact list
- Set up automated transfer of new data, by either: - Using the [Suite API](http://dev.emarsys.com "Suite API Programmers’ Guide"), or
- Scheduling a daily, automated import from a [Web-DAV or SFTP server](/Getting%20Started/data-exchange.md "Data Exchange Resources")

### 3. You use an external CRM and want to use Suite to send marketing campaigns only

 You can also perform all your segmentation, duplication handling and list management outside Suite, and simply import lists of email addresses when you want to send an actual campaign. This method is suited to high-volume B2C businesses, such as shopping clubs and daily deals, but loses some of the more advanced Suite features such as content personalization or section targeting, and is generally less suited to the kind of advanced customer engagement activities that Suite specializes in. Whichever scenario you choose, you will need to think about the kind of resources to use to transfer and store your contact data.