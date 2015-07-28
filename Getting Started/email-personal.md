---
title: 'Example 3: Abandoned Browse Campaign'
tags: 'Getting Started, GettingStarted_Predict, Predict'
old_url: 'http://emarsys.dev/predict/use-cases/email-personal/'
---

In this example we use the **Mail Personal** widget to include two sets of three recommendations in an email sent after a visitor has browsed your web shop without adding any items to the cart or making a purchase.[![Predict_EMRER_email_3](/assets/images/Predict_EMRER_email_3.png)](/assets/images/Predict_EMRER_email_3.png) This program identifies all eligible visitors, waits for two days, and then sends the most up-to-date recommendations for each one. The two-day delay is designed to reduce the chance of coming across as overly aggressive. We would suggest a participation cycle of once every 14 days (or more) for this program.[![Predict_EMRER_program_3](/assets/images/Predict_EMRER_program_3.png)](/assets/images/Predict_EMRER_program_3.png)

#### Required segments and filters

- Last session time spent > 180 seconds

This filter includes only visitors who really spent time on your website (more than three minutes).

[![](/assets/images/Predict_last_session_over_180-300x110.png)](/assets/images/Predict_last_session_over_180.png)- Exclude: Last abandoned date was in the last 4 days

This filter ensures that the same contact will not also receive your [**abandoned cart program**](/Getting%20Started/email-abandoned.md).

![Predict_last_abandoned_in_last_4_days](/assets/images/Predict_last_abandoned_in_last_4_days-300x33.png)- Exclude: Last purchase date was in the last 4 days

This will ensure that you don't include customers who did return and complete their purchase.

[![predict_last_purchase_date_in_last_4_days](/assets/images/predict_last_purchase_date_in_last_4_days-300x32.png)](/assets/images/predict_last_purchase_date_in_last_4_days.png)- Last purchase date was in the last 6 days

 Although the node says 'in the last 5 days', we also need to include the first day as well as today, so the filter must include one extra day.

[![predict_last_purchase_date_in_last_6_days](/assets/images/predict_last_purchase_date_in_last_6_days-300x112.png)](/assets/images/predict_last_purchase_date_in_last_6_days.png)