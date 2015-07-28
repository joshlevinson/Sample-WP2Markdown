---
title: 'Sender Authentication Guide'
tags: 'Deliverability, Resources'
old_url: 'http://emarsys.dev/resources/deliverability/sender-authentication-guide/'
---

Introduction
------------

 Sender Authentication refers to the different technologies that are used to make sure email content is legitimate and deliverable. The following instructions will assist you in configuring and successfully deploying the various email authentication methods. We provide a number of resources and highlight some common problem areas as identified by the collective experience of hundreds of our customers.

### Why do I need sender authentication?

 If you have no authentication, most freemail accounts refuse to accept emails from you. Emails are easy to spoof and criminals have identified spoofing as a reliable way to exploit user trust in well-known brands. Email recipients are often unable to differentiate between a real message and a faked one, and large freemail providers have to make very difficult (and often guesswork) decisions as to which messages to deliver and which messages to categorize as spam. Sender authentication assists senders, email service providers and ISPs in their cooperation towards ensuring more secure emails, and helps to protect both email recipients and senders from painfully expensive abuse. Our policy is to ensure compliance with all authentication mechanisms, to help eliminate the risk to you by making sure your content is delivered without being flagged as suspicious.

Overview of Sender Authentication Technologies
----------------------------------------------

### SenderID

 Any domain which appears in the `From:` field of an email must have a SenderID-compliant SPF record published.

<table style="width: 100%;"><tbody><tr><td style="text-align: left; width: 80px; border-color: #fff; background-color: #fff; color: #eb5a19;">**Please Note:**</td> <td>A domain is the entire value which follows the @ sign. For example, if you use *recipient@example.com* in the `From:` field, then *example.com* must have either a SenderID or SPF record published. Depending on the provider you use for your email delivery infrastructure, you may not be able to control these domains directly, so make sure to discuss any issues with your provider as necessary.</td> </tr></tbody></table><table cellpadding="1" class="wikitable" style="width: 100%; border: 0px;"><tbody><tr><td scope="col" style="text-align: left; border: 0px solid #999; vertical-align: middle;" width="60">[![Icon BeCareful.png](/assets/images/Icon_BeCareful.png)](/assets/images/Icon_BeCareful.png)</td> <td scope="col" style="border: 0px solid #999; vertical-align: middle; color: #555555;">SPF records do NOT cover subdomains. A SenderID or SPF record for *example.com* would not cover *campaign.example.com*.</td></tr></tbody></table>### Sender Policy Framework (SPF)

 Any domain which appears in the `Return-Path` header field must have a SenderID-compliant SPF record published.

### DomainKeys Identified Mail (DKIM)

 DKIM is the successor of DomainKeys (DK), and is quickly gaining popularity amongst a wide variety of freemail providers, e.g. Yahoo! or GMail. While SPF and SenderID authenticate the *path* a message takes, DKIM authenticates each individual *message* — no matter where it has travelled. Therefore, it is a way to determine who is responsible for a particular message. This is achieved so by inserting a special signature header into the message itself. The sender of a message (you) is responsible for doing this; contact your email infrastructure provider to see if the software you are using is capable of including DKIM signatures.

<table style="width: 100%;"><tbody><tr><td style="text-align: left; width: 80px; border-color: #fff; background-color: #fff; color: #eb5a19;">**Please Note:**</td> <td>DK authentication alone is insufficient for sending with Emarsys. If you are still using this method, you should upgrade to DKIM as soon as possible.</td></tr></tbody></table>### Domain-based Message Authentication, Reporting & Conformance (DMARC)

 DMARC is an email authentication method created by a group of organizations, among them AOL, Google, Microsoft and Yahoo!. It allows senders to tell ISPs how to handle unsigned (non-authenticated) or failed (broken authentication) emails which use the sender’s domain name. For example, a DMARC record can indicate that such emails should be delivered, flagged as suspicious or deleted. DMARC also provides a way for the ISP to send feedback to the sender about which messages passed and/or failed the tests. It is this reporting capability which make DMARC interesting. Senders can find out how many emails are coming from their domain (or claiming it), where they came from, and whether their SPF and DKIM policies are correctly authenticating them.

