---
title: 'Example 2: Post-Purchase Campaign'
subject: 'Getting Started, GettingStarted_Predict, Predict'
old_url: 'http://emarsys.dev/predict/use-cases/email-purchase/'
---

In this example we have followed up on a purchase with a thank you message and some additional recommendations. For this we have used the ***Post-Purchase** *widget to display two sets of three recommendations that might also interest the customer.[![Predict_EMRER_email_2](/assets/images/Predict_EMRER_email_2.png)](/assets/images/Predict_EMRER_email_2.png)This campaign also uses a recurring filter, and again includes an A/B to measure its efficacy. The follow-up email is sent seven days after the purchase. [![Predict_EMRER_program_2](/assets/images/Predict_EMRER_program_2.png)](/assets/images/Predict_EMRER_program_2.png)

#### Required segments and filters

- Last purchase date was in the last 2 days

This filter is intended to check whether the data field change reflects a purchase which occurred today or yesterday (in case of time zone variations).

[![](/assets/images/predict_last_purchase_date_in_last_2_days-300x110.png)](/assets/images/predict_last_purchase_date_in_last_2_days.png)- Last purchase date was in the last 6 days

Although the node says 'in the last 5 days', we also need to include the first day as well as today, so the filter must include one extra day.

[![predict_last_purchase_date_in_last_6_days](/assets/images/predict_last_purchase_date_in_last_6_days-300x112.png)](/assets/images/predict_last_purchase_date_in_last_6_days.png)