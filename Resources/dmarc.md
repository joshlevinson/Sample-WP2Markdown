---
title: 'Understanding DMARC'
subject: Deliverability
old_url: 'http://emarsys.dev/resources/deliverability/dmarc/'
---

Below is a short history of DMARC, giving some background into why this is important and how it works. But first, a little history... When email was invented, the Internet was a very different place. The Simple Mail Transfer Protocol (rfc821) was used mainly to send quick messages between the few individuals active on the net in those days. This soon changed, however within 15 years of its original specification, email was used for far more purposes than it was designed for. People had to start thinking about methods to separate personal and commercial email from unwanted email; Internet fraud, hitherto unhheard of, became a topic of interest. Email Authentication began to help to prove that messages originated from an authenticated source, with SPF (by declaring the source in DNS), and DKIM (using keys pairs to authenticate).

#### Email Authentication

 Receiving an email from domains authenticated with SPF and DKIM means you can reliably say that the message comes from the person who claims to be the sender. But what if there is no authentication at all? If authentication fails, we must presume it's spam, but some badly-configured mailing list software might still resend a message using the original sender address. This results in authentication failures even for legitimate email, and if genuine messages can appear as phishing attempts, how do we know what to block and what to open?

#### Domain-based Message Authentication, Reporting, and Conformance (DMARC)

 This is where DMARC comes in. It helps domain owners to protect their domains reliably from all spoofing and phishing attempts. A DMARC record is set as simple text in the DNS for a given domain. An example record is:

**v=DMARC1; p=reject; adkim=s; aspf=r; rua=mailto:abuse@example.com; ruf=mailto:abuse@example.com; rf=afrf; pct=100;**

 A full explanation of this record can be found in our [Sender Authentication Guide](/Resources/sender-authentication-guide.md). The main purpose for DMARC is to set a "policy". This policy contains the action that should take place when unauthenticated mail from this domain is received. The options are to do nothing ("none"), put the mail in "quarantine" or "reject" the message. Only by using the “reject" policy, can a domain be fully protected. The second functionality of DMARC enables ISPs to send reports about the authentication success or failure for a domain. Those reports are sent to the addresses defined in "rua" (aggregated reports) and "ruf" (forensic reports). <https://e-mail.eco.de/wp-content/blogs.dir/26/files/eco_dmarc_legal_report.pdf> provides an interesting perspective on the legal aspect of DMARC reports.

#### The turning point: Yahoo and AOL are forced to protect their domains with DMARC

 In early 2014, one of the world’s biggest ISPs was confronted with abuse of their existing addresses. Many Yahoo addresses were known by spammers and not used to send mail *to*, but to send mail *from*. Because it was a common habit to send with your original Yahoo address through badly-configured mailing lists, unauthenticated mail from, for example, yahoo.com would not necessarily be quarantined or blocked. Without a DMARC policy, it was easy for spammers to use real Yahoo addresses to send from. As Yahoo published their DMARC reject policy, the world for many people was turned upside down. Suddenly, not only the spoofed emails stopped, but also legitimate mail from badly configured mailing lists was massively blocked. [This article](https://wordtothewise.com/2014/04/brief-dmarc-primer) clearly describes the confusion that occurred the next day. Abuse rates coming from Yahoo addresses went quickly down, but now suddenly AOL addresses were the target of abuse. At this point, also AOL changed their DMARC policy to "reject". Meanwhile, even Gmail has expressed their intention to change their DMARC policy to "reject", and just in time, too.

#### Recent developments

 This means we are certainly looking at a world where full DMARC protection is becoming more and more of a standard. The latest DMARC standard, rfc7489, was released only in the spring of 2015, and in February of that year, Google manager John Rae Grant was quoted: "If your domain doesn’t protect itself with DMARC, you will be increasingly likely to see your messages sent directly to a spam folder or even rejected." (<http://dmarc.org/2015/02/dmarc-is-a-proven-tool-in-the-fight-against-fraudulent-email/>).

#### How does DMARC affect deliverability?

 DMARC allows ISPs to rely more on domain reputation. Especially when sending via shared IPs, a good domain reputation can be helpful in delivering your emails to the right place. Any domain owner that does not protect with DMARC is vulnerable for phishing and spoofing abuse, and if your domain can be abused by a third party, your domain reputation will most likely suffer. But there's more than that. Many senders use link tracking methods to track clicks. Some of those trackable links have the same characteristics as links used in phishing emails. Using badly-designed trackable links may lead to emails landing in the spam folder or even being blocked, unless DMARC is being used. DMARC excludes the possibility that badly-designed or formatted emails can be taken as phishing attempts.

#### Setting up DMARC

 Before you can fully protect your domain with DMARC, it may be useful to test if all the mail you send from all environments you use is properly authenticated. This can be done with a policy set to "none" or "quarantine" and reporting mode on. You should be able to read the reports you receive in order to determine if your authentication works as expected. As soon as SPF and DKIM are assured to be fully in line on all affected infrastructure, it is safe to change the policy to "reject". DMARC records are valid for all subdomains of the domain it is configured with. For example, a standard DMARC record on *example.com* also applies to *subdomain.example.com*. For optimal protection of your brand, it is recommended to set DMARC at the highest domain-level possible.