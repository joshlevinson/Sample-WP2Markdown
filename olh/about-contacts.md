---
title: 'Contacts  - About Contacts'
subject: 'olh, SuiteContacts'
old_url: 'http://emarsys.dev/suite/online-help/about-contacts/'
---

#### What are external key fields?

 In Emarsys eMarketing Suite, an external key field serves as a unique identifier of a contact. You can define any database field (or a combination of such fields) as external key field. If the data you want to import originates from an external database, the system assigns IDs by default. These can be imported as external IDs and be defined as external key fields. If data is imported via key fields, and newly imported values in the new key fields comply with already existing data, older data is replaced by newer data (exception: contacts who have unsubscribed). #### How can I avoid overwriting crucial data upon import?

 If you want to regularly import lists with new and edited contact data, please consider that by doing so, all changes done by the contacts themselves via a change profile form (such as new phone number, email address) are overwritten. To avoid this, first export any changes of contact data saved in Emarsys eMarketing Suite, update your own contact data and then import new and updated data records. #### What does data export include?

 You can export contact data from the Suite database. This way, you get a snapshot of your Suite permission database at any given point or period in time (e.g. to analyze data), and you can synchronize your own CRM database to include the Suite data. **Attention**: All exports from Suite are password protected. The following data can be exported: - Contact lists
- Contact data changes and/or new registrations (manually and automatically)
- Contact responses (manually and automatically)
 
 During the export, the system assigns an internal ID to each record. The internal ID is unique and will later on allow you to re-import the same file to Emarsys eMarketing Suite. Example: You exported a list with invalid email addresses and corrected them in Microsoft Excel. In order to re-import the records, you only need to provide the internal IDs and the updated email addresses. Emarsys eMarketing Suite will update the records in the database accordingly.