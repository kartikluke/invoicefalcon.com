---
layout: post
title:  "Collect payments for unpaid invoices with Stripe"
category: [Payments]
teaser: "With Invoice Falcon, you can collect payments for your invoices & quotes with Stripe"
---

With Invoice Falcon, you can collect payments for any of your unpaid or due invoices with Stripe. Send an email to your customer with a payment link that takes them to a checkout on your Stripe account. As soon as they make a payment, you'll be notified of it via email. And the best part - we do not collect the amount on your behalf; any payments made by your customers goes directly to your Stripe account!

To send an email with a payment link for an invoice, please follow the steps below -

<br/>
#### Connect Invoice Falcon to your Stripe account

![an image alt text]({{ site.baseurl }}/assets/img/payments/payment-stripe.png "Connect Invoice Falcon to your Stripe account")

1. Click on 'Collect Payments' in the left menu bar of our app.
2. Here, you'll find 2 separate fields - one for your publishable key and another for your secret key. Both keys are required in order to create & send a payment link.
3. In a separate tab, head over to your Stripe dashboard by clicking on this link - [Stripe Dashboard](https://dashboard.stripe.com) (or alternatively you can copy this link too - https://dashboard.stripe.com)
4. Click on 'Developers' -> 'API Keys' in the left menu bar.
5. On this page, you'll find 2 keys listed in the 'Standard Access' section. Copy and paste both keys in the respective field in our app.
6. Click 'Save Changes'

<br/>
<hr/>
<br/>

#### Send an email with a payment link


Now that you've successfully set up your Stripe account with our app, you can send an email with a payment link to your customer.

![an image alt text]({{ site.baseurl }}/assets/img/payments/payment-email.png "Send email with a payment link")

1. Click on **Invoices** tab in the left menu bar of our app.
2. Here, you'll find a list of all the orders from your Shopify store.
3. Once you've found the order you're looking for, click on the blue highlighted order name to generate the invoice for that order. This will redirect you to the Invoice Preview page, where you can review the invoice.
4. Click 'Send' -> 'Review & Send' from the dropdown
5. <b>enable</b> the checkbox labelled 'Send email with payment link'.
6. Review your email and click 'Send Invoice' to send the invoice with the payment link to your customer!
