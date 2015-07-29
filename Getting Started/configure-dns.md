---
title: 'Configuring your DNS Settings'
subject: 'Deliverability, Getting Started'
old_url: 'http://emarsys.dev/getstarted/configure-dns/'
---

It is important to make sure that the DNS settings are correctly updated, otherwise you may have a delay before you can start to send emails. On this page you can find all the information you need to configure these settings correctly.

##### Contents

- [DKIM Settings](#dkim)
- [SenderID/SPF Record](#spf)
- [DMARC](#dmarc)
 
<table style="width: 100%;"><tbody><tr><td style="text-align: left; width: 80px; border-color: #fff; background-color: #fff; color: #eb5a19;">**Please Note:**</td> <td>In the examples below, **example.com** is used to describe the domain that you use to configure all your DNS settings.<a name="dkim"></a></td></tr></tbody></table>DKIM Settings
-------------

### DKIM settings (Selector)

 To configure DKIM authentication for your sender domain, create the following subdomains and set the following DNS TXT record: #### Subdomain (DNS Host Name)

`key2._domainkey` This prefix should be added to the (sub)domain you are sending from. For example, if you are using **.reply.example.com** for sending, then the full domain for this record should be: `key2._domainkey.reply.example.com`#### TXT record

 Please add the following TXT record to the new subdomain: `v=DKIM1;k=rsa;p=MIGfMA0GCSqGSIb3DQEBAQUAA4GNADCBiQKBgQCqFwlkVVM4irVCuSD/bs1ewUWLU/0c8qOdhw4/YXXZugQapNKUpcpmaFwZ3Dw380eIm8fFUfv96ObYEPeDBb32KcOjQfHV6cquwMfnIy7iZtC+3lloRJKKc/fHDgaP81l8fOEwpm7F4jXqa3Qh775JlsrptFfBoMAyQ0XDgUQI1QIDAQAB`### DKIM settings (Policy/Domain key)

#### Subdomain (DNS Host name)

`_domainkey` This prefix should be added to the (sub)domain you are sending from. For example, if you are using **.reply.example.com** for sending, then the full domain for this record should be: `_domainkey.reply.example.com`#### TXT record

 Please add the following TXT record to the new subdomain. Replace the link in the example with the link to your own privacy policy: `o=~;n=<a class="external free" href="http://www.example.com/privacy_policy.html" rel="nofollow">http://www.example.com/privacy_policy.html</a>` In the example above, the URL is a link to your privacy policy. The domain must match the domain used for all your DNS settings. In other words, your privacy policy cannot be hosted on a different domain.<a name="spf"></a>SenderID/SPF Record
-------------------

 The SenderID/SPF is an explicit list of your hosts that you want to configure to be able to send emails from, and is a check that ISPs can use to confirm the legitimacy of your emails. Add the following TXT record to all your sender domains (including sub-domains): `v=spf1 include:emarsys.net include:emsmtp.com ~all` <table style="width: 100%;"><tbody><tr><td style="text-align: left; width: 80px; border-color: #fff; background-color: #fff; color: #eb5a19;">**Please Note:**</td> <td>In case you are using your own infrastructure to send emails in addition to Emarsys, you will have to set **additional SPF records** according to that infrastructure’s processes.<a name="dmarc"></a></td></tr></tbody></table>DMARC
-----

 DMARC (Domain-based Message Authentication, Reporting & Conformance) is a method to configure actions related to authentication failures and was created by a group of organizations, among them AOL, Google, Microsoft and Yahoo!. It allows senders to tell ISPs how to handle unsigned (non-authenticated) or failed (broken authentication) emails which use the sender’s domain name. You can optionally receive reports regarding failed authentication attempts. For example, a DMARC record can indicate that such emails should be delivered, flagged as suspicious or deleted. This step is optional but highly recommended. #### Configuring DMARC Step 1

 The DMARC record is a special subdomain to your domain called `_dmarc` (for example: `_dmarc.example.com`). ##### DMARC entry

 Add the following DMARC entry to the TXT record of all your domains: `DNS Host name: _dmarc` If you are using a subdomain, you should add this. For example, if you are using the subdomain **.reply.example.com**, then the entry should be: `_dmarc.reply.example.com`##### TXT record

`v=DMARC1; p=reject; adkim=s; aspf=r; rf=afrf; pct=100;` The parameters used here are: <table class="wikitable"><thead><tr><th>Parameter</th> <th>Description</th> </tr></thead><tbody><tr><td>`v=DMARC1`</td> <td>The version of DMARC being used is `DMARC1`</td> </tr><tr><td>`p=reject`</td> <td>ISPs should reject messages which fail to authenticate</td> </tr><tr><td>`adkim=s`</td> <td>Strict identifier alignment should be applied to DKIM checks</td> </tr><tr><td>`aspf=r`</td> <td>Relaxed identifier alignment should be applied to SPF checks</td> </tr><tr><td>`rf=afrf`</td> <td>Authentication Failure Reporting Format</td> </tr><tr><td>`pct=100`</td> <td>Percent of messages on which the policy is to be applied is 100%</td></tr></tbody></table>#### Configuring DMARC Step 2

##### Enable feedback

 In case you would like to receive an aggregated feedback report, you can modify your DMARC entry with a number of additional parameters. These are: <table class="wikitable"><thead><tr><th>Parameter</th> <th>Description</th> </tr></thead><tbody><tr><td>`rua=<a class="external free" href="mailto:dmarc-feedback@example.com" rel="nofollow">mailto:dmarc-feedback@example.com</a>`</td> <td>Aggregated feedback reports are sent via email to this address</td> </tr><tr><td>`ruf=<a class="external free" href="mailto:dmarc-forensic@example.com" rel="nofollow">mailto:dmarc-forensic@example.com</a>`</td> <td>Forensic information reports are sent via email to this address</td> </tr></tbody></table><table style="width: 100%;"><tbody><tr><td style="text-align: left; width: 80px; border-color: #fff; background-color: #fff; color: #eb5a19;">**Please Note:**</td> <td>This step is optional but highly recommended. However, only an experienced DNS administrator should do this and test it because otherwise it will prevent any of your emails from being delivered.</td></tr></tbody></table>##### Example

 An example feedback record might look as follows:     v=DMARC1; p=reject; adkim=s; aspf=r; rf=afrf; pct=100; rua=<a class="external free" href="mailto:dmarc-feedback@example.com" rel="nofollow">mailto:dmarc-feedback@example.com</a>; ruf=<a class="external free" href="mailto:dmarc-forensic@example.com" rel="nofollow">mailto:dmarc-forensic@example.com</a>;

 The above example tells the receiving email servers to drop all emails from unauthorized domains, and to send you an abuse report to the nominated email addresses. ### Reply Mail Management

 If you are intending to use the Emarsys Reply Mail Management, you will need to configure the MX record. Add the following MX record to all your **sender** domains (including sub-domains): `10 mx.eemms.net` <table style="width: 100%;"><tbody><tr><td style="text-align: left; width: 80px; border-color: #fff; background-color: #fff; color: #eb5a19;">**Please Note:**</td> <td>The value **10** refers to the relative priority of the server and may have to be entered in a separate field, depending on your domain host.</td> </tr></tbody></table> If you are planning to manage your own reply mails, you do not need to perform this step. However, you will be receiving an email from Yahoo! following configuration of the Yahoo! Feedback Loop by Emarsys Support. This email will be sent to the **abuse** mailbox of your sender domain, i.e. **abuse@example.com**. Please make sure to reply to this email by clicking the confirmation link it contains. ### Link Domains

 This is important for link tracking. You will need to provide a subdomain for the DNS host name and the Emarsys environment where your eMarketing Suite account is hosted for the CNAME record. Emarsys Support will tell you which Emarsys environment to use, and then add this as the CNAME record to all your tracking (link) domains (including sub-domains). #### Example

`suite6.emarsys.net`