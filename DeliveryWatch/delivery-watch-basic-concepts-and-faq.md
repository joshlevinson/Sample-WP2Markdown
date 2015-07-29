---
title: 'Delivery Watch Basic Concepts and FAQ'
subject: DeliveryWatch
old_url: 'http://emarsys.dev/ebene2-2/delivery-watch-basic-concepts-and-faq/'
---

Introduction
------------

 When email marketing first emerged, it quickly became apparent that sending improved content at faster speed is not in itself enough to improve campaign deliverability and increase the campaign penetration rate. Email by its nature, is an insecure method of sending information over the internet, and as a result the need to estimate the inbox delivery rate and assess the sender authentication has emerged. Delivery Watch is a tool kit designed to analyze and address any potential deliverability issues of any given email campaign as it is sent, thereby ensuring the quality of a campaign. The tool kit works by assessing several aspects of the campaign to identify potential issues that can have a negative impact on deliverability, and subsequently the reputation of the sender. Delivery Watch tests all aspects of a campaign during sending to help maximize the deliverability rates, using the following modules:

- Campaign Module
- Spamfilter Module
- Monitoring Module (Blacklist, Mailserver Config, Mail Authentication)
- Analysis Module

 Each module is designed to test a specific aspect of the campaign, analyzing both the campaign and sender to identify weakness that are most commonly exploited (e.g. spamming, spoofing, etc.). By offering this service any potential configuration issues or reputation issues can be flagged and addressed to help maximize the deliverability of a campaign.

The Delivery Watch Toolkit
--------------------------

 The Delivery Watch tool-kit is an integrated solution which provides automated monitoring services for the complex landscape of email deliverability and, as a consequence, reputation building. By actively evaluating content against a variety of policy-enforcing mechanisms currently used by various players from large email providers through to individuals, who use anti-spam measures such as black/whitelisting, domain-based reputation scoring, etc. The four main core modules of the toolkit allow measuring the behavior of individual campaigns against various aspects that influence deliverability.

<table border="0" class="wikitable" style="width: 100%;"><thead><tr><th>Module Name</th> <th>Scope</th> </tr></thead><tbody><tr><td>Campaign Module</td> <td>Tests general ISP deliverability by maintaining a number of active mailboxes with all major email providers to estimate the respective inbox delivery rates.</td> </tr><tr><td>Spamfilter Module</td> <td>Tests content against all major spam filters using a mixture of server side plug-ins, client side plug-ins and external cloud-based services, in order to evaluate how they will categorize the campaign.</td> </tr><tr><td>Monitoring Module</td> <td>Tests configuration and reputation of the sending mail server by monitoring the various mail authentication checks, blacklists and standard no-use practices.</td> </tr><tr><td>Analysis Module</td> <td>Provides insightful content analysis of the campaign based on the testing done by the other modules.</td></tr></tbody></table>### The Campaign Module

 The Campaign Module provides an ISP tracking service, which works by testing the deliverability of an email campaign against the various major ISPs around the world, using a series of test-mailboxes set up with each ISP. The results from these mailboxes for the campaign can then be used to calculate the expected inbox delivery rates for the ISPs based on the test results. These test-mailboxes are referred to as the **seedlist**, and Delivery Watch monitors the deliverability outcome of test campaigns by categorizing the outcome as "pass", "spam" or "blocked/missing" for each ISP. The seedlist is grouped by region (North America, DACH, etc.) and Delivery Watch displays the results by region, where you can drill down by country to individual ISP mailboxes. The tracking process starts when a copy of the campaign mail (referred to as the "trigger email") is sent to a Delivery Watch mailbox, which is also part of the seedlist. The trigger email tells Delivery Watch that a new campaign has been sent and is waiting processing. The ISP tracking service compares the content of the trigger email with its counterparts from the seedlist mailboxes.

