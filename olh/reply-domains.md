---
title: 'Admin - Domain Setup for Reply Management'
subject: 'olh, SuiteAdmin'
old_url: 'http://emarsys.dev/suite/online-help/reply-domains/'
---

**Admin** menu ->** Reply Management** To set up a dedicated domain for reply management, proceed as follows: 1. Register a domain or create a subdomain.

**Attention**: Domains/subdomains which were already set up for the display of trackable links in Emarsys eMarketing Suite and changed to Emarsys per C-Name entry, **cannot** be used.

1. Have your provider or network administrator show you the MX record of the domain or subdomain for Emarsys eMarketing Suite. The name server entry for the MX record must changed.

- If you make the entry in an administration menu interface, enter mx.eemms.net. as a target in the MX entry of the favoured domain or subdomain. All other settings can remain unchanged.
- If you make the entry via an admin-console, enter the following in the zonefile of the domain/subdomain:


IN                MX                10             mx.eemms.net

1. Please provide your Emarsys Account Manager with the domain/subdomain name used, so that we can activate the domain/subdomain for your account.