<table border="0" cellpadding="1" class="wikitable" style="width: 100%; border-width: 0px; border-style: solid;"><thead><tr><th style="text-align: left; border-color: #fff; background-color: #fff; color: #eb5a19;">**Please Note:**</th> </tr></thead><tbody><tr><td style="text-align: left; border-color: #fff; background-color: #fff; color: #555555;">Although the DMARC record is currently only a recommendation for the ISP, we do strongly recommend using it and expect this to become obligatory in the near future. DMARC does not provide reports on how ISPs actually handle the emails in question, but it does offer valuable reports on emails which have been received and which claim to come from the sending domain, along with the results of the SPF and DKIM checks.</td></tr></tbody></table>Implementing email authentication mechanisms
--------------------------------------------

<table cellpadding="1" class="wikitable" style="width: 100%; border: 0px solid #999;"><tbody><tr><td scope="col" style="text-align: left; border: 0px solid #999; vertical-align: top;" width="60">[![Icon AdditionalInfo.png](/assets/images/Icon_AdditionalInfo.png)](/assets/images/Icon_AdditionalInfo.png)</td> <td scope="col" style="border: 0px solid #999; vertical-align: top; color: #555555;">In order to enable problem-free sending, we recommend to implement all of the authentication mechanisms described below.</td></tr></tbody></table>### Configure SPF/SenderID

 The SPF/SenderID is an explicit list of your domains that you want to configure to be able to send mail from, and is a check that ISPs can use to confirm the legitimacy of your mail.

### Pre-requisites

- Make a list of the domain(s) and subdomain(s) that you want to be able to send email on your behalf. For illustrative purposes, our examples below will use reply.example.com as the domain.
- Find out who controls your DNS (Domain Name System) servers as you will need their help to publish the email authentication records you are about to create.
- Make sure that you have access to your domain’s DNS entry, if in doubt ask your ISP to provide the key information and policy entries for your DNS entry.

### Sending via Emarsys

 Add the following SenderID entry to the TXT record of all your sender and reply domains: `v=spf1 include:emarsys.net include:emsmtp.com ~all` That's it, you have now successfully configured SPF/SenderID for use. Please continue to the next authentication mechanism setup.

### Sending via your own infrastructure - Step 1

 Use an online wizard to create the SPF/SenderID record. Here is an online wizard you can use: Microsoft SenderID Framework SPF Record Wizard: http://www.microsoft.com/mscorp/safety/content/technologies/senderid/wizard/

### Sending via your own infrastructure - Step 2

**Publish your SPF/SenderID records**- Work with your DNS administrator to publish the email authentication records you have created.
- Place the SPD/SenderID records in your public-facing DNS record.

### Sending via your own infrastructure - Step 3

**Validate your SPF/SenderID records** Make sure your records are working correctly. Some of the many available testing options are:

- VAMSOFT (use the 'show log' function on the results page)

 http://www.vamsoft.com/spfcheck.asp

- Port25 Email Tester

 check-auth@verifier.port25.com

- Sendmail Email Relay

 sa-test@sendmail.net **Hotmail** Send a testmail to a Hotmail or Windows Live account, log in, view the message and view the header. Look for the "X-SIDResult:" line for the result of their SenderID check. **GMail** <http://gmail.com> Send a testmail to a GMail account, log in, view the message and view the header. Look for the "Received-SPF" line for the result of their SPF check.

### Additional Information

