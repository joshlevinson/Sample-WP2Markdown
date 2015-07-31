---
title: 'Using HTTPS Requests to Import Data'
subject: Gettingstarted
old_url: 'http://emarsys.dev/old/getstarted/contact-data/http-requests/'
---

Suite can take advantage of any existing forms you have by using background HTTPS requests, using one of two methods. These features require some technical understanding on your part but are considerably quicker and easier than using the API.

- **register.php** For this feature you need to create a form in Suite to host the required fields, then use that form ID and the field IDs in a URL that can be called by your web page. Duplication handling is performed according to your standard settings (e.g. using first name, last name or email address, or the field that has been specified as external key). This method can handle a large volume of requests (up to 10,000 per hour) but does not return a contact ID, so responses cannot be tracked from outside Suite, and contact updates are queued so are not always immediate.
- **register_bg.php** For this feature you only need a form ID - the form itself does not need any fields or content. Any fields can be used, and you are free to specify any one as the external key for duplication handling. This method is faster, updating the data immediately, and does return a contact ID, but is more suitable for lower volumes (around 3,000 requests per hour).

 Both of these are very simple and flexible ways to use any web event to send real-time updates to your Suite database, and can also link these forms to an email campaign in Suite and trigger transactional emails. If you are interested in using this method to import data, please pass this document on to your technical support:

- [Using HTTPS Feeds in Suite](/Suite/http-feeds.md "Using HTTPS Feeds in Suite")