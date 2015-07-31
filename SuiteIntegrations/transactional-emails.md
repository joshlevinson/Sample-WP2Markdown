---
title: 'Sending Transactional Emails'
subject: 'SuiteIntegrations, SuiteMagento'
old_url: 'http://emarsys.dev/old/suite/magento/transactional-emails/'
---

In Magento you can define certain transactional emails, for example Confirmation Link Email, Welcome email or Order Confirmation Email. These emails can be triggered in Emarsys by associating the event in question with an Emarsys email campaign.

### Setting up the External Event in Emarsys

 To enable translational emails in Emarsys you must first create the external events in your Emarsys account (**Admin** menu / **External Events**). Here you simply define the name that will link the Magento event with the Emarsys email campaign.

### Preparing the Email Campaign in Emarsys

 Now that you have created the external event, select the Emarsys email campaign that you want to send to your Magento contacts (**Campaigns** menu / **Email Campaigns**). In the **Campaign Settings**, set the **Recipient source** to *Generated through an event* and then select the external event you created above. [![magento_txm_6](/assets/images/2015/07/magento_txm_6-300x245.png)](/assets/images/2015/07/magento_txm_6.png) Once this campaign has been launched, it is ready to send emails to your Magento contacts when triggered by the selected actions in your Magento shop. You should remember to set the **Campaign Scheduling** to launch *Exactly on event*: [![magento_txm_7](/assets/images/2015/07/magento_txm_7-300x102.png)](/assets/images/2015/07/magento_txm_7.png)

### Personalising your Transactional Email

 Since your Magento contacts are synchronized with Emarsys, you can of course use all the regular personalization variables available in Emarsys, including conditional content and section targeting. However, there may be important information about the event that triggers the email that is only available in Magento (for example, the URL of the confirmation link in a confirmation email). To add this Magento content to your Emarsys email, you must add special Magento **Transactional email** placeholders to the email content. The list of these placeholders and the Magento content they are mapped to can be found [here](/SuiteIntegrations/placeholders.md).They are grouped by the most common types of transactional emails.

### Registering the Emarsys Events in your Magento Shop

 To link the Emarsys email campaign with the Magento action that will trigger it, you must first register the Emarsys events. Proceed as follows:

1. In the Magento admin module, navigate to **System / Configuration /** **Emarsys Connect / Transactional Mail Setup**. There, set **Enable Emarsys transactional mails** to ***Yes***.
 
[![magento_txm_1](/assets/images/2015/07/magento_txm_1-300x133.png)](/assets/images/2015/07/magento_txm_1.png)1. In the **Event registration** section you can see all the external events in your Emarsys account. To register them in Magento, simply select the event and click the right arrow (use the left arrow to reverse this action at any time).
2. Click **Save Config** to register your event list.

 The registered events are now visible in the list of custom Transactional Mail templates (**System **menu** / Transactional Emails**). **Note:** After you have associated an event with a Magento transactional email (see below), clicking that event in the **Event registration** section will show the Magento email where the event is used: [![magento_txm_4](/assets/images/2015/07/magento_txm_4-300x80.png)](/assets/images/2015/07/magento_txm_4.png) You cannot deregister an event which is in use; this action will not be saved with your new configuration and you will receive an error message: [![magento_txm_5](/assets/images/2015/07/magento_txm_5-300x33.png)](/assets/images/2015/07/magento_txm_5.png)

### Selecting the Emarsys Event as a Magento Transactional Email

 The Emarsys events are also now available for selection as transactional emails in your Magento Customer Configuration (**System** menu / **Configuration** / **Customers** / **Customer Configuration**): [![magento_txm_3](/assets/images/2015/07/magento_txm_3-300x185.png)](/assets/images/2015/07/magento_txm_3.png) After you save your configuration, the corresponding email will be triggered in Emarsys by the event in Magento.

### Double Opt-in

 Emarsys insists that all clients use **Double opt-in registration** as the best practice to guarantee and safeguard the Emarsys deliverability reputation, and ensure the best deliverability rates for all its clients. In Magento this is called **Requiring Email Confirmation**. You must ensure that this field is always set to *Yes*.