<table cellpadding="1" class="wikitable" style="width: 100%; border: 0px;"><tbody><tr><td scope="col" style="text-align: left; border: 0px solid #999; vertical-align: top;" width="60">[![Icon BeCareful.png](/assets/images/Icon_BeCareful.png)](/assets/images/Icon_BeCareful.png)</td> <td scope="col" style="border: 0px solid #999; vertical-align: top; color: #555555;">For Microsoft Hotmail and Windows Live Mail, the SenderID will fail if the PTR (Pointer) mechanism is included in the SPF record.</td> </tr></tbody></table><table cellpadding="1" class="wikitable" style="width: 100%; border: 0px;"><tbody><tr><td scope="col" style="text-align: left; border: 0px solid #999; vertical-align: top;" width="60">[![Icon BeCareful.png](/assets/images/Icon_BeCareful.png)](/assets/images/Icon_BeCareful.png)</td> <td scope="col" style="border: 0px solid #999; vertical-align: top; color: #555555;">Use of the pointer directives '?all' or '+all' is not sufficient to authenticate messages accurately. Emarsys deliverability standards do not require, but strongly encourage you to use the '–all' directive whenever possible.</td></tr></tbody></table>### Configuring DKIM

<table cellpadding="1" class="wikitable" style="width: 100%; border: 0px solid #999;"><tbody><tr><td scope="col" style="text-align: left; border: 0px solid #999; vertical-align: top;" width="60">[![Icon AdditionalInfo.png](/assets/images/Icon_AdditionalInfo.png)](/assets/images/Icon_AdditionalInfo.png)</td> <td scope="col" style="border: 0px solid #999; vertical-align: top; color: #555555;">If you are hosting your own email servers, follow these steps to configure DKIM.</td></tr></tbody></table> DKIM authenticates your content on a message level, which means that every single email can be tracked to the point of origin using information in the email header.

### Prerequisites

- Make a list of *all* the domain(s) and subdomain(s) that you want to be able to send email on your behalf. For illustrative purposes, our examples below will use `reply.example.com`.
- Find out who controls your DNS (Domain Name System) servers as you will need their help to publish the email authentication records you are about to create.
- Make sure you that have access to your domain’s DNS entry. Ask your ISP to provide you the key information and policy entries for your DNS entry.

### Configuring DKIM Step 1

 Use an online wizard to create a pair of public and private keys and the policy record. Please provide a copy of your private keys to Emarsys Support. Enter your sending domain(s) and enter a '*selector'* which works like a password. Here are two online wizards you can use: http://www.socketlabs.com/services/dkwiz http://www.port25.com/support/support_dkwz.php **Example:** "**key2._domainkey.**reply.example.com": **key2._domainkey.**reply.example.com IN TXT `v=DKIM1;k=rsa;p=MIGfMA0GCSqGSIb3DQEBAQUAA4GNADCBiQKBgQCqFwlkVVM4irVCuSD/bs1ewUWLU/0c8qOdhw4/YXXZugQapNKUpcpmaFwZ3Dw380eIm8fFUfv96ObYEPeDBb32KcOjQfHV6cquwMfnIy7iZtC+3lloRJKKc/fHDgaP81l8fOEwpm7F4jXqa3Qh775JlsrptFfBoMAyQ0XDgUQI1QIDAQAB`

- Work with your DNS (Domain Name System) administrator to publish the email authentication records you have created.
- Place the *public* key in your public-facing DNS record.

#### The Policy Record

 The *policy* is a special subdomain to your domain called `_domainkey`, for example "_domainkey.reply.example.com". It contains the following TXT record: `_domainkey.reply.example.com IN TXT "o=~;n=<a class="external free" href="http://www.example.com/privacy_policy.html" rel="nofollow" target="_blank">http://www.example.com/privacy_policy.html</a>"`

- Replace the URL with the link to the privacy policy page on your website.
- Work with your DNS administrator to publish the email authentication records you have created.
- Place the *policy record* in your public-facing DNS record.

### Configuring DKIM Step 2

 Create DNS text records that include DKIM information for every domain. These will be inserted in your public-facing DNS record for each of the sending domains.

### Configuring DKIM Step 3

 Once you are ready, ask Emarsys Support to add your domains for signing to the Emarsys email servers.

