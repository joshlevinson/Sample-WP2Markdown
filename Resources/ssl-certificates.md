---
title: 'SSL Certification'
tags: 'Resources, Security'
old_url: 'http://emarsys.dev/resources/data-security/ssl-certificates/'
---

### What is SSL

 Secure Socket Layer (SSL) is a term used to describe a protocol for secure communication in computer networks, and in order to clearly identify the communication partners, so-called SSL certificates are used. Emarsys uses SSL certificates to encrypt the access to our services and to our customers’ link domains. [![SSL_Cert_Process_address bar](/assets/images/SSL_Cert_Process_address-bar.png)](/assets/images/SSL_Cert_Process_address-bar.png)

#### Practical Example

 A possible application for SSL certificates would be when using an authentication form. In such cases, users enter personal data, so security should is a must. All forms that involve personal data and all e-commerce applications should always make use of encrypted communication. The same can be said for registration confirmation pages, unsubscribe pages, or any other web resources central to your eMarketing activities: your customers must always feel that they are operating in a secure online environment. SSL certificates enable the web browser and the web server to build a secure, encrypted connection. A "handshake" process which establishes the session takes place behind the scenes, this is done by the web browser sending an encrypted file sample from your website which is then matched against a private key on your server. Once the secure connection is made, it is then represented by a small padlock icon in the browser’s address bar and the "https" (the 's' is for secure) prefix in the URL, which are the only visible indications of a secure session in progress. In contrast, when a user opens an unsecured website (i.e. one that is not protected with a valid SSL certificate), the browser’s security mechanism triggers a warning to the user, reminding them that the site is not secure and that sensitive data might be intercepted by third parties. Faced with such a warning message, most users will be reluctant to enter data into a form.

<div class="center"><div class="floatnone">[![SSL Certificate Warning](/assets/images/SSL_Cert_Process_SSLFailure.png)](/assets/images/SSL_Cert_Process_SSLFailure.png)</div></div> Once you have decided that you want to use encryption in communication with users, the goal would be that a secure web site can be accessed without triggering any warnings. A correctly implemented URL would look like this: `https://newsletter.yourdomain.com/u/register.php?CID=12345678&f=12345`

<table cellpadding="1" class="wikitable" style="width: 100%; border: 0px;"><tbody><tr><td scope="col" style="text-align: left; border: 0px solid #999; vertical-align: top;" width="60px">[![Icon BeCareful.png](/assets/images/Icon_BeCareful.png)](/assets/images/Icon_BeCareful.png)</td> <td scope="col" style="border: 0px solid #999; vertical-align: top; color: #555555;">As an alternative, the link above could also be converted to "normal" HTTP by removing the S in the URL - but in that case you would risk that users’ personal data might be stolen.</td></tr></tbody></table>### Obtaining a Certificate

<table cellpadding="1" class="wikitable" style="width: 100%; border: 1px solid #fff;"><tbody><tr><td scope="col" style="text-align: left; border: 1px solid #fff;" width="60px">[![Icon FurtherReading.png](/assets/images/Icon_FurtherReading.png)](/assets/images/Icon_FurtherReading.png)</td> <td scope="col" style="border: 1px solid #fff;">This section assumes that you are already familiar with creating forms in Suite. For more information, please see the *Suite Online Help*.</td> </tr></tbody></table>[![The Certification Process](/assets/images/SSL_Cert_Process_Process.png)](/assets/images/SSL_Cert_Process_Process.png) To obtain a certificate, proceed as follows:

- Create a Certificate Signing Request (CSR) file for the domain you are using. This file contains information about the domain ("who are you"). See below for further information on CSR files.
- Go to a Certification Authority (CA) and buy a certificate. Certificates are available with different contract periods, and are available for different operating systems. It is important that you make sure to choose the most appropriate from the following: - Single Certificate for only one domain, e.g. "newsletter.yourdomain.com"
- Wildcard Certificate for all first level subdomains below "*.yourdomain.com", which allows you to cover registration forms as well as web shops.
 
<table border="0" cellpadding="1" class="wikitable" style="width: 100%; border-width: 0px; border-style: solid;"><thead><tr><th style="text-align: left; border-color: #fff; background-color: #fff; color: #eb5a19;">**Please Note:**</th> </tr></thead><tbody><tr><td style="text-align: left; border-color: #fff; background-color: #fff; color: #555555;">The certificate must match the server’s operating system, which in the case of Emarsys this means selecting a certificate for a Linux operating system.</td></tr></tbody></table>- Once you have received the certificate from the CA, send the following two files to Emarsys: - Private key file (.key)
- Certificate file (.crt)
- Emarsys will then install the certificate and link them to the domain (e.g., newsletter registration form).
 
<table cellpadding="1" class="wikitable" style="width: 100%; border: 0px;"><tbody><tr><td scope="col" style="text-align: left; border: 0px solid #999; vertical-align: top;" width="60px">[![Icon BeCareful.png](/assets/images/Icon_BeCareful.png)](/assets/images/Icon_BeCareful.png)</td> <td scope="col" style="border: 0px solid #999; vertical-align: top; color: #555555;">Certificates must not be installed while campaigns are running!</td></tr></tbody></table>#### CSR Files

 A Certificate Signing Request (CSR) is an encrypted piece of data containing all your information (organization name, location, country, etc.) which you need when you want to buy a certificate from a Certification Authority (CA). The CA uses this information in order to create the SSL certificate which is then linked to the domain you created the CSR for, which is what makes the SSL connection possible. If you need help getting information about your domain, you can simply use the Whois protocol to find out all the relevant domain information. As the CSR file is linked to the domain, it needs to be created on the web server which is hosting your domain. You might need to contact a person with access to this server to create the CSR file for you.

<table cellpadding="1" class="wikitable" style="width: 100%; border: 0px;"><tbody><tr><td scope="col" style="text-align: left; border: 0px solid #999; vertical-align: top;" width="60px">[![Icon BeCareful.png](/assets/images/Icon_BeCareful.png)](/assets/images/Icon_BeCareful.png)</td> <td scope="col" style="border: 0px solid #999; vertical-align: top; color: #555555;">- If your domain is just a forwarding domain (A-Record), the CSR file needs to be created on the web server which is actually hosting the website!
- If you have a CNAME entry, remove it before installing the certificate.
 
</td> </tr></tbody></table><table border="0" cellpadding="1" class="wikitable" style="width: 100%; border-width: 0px; border-style: solid;"><thead><tr><th style="text-align: left; border-color: #fff; background-color: #fff; color: #eb5a19;">**Please Note:**</th> </tr></thead><tbody><tr><td style="text-align: left; border-color: #fff; background-color: #fff; color: #555555;">It is important that all data in a CSR file is an exact match for the information used when applying for a certificate. If not, the certification process might fail, or the certificate won’t work for the domain you actually want it for.</td></tr></tbody></table>#### Recommended Certification Authorities

 Emarsys recommends the following Certification Authorities

- Symantec (formerly VeriSign): <http://www.symantec.com/en/uk/ssl-certificates>
- Trustwave: <https://ssl.trustwave.com/>