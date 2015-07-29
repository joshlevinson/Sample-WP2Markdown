---
title: 'Preparing your contact database'
subject: SuiteSMS
old_url: 'http://emarsys.dev/suite/sms/contact-data/'
---

When importing contacts into Suite there are two database fields which are critical for the SMS feature.

##### Mobile SMS Opt-in

 When the SMS feature is activated, Suite automatically creates a **Mobile SMS Opt-in **field in your account. This field determines whether or not a contact can be sent content via SMS. When the SMS feature is first activated, this field is of course empty, so Suite will treat all contacts as having an SMS opt-in initially. This means that all contacts with a valid mobile phone number will be eligible to receive SMS campaigns. It is up to you to segment the contacts accordingly using other database fields. After a contact opts out by clicking the unsubscribe link, the value for this field will be set to FALSE and they will no longer be able to receive SMS campaigns. ##### Mobile

 The** Mobile** field stores the mobile number of the contacts. This is a system field and exists in your Suite account by default. Suite treats all mobile numbers as international, therefore there is no need to prefix them with 00 or +. However, we do recommend to include the country code with the number, for example: **436642606096**. **Please note:** numbers starting with both **00** and **+** will be accepted. When importing contact data, make sure to map these two fields correctly in the same way as you would for any other data imports.  