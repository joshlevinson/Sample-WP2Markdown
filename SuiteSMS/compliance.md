---
title: 'SMS Content Compliance and Opt-in'
subject: SuiteSMS
old_url: 'http://emarsys.dev/old/suite/sms/compliance/'
---

Introduction
------------

 SMS sending is generally limited by the behavior of the local carriers who actually deliver the message to the device, as well as the handset used by the recipient. It may be that certain carriers or devices do not support some features, such as numeric/alphanumeric **From names**. Emarsys maintains a **Reach Table** which lists the geographical idiosyncrasies that you can expect when sending to different parts of the world; this table is available from Emarsys Support. Below you can find more general guidelines to help you when selecting the right content for your SMS campaigns, to ensure the best possible deliverability, as well as best practice guidelines on how to manage your SMS subscriptions. In short, all SMS messages sent using Emarsys must include the following elements:

- Your SMS marketing messages must include a single opt-out process that immediately discontinues sales and marketing SMS messages to a subscriber.
- All opt-ins must be collected by you

### **General Content guidelines**

 As with email, SMS content should not:

- Violate any laws or regulations
- Be deliberately deceptive
- Contain obscene or pornographic content
- Be harmful to minors
- Be defamatory in nature

 Some additional tips:

- Content should always include a clear and relevant call-to-action stating the purpose of the message, for example a reminder, discount, sale, etc.
- Personalize any external links and use these in combination with attractive offers to not only improve campaign performance, but to help reduce opt-out requests.

### Confirming Opt-in

 Sending marketing SMS content requires a separate, visible and explicit opt-in, which means that if a contact has opted-in for email content you <u>must not</u> send them any SMS content just because you also have their mobile number. You can (and should) use double opt-in for SMS in the same way as you do for email, with the contact signing up on your website followed up by an SMS opt-in confirmation request being sent to them for agreement. A best practice SMS opt-in message is made up of the following:

- Clear description of what content they will receive
- A clear opt-out / unsubscribe link
- An indication of how often they will receive messages (this is legally required in France & the USA only)
- Associated data rates and/or costs (if no costs, you must explicitly state this)*
- A legally compliant SMS Opt-in message

*Also mandatory in France the USA. The following phrase must be included exactly as is, since it is mandatory for any SMS message content being sent by businesses: **“Msg&Data rates may apply”**.

### Managing Opt-outs (Unsubscribes)

 We support two methods for opting out of receiving SMS content. These are the only replies that the automated SMS module handles within Emarsys.

- **Using an SMS Unsubscribe link**

Our recommended option is to place a unique unsubscribe link in your SMS message. The link is provided by Emarsys in the form of a short URL. Clicking the unsubscribe link will cause the contact’s SMS opt-in to be set to FALSE without further action needed by you, and at no cost to the contact.

**Please note:** The link will reduce the total size of the message by around 22 characters.

- **Using STOP Words (mandatory in France and the USA) **

A contact can reply to an SMS using one of the common STOP keywords, for example STOP, EXIT, QUIT, UNSUB, etc. Suite can analyze and identify a variety of such words, which it then uses to change the sender’s opt-in status to FALSE (i.e. they are flagged as having opted out).

To enable this, you will need to request your own dedicated number from Emarsys. However, we do not recommend this method except where it is mandatory, since purchasing a dedicated number per country is time-consuming and expensive.

Please also bear in mind that if a contact sends you a STOP word, they might have to pay a fee for sending the SMS reply, particularly if you are messaging them from non-local number. Generating costs for a contact to unsubscribe is a sure-fire way to damage their impression of your brand.

Furthermore, if you use an alphanumeric **From name** instead of a number, then this functionality will not work. It is also not universally supported by all carriers.

 In addition to this, there are two methods for managing unsubscribes that you can handle yourself.

- **Through your own Customer Service number **

If you want to handle unsubscribes (or any other form of SMS replies) yourself, then you must provide your own valid **From number** (for example your Customer Services helpline) and collect and process the replies yourself. This is subject to a numeric sender ID support in your regions, and of course incurrs costs for the contact.

- **Making a manual unsubscribe request**

Contacts can also make a request to unsubscribe via another channel such as telephone, email, or directly to your own Customer Services, in which case their opt-in status needs to be manually changed in the Suite database. You should search for the contact in Suite and then set their Mobile SMS Opt-in status to FALSE.

### **Further Compliance and Best Practice Information**

 The [Mobile Marketing Association](http://www.mmaglobal.com/) (MMA) is a global non-profit organization responsible for establishing mobile marketing standards that works with mobile and wireless compliance associations. On a regional level, SMS and MMS messaging activities fall under the regulatory guidelines of several groups, depending on the nation in which you send the messages. Below is a list of some of these regulatory agencies:

- Germany - BNA
- UK - OFCOM
- France - ARCEP
- Australia - RTR
- Brazil - ANATEL
- Japan - MIC
- Sweden - PTS
- Canada - CRTC
- USA - CTIA, MMA - [CTIA Frequently Asked Questions](http://www.wmcglobal.com/faq.html#frequentlyaskedquestions)
- [CTIA Mobile Commerce Compliance Handbook](http://wmcglobal.com/media/ctia-mobile-commerce-compliance-handbook-v-1-3.pdf)
- [CTIA Best Practices and Successes](http://www.ctia.org/policy-initiatives/common-short-codes/best-practices-successes)
- [MMA Mobile Marketing Best Practice](http://mmaglobal.com/education/bestpractice)
- [MMA U.S. Consumer Best Practices for Messaging](http://mmaglobal.com/files/Best_Practices_for_Messaging_Version_7.0%5B1%5D.pdf)

The CTIA also publishes [voluntary guidelines](http://www.ctia.org/policy-initiatives/voluntary-guidelines "CTIA Voluntary Guidelines") regarding SMS regulations and best practices for use by those involved in mobile messaging activities.

 See our own [FAQs](/SuiteSMS/sms-faq.md) for more information.