### Configure DMARC

 DMARC is a framework that ISPs use to help them know how to handle emails without authentication, or broken authentication, being sent from a specific domain.

#### Prerequisites

 For illustration purposes, our examples below will use example.com.

- Ensure you have access to your domain’s DNS entry. Ask your Domain Registrar / ISP to provide you the key information and policy entries for your DNS entry.
- An email address to which to send the feedback and information reports.

 Please note: Not every Domain Registrar interface is able to set the DNS entry required for DMARC, so you might need to contact their support for further assistance.

#### <span class="mw-headline" id="c50e589fe419a6f3e6d63d72536b247c">Configuring DMARC Step 1<a name="bs-ue-jumpmark-3bfd32307fc87e6c2c92da0760b4a10d"></a></span>

 The DMARC record is a special subdomain to your domain called _dmarc, for example "_dmarc.example.com". Add the following DMARC entry to the TXT record of all your sending domains: `_dmarc.example.com IN TXT "v=DMARC1; p=reject; adkim=s; aspf=r; pct=100;"` This tells receiving email servers to drop all emails from this domain in case of authentication failure.

#### Configuring DMARC Step 2

**Enable feedback** You can receive DMARC feedback reports, choosing to receive aggregated reports (using the rua= switch) or forensic reports (using the ruf= switch), or both, as follows: `_dmarc.example.com IN TXT "v=DMARC1; p=reject; adkim=s; aspf=r; pct=100; <i>rua=<a class="external free" href="mailto:dmarc-feedback@example.com" rel="nofollow" target="_blank">mailto:dmarc-feedback@example.com</a>; ruf=<a class="external free" href="mailto:dmarc-forensic@example.com" rel="nofollow" target="_blank">mailto:dmarc-forensic@example.com</a>; rf=afrf;</i> "` The above example tells the receiving email servers to drop all emails from this domain, *and* to send you an abuse report to the nominated email addresses.

#### Understanding the DMARC components

 In detail, the individual parts of the record mean the following:

<table border="0" class="wikitable"><tbody><tr><td>`"v=DMARC1"`</td> <td>The version of DMARC being used is "DMARC1"</td> </tr><tr><td>`"p=reject"`</td> <td>ISPs should reject messages which fail to authenticate</td> </tr><tr><td>`"adkim=s"`</td> <td>Strict identifier alignment should be applied to DKIM checks</td> </tr><tr><td>`"aspf=r"`</td> <td>Relaxed identifier alignment should be applied to SPF checks</td> </tr><tr><td>`"pct=100"`</td> <td>Policy is to be applied to 100% of messages</td> </tr><tr><td>`"rua=<a class="external free" href="mailto:dmarc-feedback@example.com" rel="nofollow" target="_blank">mailto:dmarc-feedback@example.com</a>"`</td> <td>Aggregated feedback reports are sent via email to this address</td> </tr><tr><td>`"ruf=<a class="external free" href="mailto:dmarc-forensic@example.com" rel="nofollow" target="_blank">mailto:dmarc-forensic@example.com</a>"`</td> <td>Forensic information reports are sent via email to this address</td> </tr><tr><td>`"rf=afrf"`</td> <td>Reporting format is the "Authentication Failure Reporting Format"</td></tr></tbody></table>Further Reading
---------------

<table border="1" class="wikitable"><tbody><tr><td>Microsoft SenderID Overview</td> <td><http://www.microsoft.com/senderid></td> </tr><tr><td>Sender Policy Framework Project</td> <td><http://openspf.org></td> </tr><tr><td>Authentication and Online Trust Alliance Resource Center</td> <td><http://aotalliance.org/resources/authentication/index.html></td> </tr><tr><td>DomainKeys Identified Mail (DKIM)</td> <td><http://dkim.org></td> </tr><tr><td>DMARC specifications</td> <td><http://www.dmarc.org/draft-dmarc-base-00-01.html></td></tr></tbody></table>