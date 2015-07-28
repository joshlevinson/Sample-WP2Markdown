---
title: 'Emarsys Deliverability Policy Requirements'
tags: Deliverability
old_url: 'http://emarsys.dev/resources/deliverability/policy-requirements/'
---

Emarsys clients benefit from the highest standards in email marketing: state-of-the-art infrastructure, the fastest available mail servers and reliable applications. We set the standards for security in email marketing and have achieved the highest level of security accreditation â&#128;&#147; the ISO 27001 certification. Our Deliverability team ensures optimal results for all our clients by actively managing thousands of IP addresses, which are grouped for optimal performance and deliverability. In short, we take care of almost every aspect of email marketing which can facilitate the success of our clients. However, there are still some aspects which will always require additional cooperation from the clients themselves. To facilitate this we have prepared these guidelines which all our clients must follow in order to be allowed to send via our infrastructure and applications. It also describes the best practices which help our clients to achieve perfect deliverability results, right from the start.

<table style="width: 100%;"><tbody><tr><td style="text-align: left; width: 110px; border-color: #fff; background-color: #fff; color: #eb5a19;">**Important Note:**</td> <td>Our excellent sending reputation is a result of **all** our clients satisfying our high quality standards. It is therefore vital that every single account complies with these guidelines in order for everyone to benefit.</td></tr></tbody></table>##### Contents

