---
title: 'SMS FAQ'
subject: SuiteSMS
old_url: 'http://emarsys.dev/old/suite/sms/sms-faq/'
---

**1.1.1     What are Emarsys SMS Campaign Product Limitations?** The Emarsys SMS product includes advanced features and personalization.Therefore there is a slight response-time overhead between Suite and submitting the message to the suppliers/operators, when data processing, automation, personalization and segmentation are factored in. The result is that an SMS message usually has a total send time of around 20-60 seconds (sometimes longer), which makes it unsuitable for time-sensitive transactional messages, e.g. password reset or online banking authorization. Faster delivery for transactional will be coming soon! <a name="_Toc401666503"></a>1.1     Character Encoding, Restrictions
--------------------------------------------------------------------

 The input settings of your computer will have an effect on the character encoding, and as a result the number of characters you can include in a single text message. We currently support GSM encoding 03.38 (standard and extended). Anything else will automatically be converted to UTF-16 encoding. The different encoding types result in the different character limits because of the size of the individual characters in the message: Latin1 characters are 1-byte characters, whereas UTF-16 are 2-byte characters. Please note: With GSM encoding there are exceptions called Extended Characters which are 2-byte characters, including: ( , ~ , ^ , } , { , | , > , <. These might not display correctly due to limitations on the recipient’s device. <a name="_Toc401666504"></a>1.2 Sending Long messages: SMS Concatenation
------------------------------------------------------------------------

 To help compensate for the limited characters per SMS, some mobile phones and networks support SMS Concatenation. This is where extra-long SMS message content is split into multiple messages when it is sent, and is then recombined into a single message by the recipient device. To the recipient it looks like one long SMS, and the concatenation is nearly transparent – with the exception that each message is billed separately. If an SMS is sent with 240 characters (GSM encoding) then it will be processed as two separate messages, and billed accordingly. Please note: not all network operators support this feature, please refer to the features table. GSM encoding: - One standard SMS message = 160 characters (max)
- Two concatenated SMS messages = 306 characters (max)
 
 UTF-16 encoding: - One standard SMSmessage = 70 characters (max)
- Two concatenated SMSmessages = 134 characters (max)
 
 Although we do support concatenation we do not recommend using it as not all providers fully support this technology, resulting in the content potentially not being correctly rendered – But if you still wish to use it check the **Reach table.**   ### One of our prospects wants to use his already existing SMS provider. Is it possible?

<div class="panel"><div class="panelContent"> It’s currently not possible to “Easily” integrate an sms provider. There’s a lot of testing and optimization evolved. Also if it was possible, it would be just a 1 way sending with no other components such as; opt in management, reporting etc… Therfore we recommend using our fully integrated providers; Mblox and Wavecell ### What happens if the prices are to expensive for the customer

<div class="panel"><div class="panelContent"> We can manually work with our partners to modify prices for clients on a case by case method. Discounts can apply only in high volumes, above 1M, or in other exceptional cases were the target market price is significantly lower then our partners prices. ### **Do we have a frequency cap for SMS?**

<div class="panel"><div class="panelContent"> We dont have a frequence cap at this time, but it can be capped via the AC. </div> </div> </div> </div> </div></div>