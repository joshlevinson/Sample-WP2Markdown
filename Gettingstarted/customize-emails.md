---
title: 'API Use Case 3: Customizing your email with data from external events'
subject: 'Gettingstarted, SuiteAPI'
old_url: 'http://emarsys.dev/old/suite-api/customize-emails/'
---

If you want to thank contacts for their first purchase and you also want to mention the product they bought, you need to include ***transaction-specific content***. In this case you have to use a placeholder for the transaction-specific content in your email and send the item name along with the external event.

#### Preparation

##### **Preconditions**

 To perform these preparatory steps you will need the credentials for your Suite account (account name and environment, user name and password).

<table cellpadding="1" class="wikitable" style="width: 100%; border: 0px;"><tbody><tr><td scope="col" style="text-align: left; border: 0px solid #999; vertical-align: top;" width="60px">[![Icon BeCareful.png](/assets/images/2014/04/Icon_BeCareful.png)](/assets/images/2014/04/Icon_BeCareful.png)</td> <td scope="col" style="border: 0px solid #999; vertical-align: top; color: #555555;">Create a dedicated external event for each of your emails, otherwise a single external event may accidentally trigger many emails.</td></tr></tbody></table>#### **Create an external event**

- Create the external event in the Suite UI. You can find external events in the **Admin** menu.

#### [![](/assets/images/2014/04/Suite_API_create_external_event_crop.png)](/assets/images/2014/04/Suite_API_create_external_event_crop.png) **Email Settings**

- Create the email: - Set **Generated through an event** as the **Recipient source**.
- Set **On External Event** as the **Event**.
- Choose your event
 
[![](/assets/images/2014/04/Suite_API_set_external_event_as_recipient_source_of_an_email_crop.png)](/assets/images/2014/04/Suite_API_set_external_event_as_recipient_source_of_an_email_crop.png)#### **Launch Email**

- Make sure that your email is launched.
 
[![](/assets/images/2014/04/Suite_API_acivate_email_colour.png)](/assets/images/2014/04/Suite_API_acivate_email_colour.png)<table cellpadding="1" class="wikitable" style="width: 100%; border: 1px solid #fff;"><tbody><tr><td scope="col" style="text-align: left; border: 1px solid #fff;" width="60px">[![Icon FurtherReading.png](/assets/images/2014/04/Icon_FurtherReading.png)](/assets/images/2014/04/Icon_FurtherReading.png)</td> <td scope="col" style="border: 1px solid #fff;">For further information about creating an email via the Suite UI please see the eMarketing Suite Online Help.</td></tr></tbody></table>#### Step 1: Create user

 To create a new contact, send a `POST` request to the `<a class="external text" href="http://dev.emarsys.com/suite/contacts/contact_create.html" rel="nofollow" target="_blank">/api/v2/contact</a>` URI. The following example shows a minimal payload:


    {
       "3":"test@example.com"
    }

 To identify the contact we are using their email address, which is also the default key. Therefore, we do not have to define a `key_id` here.

<table border="0" cellpadding="1" class="wikitable" style="width: 100%; border-width: 0px; border-style: solid;"><thead><tr><th style="text-align: left; border-color: #fff; background-color: #fff; color: #eb5a19;">**Please Note:**</th> </tr></thead><tbody><tr><td style="text-align: left; border-color: #fff; background-color: #fff; color: #555555;">You cannot create an already existing contact.</td> </tr></tbody></table><table cellpadding="1" class="wikitable" style="width: 100%; border: 1px solid #fff;"><tbody><tr><td scope="col" style="text-align: left; border: 1px solid #fff;" width="60px">[![Icon FurtherReading.png](/assets/images/2014/04/Icon_FurtherReading.png)](/assets/images/2014/04/Icon_FurtherReading.png)</td> <td scope="col" style="border: 1px solid #fff;">For further information about *creating* a contact in Suite, see [**Creating a Contact**](http://dev.emarsys.com/suite/contacts/contact_create.html) in the Suite API Technical Reference.</td> </tr></tbody></table><table cellpadding="1" class="wikitable" style="width: 100%; border: 1px solid #fff;"><tbody><tr><td scope="col" style="text-align: left; border: 1px solid #fff;" width="60px">[![Icon FurtherReading.png](/assets/images/2014/04/Icon_FurtherReading.png)](/assets/images/2014/04/Icon_FurtherReading.png)</td> <td scope="col" style="border: 1px solid #fff;">For further information about *updating* a contact in Suite, see [**Updating a Contact**](http://dev.emarsys.com/suite/contacts/contact_update.html) in the Suite API Technical Reference.</td></tr></tbody></table>#### Step 2: Trigger the event

##### **Preconditions**

- You need at least one contact available in Suite so that the contact data can be used.

 You can trigger your external event by sending a `POST` request to the `/api/v2/event/<id>/trigger` URI, where the `<id>` is your external event ID. The following example shows a minimal payload:


    {
       "key_id":"3",
       "external_id": "test@example.com"
       "data":
       {
          "global":
          {
             "itemName": "keyboard",
             "itemPrice": "123"
          }
       }
    }

**Where...****id** = The external event ID (not the name!). Since these IDs don’t change, you can just use the API demo page to get the ID, and use it in your integration script. **key_id** = The ID of the key field of the contact. We are using '3' meaning the e-mail address. **external_id** = The value of the key field, the contact’s email in this case. **data** = Your transaction-specific content in form of **placeholder:value** that are included in a **global** object.

<table cellpadding="1" class="wikitable" style="width: 100%; border: 1px solid #fff;"><tbody><tr><td scope="col" style="text-align: left; border: 1px solid #fff;" width="60px">[![Icon FurtherReading.png](/assets/images/2014/04/Icon_FurtherReading.png)](/assets/images/2014/04/Icon_FurtherReading.png)</td> <td scope="col" style="border: 1px solid #fff;">- Retrieve external event IDs by querying all external events on the API (see the [Querying External Events](http://dev.emarsys.com/suite/external_events/external_event_list.html) chapter in the Suite API Technical Reference).
- For further information about triggering external events, see the chapter [Triggering External Events](http://dev.emarsys.com/suite/external_events/external_event_trigger.html) in the Suite API Technical Reference.
- For a list of available Field IDs, [click here](http://dev.emarsys.com/suite/appendices/system_fields.html).
 
</td></tr></tbody></table>#### Step 3: Check results

##### **Check Sent-Counter**

- Check whether an email was sent successfully: - Check with a test contact if the 'Welcome email' has arrived - it should be delivered within seconds.
- Use the Suite UI to check if an email was sent.In the **Analysis** module in the **Emails** page you can see that the count of **Sent** emails increases.
 
[![](/assets/images/2014/04/Suite_API_check_email_sent_colour.png)](/assets/images/2014/04/Suite_API_check_email_sent_colour.png)<table cellpadding="1" class="wikitable" style="width: 100%; border: 1px solid #fff;"><tbody><tr><td scope="col" style="text-align: left; border: 1px solid #fff;" width="60px">[![Icon FurtherReading.png](/assets/images/2014/04/Icon_FurtherReading.png)](/assets/images/2014/04/Icon_FurtherReading.png)</td> <td scope="col" style="border: 1px solid #fff;">For further information please see the eMarketing Suite Online Help.</td></tr></tbody></table>