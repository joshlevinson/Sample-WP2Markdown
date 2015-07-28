---
title: 'The Web Extend Fields in Suite'
tags: 'Getting Started, GettingStarted_Suite, WebExtend'
old_url: 'http://emarsys.dev/web-extend/implementation/fields/'
---

The data that Web Extend collects on your web shop is sent to the Predict Servers for analysis, but at the same time the Suite database is updated daily with the latest information on the activities of known customers (i.e. who logged in to the web shop or who reached it via an Emarsys email, so that their web shop ID and Suite contact ID are matched). This data can be used by you to launch targeted product campaigns, such as cart abandonment or stock clearance.

<table border="0" class="wikitable" style="width: 100%;"><caption>##### Web Extend fields in Suite

 </caption> <thead><tr><th>Field name</th> <th>Field type</th> <th>Description</th> </tr></thead><tbody><tr><td>predict last session date</td> <td>Date</td> <td>The last time the contact interacted with the website, expressed in YYYY-MM-DD format.</td> </tr><tr><td>predict last session time spent</td> <td>Numeric</td> <td>The duration of the last session, in seconds, maximum 1800 (30 minutes).</td> </tr><tr><td>predict last session categories</td> <td>Text (255 chars)</td> <td>The categories of the products viewed in the last session, maximum 10.</td> </tr><tr><td>predict last abandoned date</td> <td>Date</td> <td>The date when a product was last abandoned, expressed in YYYY-MM-DD format.</td> </tr><tr><td>predict last abandoned categories</td> <td>Text (255 chars)</td> <td>Categories of products abandoned in the cart, maximum 10.</td> </tr><tr><td>predict last abandoned total price</td> <td>Numeric</td> <td>Total price of all products left in the cart, using the currency value of the website itself.</td> </tr><tr><td>predict last purchase date</td> <td>Date</td> <td>The date of the last purchase, expressed in YYYY-MM-DD format.</td> </tr><tr><td>predict last purchase categories</td> <td>Text (255 chars)</td> <td>The categories of products bought in the last purchase, maximum 10.</td> </tr><tr><td>predict last purchase total price</td> <td>Numeric</td> <td>Total price spent in the last purchase.</td> </tr></tbody></table> If you are using the Suite interface in a language other than English, you will need to make sure that these fields have the correct name in both English and that language. A full list of translations is available on the next page.