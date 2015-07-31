---
title: 'Integrating with External Applications'
subject: Gettingstarted
old_url: 'http://emarsys.dev/old/getstarted/contact-data/connect/'
---

Emarsys Connect is a family of products which offer out-of-the-box integrations with a number of third-party applications. These require no implementation efforts and are typically enabled via the app store (or similar) of the application in question. The functionality available varies from product to product, but will usually involve an initial export of all contacts from the product into Suite and then automatic synchronization in both directions when data is updated. If supported by the integrating application, transactional email can also be triggered. Email responses are sent at regular intervals from Suite to the integrating application. Although not as flexible as the API, these integrations provide great value to both Suite and the supported products as they are quick and easy to install. The products which integrate with Suite include:

#### AT Internet

- Click here for the [AT Internet Integration End-user Guide](/assets/images/2014/06/ATInternet-Integration-End-user-Guide-English.pdf)

#### Microsoft Dynamics

- Click here for the [MS Dynamics Integration End-user Guide](/assets/images/2014/06/MS-Dynamics-Integration-End-user-Guide-English.pdf)

#### Magento

- Click here for the [Magento Integration End-user Guide](/SuiteIntegrations/magento.md)

#### Gigya

- This integration is handled entirely by Gigya; Emarsys Support will provide them with the necessary account details.

 If you are using one of the applications listed here, but have not yet integrated it with Suite, please contact Emarsys Support for more information. Some integrations offer a test facility, or sandbox, which you can use for testing purposes before linking the live integration with Suite. This is indicated by a checkbox which you must activate before setting up the integration. **Please Note:** in order for these integrations to work, you must have API access (which Emarsys Support will create for you) and a field in your Suite DB called **externalId**, which you must create yourself.

### Smart Insight

 [Defcon1] Smart Insight uses a separate data warehouse, and the contact properties and responses are synchronized between the Suite database and Smart Insight automatically. External data sets can be pulled from any source and placed on a secure server (FTPS) in .CSV format. Smart Insight collects this file once a day and adds the data to the relevant tables.