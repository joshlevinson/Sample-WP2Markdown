---
title: 'Example 1: Abandoned Cart Campaign'
subject: 'Gettingstarted, GettingStarted_Predict, Predict'
old_url: 'http://emarsys.dev/old/predict/use-cases/email-abandoned/'
---

In this example we use the ***Abandoned Cart** *widget to include two sets of three items in a standard cart abandonment email. You could also use this campaign to offer further incentives such as discounts or free shipping. [![Predict_EMRER_email_1](/assets/images/2014/06/Predict_EMRER_email_1.png)](/assets/images/2014/06/Predict_EMRER_email_1.png) In the program shown below we have included a simple A/B testing step to let you measure the success of using this simple campaign (90%) against not using it (10%). The results will be visible on the **Program Summary** page. To avoid sending too many emails to serial browsers, we would suggest limiting participation to every once every 30 days for this program; if incentives are included, you might even want to make this a one-time only campaign, or increase the participation period to 180 days. [![Predict_EMRER_program_1](/assets/images/2014/06/Predict_EMRER_program_1.png)](/assets/images/2014/06/Predict_EMRER_program_1.png)

#### Required segments and filters

- Last abandoned date was in the last 2 days

This filter is intended to check whether the data field change reflects an abandoned cart which occurred today or yesterday (in case of time zone variations).

[![](/assets/images/2014/07/Predict_last_abandon_date_in_last_2_days-300x110.png)](/assets/images/2014/07/Predict_last_abandon_date_in_last_2_days.png)- Last purchase date was in the last 6 days

Although the node says 'in the last 5 days', we also need to include the first day as well as today, so the filter must include one extra day.

[![predict_last_purchase_date_in_last_6_days](/assets/images/2014/07/predict_last_purchase_date_in_last_6_days-300x112.png)](/assets/images/2014/07/predict_last_purchase_date_in_last_6_days.png)