- [Permission to Send / User Registration](#permission)
- [List Hygiene](#hygiene)
- [Sender Authentication â&#128;&#147; Domain Configurations](#sender)
- [Content Policy Compliance](#content)
- [Best Practice Recommendations](#best)
 
<a name="permission"></a>1. Permission to Send / User Registration
-----------------------------------------

#### 1.1 Registration Compliance

**Permission â&#128;&#147; Registration â&#128;&#147; Website ** It is imperative that our clients do not send emails to recipients unless those recipients have actively and explicitly agreed to receive them. **The single, most important requirement is that you only send to recipients who have given you their prior, explicit and verifiable permission to send that specific type of material (i.e. opt-in).** The only exception to this rule is if there is a pre-existing business relationship between sender and recipient. In this case, content or promotions can be sent as long as the content is similar to a previous purchase. However, not all countries accept these kinds of relationships as valid reasons not to have an opt-in, which can translate to risks to your brand and reputation.

<table style="width: 100%;"><tbody><tr><td style="text-align: left; width: 80px; border-color: #fff; background-color: #fff; color: #eb5a19;">**Please Note:**</td> <td>â&#128;&#152;Similarâ&#128;&#153; is open to interpretation, which can cause unintended issues, so we recommend that you only send to contacts who have opted in. Sending content that is not related to similar products purchased is not compliant with our sending policy and is likely to result in your account being blocked.</td></tr></tbody></table> The Emarsys basic standard is the 'confirmed opt-in', where a confirmation email is sent to the registering contact with a highly visible and easy-to-use unsubscribe option. For optimal list hygiene, we highly recommend adopting our gold standard of using a double opt-in, where the recipient is sent an email with an opt-in confirmation link to make sure they are serious about receiving your content. To comply with current legal requirements, and our own [Anti-Spam Policy](/Resources/anti-spam-policy.md "Anti-Spam Policy"), your website must have a privacy policy, which must contain the following elements:

- The privacy policy must be clearly visible and displayed to the registering person, who must read and confirm that they accept the terms before they grant you permission to send them content by using an opt-in checkbox (for website registrations only). This checkbox should **not** be pre-checked.
- The privacy policy must contain information on the services provided and types of emails to be sent following the registration; Emarsys does not allow the sending of 3rd-party emails.
- Clear information is available to your customers on how you collect and use data, as well as disclose, transfer and store subscriber information.
- Detailed information on the unsubscribe functionality and process must be made available, i.e. an easy-to-use unsubscribe link must be available in every email, and the unsubscribe process is clearly explained in the Privacy Policy.
- You make physical and summonable company address available for your customers.

#### 1.2 Registration Data Requirements

**All** of the following must be available for each recipient in case of complaints or legal issues arising, as they help prove the legality of the permission to send:

- The IP from which the client registration originated
- The date and time of registration
- A copy of the Privacy Policy as shown at the point of registration
- A copy of the registration page as shown at the point of registration
- In the case of pre-existing customer relationships, the following is also required: - The date and time of the last purchase
- What items were purchased
- All shipping information (e.g. database logs, confirmation of receipt, etc.)
- And any additional registration data (e.g. personal data) that can help prove the legality of registration

#### 1.3 Registration Form Types and Scope

**Simple Newsletter / Promotional Offers Registrations** A plain newsletter or promotional offer registration consists, in the simplest form, of a form field for the email address and a button to submit the email address being registered. The only prerequisite is that the registration requires a conscious and explicit action by the person wishing to subscribe, i.e. clicking the subscribe button. The email address is the only required field, and any additional fields for personal data can be included as long as they are optional only. **Combined Registration Form** A combined registration form is where a contact can register for multiple types of content at once, e.g. a forum subscription PLUS a newsletter subscription. Such combined registration forms have the following requirements:

1. The content must be clearly separated. Each content type must have its own checkbox to use for opt-in purposes, meaning that registering for one type of content is not bound to a subscription of another. For example, a form allowing a recipient to sign up to both a forum and a newsletter subscription at the same time must allow the user to select a single option and still work.
2. The opt-in checkbox has to be deselected by default, i.e. the person has to expressly click to opt-in.
3. A checkbox must be present confirming that they have read the privacy policy at point of registration. This checkbox also has to be deselected by default, and a link to the Privacy Policy must be available next to the checkbox.
 
<a name="hygiene"></a>2. List Hygiene
---------------

 List Hygiene is how you keep your contact lists away from any potentially harmful content by removing those contacts who are not happy to receive your emails. This means cleaning your contact database regularly and quickly addressing any deliverability issues that arise including hard bounces, soft bounces, unsubscribe requests, etc. If a contact loses interest and opts out, but still receives content, then a complaint from them becomes a very real risk. ISPs are highly likely to block senders that receive high numbers of complaints, or continuously send to non-existant email addresses. Emarsys eMarketing Suite will take care of managing your list hygiene automatically, but for our other products you will need to maintain list hygiene yourself. A process has to be set up which automatically runs on a daily basis (i.e. every 24 hrs) and cleans the database by removing the addresses of recipients who should no longer receive content. This data is comprised of addresses which have been flagged as any of the following response types:

- Complaint
- Hard bounce
- Unsubscribe request
 
<table cellpadding="1" class="wikitable" style="width: 100%; border: 0px solid #999;"><tbody><tr><td scope="col" style="text-align: left; border: 0px solid #999; vertical-align: top;" width="60">[![Icon AdditionalInfo.png](/assets/images/Icon_AdditionalInfo.png)](/assets/images/Icon_AdditionalInfo.png)</td> <td scope="col" style="border: 0px solid #999; vertical-align: top; color: #555555;">Soft bounces do not have an immediate impact on your deliverability; however, we recommend to remove the corresponding addresses after 2-4 bounces.</td> </tr></tbody></table><a name="sender"></a>3. Sender Authentication â&#128;&#147; Domain Configurations
--------------------------------------------------

 Emarsys meets all industry standard requirements regarding sender authentication and domain configuration, and as such all our client domains are configured with valid records for:

- **SPF** â&#128;&#147; configured for the return path/envelope by Emarsys.
- **SenderID** â&#128;&#147; configured in the DNS of the client domains.
- **MX** â&#128;&#147; a valid MX record is required in order to receive reply mails and/or complaints. In addition, a postmaster@ and abuse@ address for every sender domain have to be available as these addresses are necessary for receiving confirmation emails from Yahoo! to ensure Y! Feedback Loop compliance.
- **DKIM** â&#128;&#147; configured in the DNS of the client domains and our MTAs
- **DMARC** - The "p" switch must be set to "reject", as this allows senders to bypass certain spam filters at major ISPs.

 In addition to the sender authentication requirements, a valid CNAME that points to the respective environment and application is required for all trackable link domain(s). Information regarding CNAME is provided during the account setup process.<a name="content"></a>

4. Content Policy Compliance
----------------------------

 With regards to the content of an email, there are certain legal and policy requirements that are outlined and implemented by most major ISPs. We have implemented our own anti-spam policy to cover these requirements which includes the following:

1. Every email must contain an easy ('one-click') unsubscribe link, i.e. after clicking the link, recipients are redirected to an unsubscribe page or form where they can unsubscribe with a single click. The unsubscribe form must comply with the following five requirements:

- No login is required to unsubscribe, i.e. it should be readily accessible by anyone
- No extra steps are required to unsubscribe, i.e. it does not lead to additional forms, pages or links to complete
- No persuasive language is used to entice a person to remain subscribed
- No costs to unsubscribe, i.e. it has to be free
- No advertising is used in the form


1. All emails must contain a link to the privacy policy on the clientâ&#128;&#153;s website.
2. All emails must contain the physical, summonable address of the client company.
 
<table style="width: 100%;"><tbody><tr><td style="text-align: left; width: 80px; border-color: #fff; background-color: #fff; color: #eb5a19;">**Please Note:**</td> <td>Offering the unsubscribe functionality via email ('mailto: unsubscribe@example.com') or telephone is not a substitute for the one-click process. We do recommend that you provide these channels as additional unsubscribe options, but they are not a valid substitute.</td> </tr></tbody></table><a name="best"></a>5. Best Practice Recommendations
--------------------------------

 Only customers who follow all best practice recommendations can expect perfect deliverability. Even if you are an existing customer, please take a moment to see how many of the following practices you currently follow. These are the easiest ways for you to ensure stable deliverability, and have been divided into recommendations for email campaigns and for list hygiene. **Campaign-specific Recommendations** The following tips and tricks might seem obvious, but can significantly improve your deliverability rates and customer engagement.

- Include a request to â&#128;&#152;add the sender to the address book or safe sender list'. This enables the image content of your email to be automatically displayed the next time they receive an email from you. This easily and drastically increases your open rates, reputation and subsequently deliverability performance.
- Place the unsubscribe link at the top of the email. Avoid low contrast combinations, e.g. light grey text on dark grey background, so that the link is visible and accessible to all recipients. The more accessible the unsubscribe link is, the more your recipients will trust you (knowing they can opt out at any time) and the **fewer** complaints and unsubscribes you will receive.
- Use Personalization. This is an easy and effective way to engage with your recipients, increasing their trust, response rates and as a consequence your reputation and deliverability.
- Balance your Text and HTML/Image content ratio. Aim for your email to be comprised of 50% text and 50% HTML/images, but the more text content you have the better.
- Do not send HTML versions with images only. It is important that recipients are able to read the content without opening or displaying the images.
- Use an Emarsys template rather than custom HTML as the code standards in our templates are designed and tested to render well on most email clients.
- Avoid using HTML designed for web pages. If you do use custom HTML, please make sure that meta-tags (charset) are not present.
- Check that none of your links can be mistaken for phishing links. These are domains or links in the text that point to a different domain, and are usually blocked by Gmail and other major ISPs because those are the typical characteristics of phishing links.
- Limit your subject lines to 50~70 characters.
 
**List Hygiene Recommendations** The best way to improve your list hygiene practices is to make sure that your recipients are actively engaged with your content. Content policy compliance takes care of the unsubscribing, which lets you focus on engaging more with your recipients.

- Only using organically grown lists can guarantee stable delivery. Data sharing or acquisition is strongly discouraged because there is so much more work involved in maintaining the list hygiene, avoiding complaints, and ultimately the benefits to you will not outweigh the risks.
- A passive expression of lack of interest should be honored in the same way as an active opt-out. If they are ignoring you, take the hint!
- Your sending strategy should focus on recipient activity, as well as inactivity. Reactivation emails should not comprise more than 5% of your total daily mail volume.