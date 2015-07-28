---
title: 'Synchronizing Contact Data'
tags: 'SuiteIntegrations, SuiteMagento'
old_url: 'http://emarsys.dev/suite/magento/synchronizing-contacts/'
---

### About Magento contacts

 Magento has two main type of contacts:

- **customers** (contacts who are able to purchase)
- **subscribers** (contacts who are subscribed to the web shop newsletter)

 These are identified by unique Magento identifiers (the **Magento Customer ID** and **Magento Subscriber ID** mentioned in the pre-requisites above). A contact can be both of these types, in which case both values are synchronized in Emarsys under the same contact record, avoiding duplicate email addresses. These two fields are the key identifiers for contacts being synchronized between Magento and Emarsys, rather than the email address, since the latter could be changed manually by the contact in their customer profile. The contact synchronization settings can be found under **System / Configuration / Emarsys Connect /** **Contacts Synchronization**.

### Field Mapping

 Magento **customers** have a very complete customer profile offering a number of fields. Depending on your business model and needs, you will probably only be interested in a subset of these fields. In contrast, Magento **subscribers** only have four fields available for synchronization: first name, last name, email address and subscription status (opt-in). Select the Magento fields you want to synchronize and the appropriate target field in Emarsys, and use the right arrow to move the mapped pairs across. If no suitable fields exist in Emarsys you can create them as custom fields, remembering to pay attention to the field type. [![magento_sync_1](/assets/images/magento_sync_1-300x133.png)](/assets/images/magento_sync_1.png) **Note:** As well as the fields you select for mapping, three Magento fields are always included for synchronization by default: Opt-in, the Customer ID and the Subscriber ID.

### The Initial Export

 The first time that you install Emarsys for Magento you must make an initial export of all the contacts you want to synchronize with Emarsys. Thereafter, data is only synchronized when necessary, i.e. when a contact has been added or modified. In the **Synchronization Settings** page, you can define whether to export all your Magento **customers** or **subscribers**, or both. Each contact type is saved to an Emarsys contact list; you must enter the name of these lists in the appropriate field. If you enter the name of an existing contact list, your Magento contacts will be added to that list. If no such contact list exists in Emarsys, a new one with that name will be created.

- For Magento **customers**, all the fields defined in the **Field Mapping** above will be exported, along with the **Opt-in** and **Customer ID** fields.
- For Magento **subscribers**, only the **First name**, **Last name**, **Email address**, **Opt-in** and **Subscriber ID** are exported.

 To start the synchronization, click the appropriate **Export…** button. The first export will start at the next multiple of five minutes.

### Synchronization mode

 Contacts synchronization can be scheduled in two ways:

- **Realtime-failsafe**

This maintains contact synchronization in real time, sending every update as it occurs in Magento. This option is suitable for use cases where Emarsys needs the data immediately (e.g. for automated engagement programs). In case of unsuccessful updates (e.g. due to network downtime or excessive volume), they are placed in a failsafe queue and are processed once a day at the specified **Background runtime** (see below). **Important note:** you should discuss your needs with Emarsys Support to ensure that you have the right API configuration to handle your requirements in terms of volume of traffic.

- **Background** **only**

This synchronizes all contact updates that have occurred in the 24 hours up to the specified **Background runtime**. This option is suitable when there is no urgency for the data to be transferred to Emarsys, and there is no limit to the volume of data being synchronized.

**Background runtime** Here you enter the time of day when your failsafe export will run (if you are using the **Realtim-failsafe** option), or when your daily export will run (if you are using the **Backgrond only** option). [![magento_sync_3](/assets/images/magento_sync_3-300x87.png)](/assets/images/magento_sync_3.png)

### What Data is Synchronized?

- **From Magento to Emarsys**

The Magento contact database is considered the Master database for contact details, and all values synchronized for the mapped fields will overwrite the existing values in Emarsys. For **Magento customers**, new contatcs will be exported will the same fields as per the initial export. For **Magento subscribers**, only the **Email address** and **Opt-in** fields are exported, since the **First name** and **Last name** fields cannot be modified in Magento.

- **From Emarsys to Magento **

Once a day, at the specified **Background runtime**, Emarsys also checks if the **Opt-in** field of any Magento contacts has been modified. If so, this change is synchronized back to Magento.

However, it is strongly recommended not to change the opt-in status in Emarsys as it will take up to 24 hours to update to Magento, during which time the contact could possibly receive further (transactional) emails. Best practices would be to update it in Magento, so the Emarsys contact will be updated as specified in the synchronization mode.