<table border="0" cellpadding="1" class="wikitable" style="width: 100%; border-width: 0px; border-style: solid;"><thead><tr><th style="text-align: left; border-color: #fff; background-color: #fff; color: #eb5a19;">**Please Note:**</th> </tr></thead><tbody><tr><td style="text-align: left; border-color: #fff; background-color: #fff; color: #555555;">Two campaigns are considered *identical* if the content is the same and arrives within 24 hours, but are considered *different* if they arrive more than 24 hours apart even if the content is the same.</td></tr></tbody></table> It is possible to avoid this behavior by ensuring a unique header is added to each campaign, which then enables campaign matching based using the header as the identifier. Campaign Module URL: [[1]](https://www.deliverywatch.net/campaign/listCampaigns.do)

### The Spamfilter Module

 The Spamfilter Module enables the deliverability of an email campaign to be tested against a selection of the most widely used spam filters available. By doing so the module identifies any potential issues with the campaign. This module uses an internal Delivery Watch mailbox which forwards the trigger mail to the spam filter environment, which tests the campaign against available anti-spam technologies. A copy of the email campaign is sent to the mailbox which then initiates the spam filter test, and presents the outcome per spam filter, as well as an overall summary. Each spam filter will flag the content as either "Inbox", "Spam" or "Pending" - along with an overall spam filter result for supported anti-spam technologies. Spamfilter Module URL: [[2]](https://www.deliverywatch.net/spamfilter/listReports.do)

### The Monitoring Module

 The Monitoring module is designed to help optimize the configuration and reputation of the mail servers used by Delivery Watch customers when sending their campaigns. To achieve this, the Monitoring Module is comprised of three sub-modules:

- Blacklist Module
- Mailserver Configuration Module
- Mail Authentication Module

 Any email campaigns sent to Delivery Watch for ISP Tracking (Campaign Module) automatically have the headers examined and compared with DNS information by the Monitoring Module.

#### The Blacklist Module

 The Blacklist Module makes sure that the senders IP-address or Return-Path domain does not appear on any blacklist by performing periodical checks against some of the most prominent and important blacklists. By using a DNS query, the status of a mail server is returned as either "OK" or "Fault", with the option to drill down to find out what the underlying fault reason is i.e. why it has been blacklisted. Blacklist Module URL: [[3]](https://www.deliverywatch.net/blacklist/listServers.do)

#### The Mailserver Configuration Module

 The Mailserver Configuration Module performs five types of configuration checks. Amongst others, it verifies information in the campaign email header related to the sending mail server. The following areas are addressed as part of this check:

- Confirm a valid DNS entry exists
- Verify the domain name is correct
- Confirm the sender is not an "Open Relay"
- Confirm sender’s IP address is not in a Dial-In IP range
- Confirm sender’s IP address is not in a known dynamic IP range

 If all five of these checks are successful then the status is “OK”, but if any one of these fails then the overall status for the Mail Server Configuration will be “Fault”. You can drill down to find out more details on which check failed, along with a verbose description of the results of all of the configuration checks run for the respective mail server IP-address.

##### Confirm a valid DNS entry exists

 The IP address of the mail server used to send the campaign is taken from the header of the email itself, and then compared against the DNS entry for the mail server. This check confirms the existence of a valid DNS entry for the server and also acts as a consistency check to ensure the campaign is sent from the same origin. Any detected inconsistency between the DNS entry and the information contained in the header, leads to a potential decrease in inbox delivery rates.

##### Verify the domain name is correct

 When the header of the campaign is examined to confirm a valid DNS exists, the domain name of the mail server is also identified. The domain name from the DNS entry is compared with the domain name in the header to ensure it matches. Any discrepancy between the domain entry information from the DNS entry and the information contained in the header, leads to a potential decrease in inbox delivery rates.

##### Confirm the sender is not an “Open Relay”

 A so-called 'Open Relay' is a mail server that does not require any authentication, or has no restrictions (e.g. IP restrictions) for allowing other hosts to send email through it. Open Relays are generally regarded as a likely source of spam, and if a mail server is flagged as one, then a potential result is a decrease in inbox delivery rates. When this check is performed, it simply sends a test mail to the server to see if it can be forwarded or not.

##### Confirm IP Address of sender is not in a Dial-In IP range

 The header of the email also reveals the IP of the mail server sending the message, which is then checked to make sure that it does not fall under a Dial In IP range. Dial-In IP ranges are anonymized because the originating IP is hidden, and the only visible IP address is from the dial in range. These IP ranges are usually not used for production mail servers as they are regarded as a potential source of spam. Any mail server flagged as using such an IP address, leads to a potential decrease in inbox delivery rates.

##### Confirm IP Address of sender is not in a known dynamic IP range

 The IP of the mail server from the email header is checked to make sure that it is using a static IP Address range, rather than one known for issuing dynamic IPs. Any mail server flagged as using such an IP address, leads to a potential decrease in inbox delivery rates. Mailserver Config Module URL: [[4]](https://www.deliverywatch.net/compliance/displayServers.do)

#### The Mail Authentication Module

 The Mail Authentication Module checks and makes sure that the IP address of the mail server derived from the header is authorized to send on behalf of the domain name that is listed in the Return-Path header. The check is performed by using the Sender Policy Framework (SPF) which helps identify if a sender address is faked, and there are four possible outcomes from this check:

<table class="wikitable"><thead><tr><th>Status</th> <th>Explanation</th> </tr></thead><tbody><tr><td>Pass</td> <td>The sender is authorized to send on behalf of the domain name contained in the Return-Path of the campaign mail header.</td> </tr><tr><td>Neutral</td> <td>Nothing can be said about the authorization status of the sender, the message should be accepted by the server.</td> </tr><tr><td>Soft-Fail</td> <td>The sender is not authorized to send on behalf of the domain name contained in the Return-Path of the campaign mail header, but the receiver should handle this failure generously. This outcome is intended for debugging purposes.</td> </tr><tr><td>Fail</td> <td>The sender is not authorized to send on behalf of the domain name contained in the Return-Path of the campaign mail header.</td></tr></tbody></table> The Mail Authentication Module will only return an "OK" if the SPF check outcome is a Pass, for any other outcome in the SPF check the outcome will be "Fault". You can drill down to find a verbose description of the results of SPF check for the campaign in question. Mail Auth Module URL: [[5]](https://www.deliverywatch.net/serverChecks/displayMailAuth.do)

### The Analytics Module

 The Analytics Module is comprised of 19 reports that are designed to provide detailed statistical information on the inbox delivery rate for the campaign, based on the characteristics such as email size, content type, sending frequency, etc.

<div class="center"><div class="floatnone">[![Sample Analytics Module report](/assets/images/DeliveryWatch_Concepts_and_FAQ_-_Page_07_Image_0002.png)](/assets/images/DeliveryWatch_Concepts_and_FAQ_-_Page_07_Image_0002.png)</div></div> The Analytics Module always displays the campaign information in two columns: the account campaign average vs. the global average. The parameters of the report can be adjusted to display results including what time frame to cover, industry sector, etc. Analytics Module URL: [[6]](https://www.deliverywatch.net/analytics/selectReport.do)

Working with Delivery Watch
---------------------------

 Delivery Watch is designed to help provide support for Emarsys customers seeking to improve their deliverability rates, and works by using a dedicated account for each customer. Larger customers are given their own Delivery Watch accounts, while all others will have their content sent to a dedicated Delivery Watch account created by Emarsys Support. Regardless of account, the monitoring is typically taken care of by Emarsys Support.

<table class="wikitable"><thead><tr><th>Customer Type</th> <th>Delivery Watch Account</th> </tr></thead><tbody><tr><td>A Key Gold</td> <td>- Dedicated account set up for customer
- Can have multiple accounts if needed
 
</td> </tr><tr><td>B C</td> <td>- Emarsys Support account used
 
</td></tr></tbody></table>### Setting up a Delivery Watch account

 To provide support using Delivery Watch an account must first be created according to the following steps:

1. Account Director or Head of Client Services approves the Delivery Watch account set-up request.
2. Account setup request is sent to Delivery Watch support with the following information: - Customer Name
- Customer Type
- Name of Emarsys Support representative

 Emarsys Support is responsible for monitoring the customer’s deliverability results in Delivery Watch. If a customer ends its contract with Emarsys, Emarsys Support must report this information to Delivery Watch support so that the account can be closed. If customers have been granted access to their Delivery Watch account (e.g. A, Gold, Key), then Emarsys Support must maintain administrator access, and provide the customer with user-level access only. More detailed information on how to do this is available in a separate document which is available from either 2<sup>nd</sup> level support, or Delivery Watch support itself.

### Providing Delivery Watch Support

 For Delivery Watch support, Emarsys Support acts as the initial point of contact for Emarsys customers; all other customers contact Delivery Watch support directly. It is always worth checking the available documentation if you have any queries or issues before contacting support. If you are unable to resolve the issue yourself, please escalate to Delivery Watch support with as much information as possible, including the account name and office location. Delivery Watch provides Emarsys with a dedicated email support service for all Delivery Watch customers on: [[7]](mailto:support@deliverywatch.com).

### Using the Web Service-API (WS-API)

 Some of the Delivery Watch modules can be accessed using a Web Service-API (WS-API), which enables third party applications to undertake testing and display the results in their GUIs. At present only the Campaign Module and Spamfilter Modules are accessible through the WS-API.

Troubleshooting and FAQs
------------------------

 The following section includes a number of frequently asked questions, common issues and provides guidelines on how to handle them.

### Campaign is not shown in Delivery Watch

 Delivery Watch registers a new campaign as soon as an email of the campaign is delivered to the trigger mailbox (displayed at the bottom of the seedlist as `cdw*@deliverywatch.com`). Make sure that this address is being included in the recipient list of the campaign in question; if it is missing, simply add it. If the problem persists please contact support.

### Campaign results missing on the bar

 The campaign was successfully registered by the system, but a large proportion is flagged as missing. The most common reason for results to be shown as missing is that the content was simply not present in the mailbox when the system queried it. If 100% of the campaigns are missing for all (or specific providers), then the reason might be that the addresses are missing from the seedlist and have not been sent to.

1. Check the sending log files to ensure recipients accepted the email using SMTP
2. Update your seedlist accordingly with the next campaign

 This is the most frequent problem users experience with the system. Alternatively, it could be that the system is unable to query the results, even though the emails were delivered successfully, e.g. POP3 providers prevent the viewing of folders other than the inbox, and so if the message has gone to the spam folder, then it cannot be viewed. Another reason for a large number of missing results is when ISPs experience technical difficulties which prevent Delivery Watch from pulling the results from the mailboxes, e.g. downtime. For a more detailed explanation contact the Deliverability department or Delivery Watch support.

### What to expect from pending SpamFilter results

 A spam filter check usually takes between 5-10 minutes. If results are still pending after 10 minutes (maximum length), then this indicates that there might be a problem with the system. The most common reason for this happening is that a spam filter has become corrupted, which needs to be reported to Delivery Watch support as soon as possible.

### What to do with Authentication warnings

 If you receive an authentication warning, contact the Deliverability department ([[8]](mailto:deliv@emarsys.com)) who are responsible for ensuring customer authentication setups are correctly performed. Please contact your local 2nd level support who can assist, or escalate to the Deliverability team as necessary.

<table border="0" cellpadding="1" class="wikitable" style="width: 100%; border-width: 0px; border-style: solid;"><thead><tr><th style="text-align: left; border-color: #fff; background-color: #fff; color: #eb5a19;">**Please Note:**</th> </tr></thead><tbody><tr><td style="text-align: left; border-color: #fff; background-color: #fff; color: #555555;">You cannot turn off these authentication checks as they are intentionally there to help ensure quality of the content, and help improve deliverability.</td></tr></tbody></table>### Multiple campaigns sent, but only one is visible on the dashboard

 The Campaign module uses a specific mechanism to filter out duplicate campaigns in order to help prevent monthly limits from being used up erroneously. Duplicate content, i.e. messages sent by mistake or due to an inappropriate setup, are filtered by this mechanism which checks the content (header + body) it flags as identical when there is 91% or more match between this content and an existing campaign. Any content that is flagged as identical and sent within 24 hours of the initial campaign registration with Delivery Watch is classed as duplicate content, and not included in the dashboard. For any duplicate that Delivery Watch detects a notification email is triggered to the admin email address.

<table border="0" cellpadding="1" class="wikitable" style="width: 100%; border-width: 0px; border-style: solid;"><thead><tr><th style="text-align: left; border-color: #fff; background-color: #fff; color: #eb5a19;">**Please Note:**</th> </tr></thead><tbody><tr><td style="text-align: left; border-color: #fff; background-color: #fff; color: #555555;">Due to technical reasons, all deliverywatch.com mailboxes are currently only accessible by members of the Delivery Watch support team.</td></tr></tbody></table>### Bug reporting process

 For any bug reporting, or improvement suggestions (e.g. formatting issues, outdated information, etc. ) please contact Delivery Watch support, with as much information as possible using the support address: [[9]](mailto:support@deliverywatch.com).