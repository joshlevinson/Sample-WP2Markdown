---
title: 'API Use Case 5: Keeping contacts up to date'
tags: 'Getting Started, SuiteAPI'
old_url: 'http://emarsys.dev/suite-api/update-contacts/'
---

If you already have contacts in Suite, then inserting further ones requires a little care as you need to use different methods depending whether or not the contact already exists. If the contacts do not yet exist in Suite, then you have to **create** them, otherwise you have to **update** them. This use case is about deciding whether a given contact exists in Suite, and then creating or updating it accordingly. We say that a contact exists in Suite if a contact with the same key can be found.

#### Step 1: Check whether contact exists in Suite

 You can check whether a contact exists in Suite by requesting its internal contact ID. Please see the [Checking Internal Contact IDs](http://dev.emarsys.com/suite/contacts/contact_check_internal_ids.html) chapter in the Suite API Technical Reference. - If you get a result with `replyCode:0` then it already exists so you have to update it.
- If you get a result with `replyCode:2008` then it does not yet exist so you have to create it.
 
 If the `replyCode` differs from the ones mentioned above it indicates an error so please refer to the error descriptions in the API Technical Reference. #### Step 2a: Update contact

 You have to execute this step if `replyCode:0` was returned in Step 1. This means that you have to update the contact (as oppose to create it) in the Suite. Please see the [Updating a Contact](http://dev.emarsys.com/suite/contacts/contact_update.html) chapter in the Suite API Technical Reference. Each field value that you provide here will override the already existing ones in Suite. #### Step 2b: Create new contact

 You have to execute this step if `replyCode:2008` was returned in Step 1. Here you can simply create the new contact in Suite. For further information please see the [Creating a Contact](http://dev.emarsys.com/suite/contacts/contact_create.html) chapter in the Suite API Technical Reference.