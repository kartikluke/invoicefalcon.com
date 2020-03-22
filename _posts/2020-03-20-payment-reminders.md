---
layout: post
title:  "Send payment reminders for unpaid invoices automatically"
category: [Payments]
teaser: "Send email payment reminders for all unpaid/due invoices automatically to your customers"
---

Are you sending invoices to your customers with payment terms or a due date? Now, with Invoice Falcon, you can send payment reminder emails automatically for each invoice to your customers. You can choose to send the reminder every few days until the payment is made, or after the due date lapses. Set the reminders and forget it; Invoice Falcon will ensure that the emails are sent & that you get your payments on time.

In this article, we've outlined the settings available to you to send a payment reminder email to your customer.

<br/>
#### 1. Enable Payment Reminders
![an image alt text]({{ site.baseurl }}/assets/img/payments/reminder-toggle.png "Enable Payment Reminders")

To enable manual & automatic payment reminder emails to your customers, click on the 'Enable' button in the 'Enable/disable all payment reminders' section.

When this toggle is enabled but the 'Automatic Payment Reminders' is disabled, you can send a payment reminder email for a specific invoice by clicking 'Send' -> 'Turn on Payment Reminders'.

Please note that if this toggle is disabled, payment reminders of both types, manual and automatic, will NOT be sent to your customer.

<br/>
<hr/>
<br/>

#### 2. Add your reminder email template
![an image alt text]({{ site.baseurl }}/assets/img/payments/reminder-email.png "Add payment reminder email template")

Unfortunately, at this time, we do not have a default email subject & body for the reminder template. If you wish to send payment reminder emails to your customer, please set up your email template in this section.

We've provided a few liquid variables that you can use in your reminder email template. Please note that these variables need to be exactly as they look in the Variables section. If they are not as specified, there may be issues with sending the emails to your customer.

To use a liquid variable in your template, simply copy the variable you need by selecting the text, pressing Ctrl+C or Cmd+C and then pressing Ctrl+V or Cmd+V in any of the fields.

When the email is sent to your customer, these fields will be resolved and replaced with the actual data for that invoice.

<br/>
**<u>How do I use the {% raw %}{% if invoice.requires_payment %}{% endraw %} variable?</u>**
<br/>
This variable is designed to add a Stripe payment link to the invoice email. When this variable is added to your template, a piece of text (asking your customer to pay) and a link to complete the payment will be shown to your customer.

Please note that setting up this payment link requires an Ultimate subscription and a Stripe account.

To use this variable, please copy the following snippet of code to your email template -

{% raw %}
    {% if invoice.requires_payment %}
    Please complete the payment for your order by clicking on this link - {{ invoice.payment_link }}
    {% endif %}
{% endraw %}

Note - You can replace the text 'Please complete the payment for your order by clicking on this link' with any text of your choice. When updating this text, please ensure that '- {%raw%}{{ invoice.payment_link }}{%endraw%}' is still present at the end of that line.

<br/>
<hr/>
<br/>

#### 3. Set your schedule
![an image alt text]({{ site.baseurl }}/assets/img/payments/reminder-settings.png "Add payment reminder email template")

<br/>
**<u>Reminder Email CC</u>**
<br/>
To receive a copy of the reminder email when it is sent to your customer, enter the email addresses in the 'CC email addresses' field in this section.

If you want to send payment reminders for unpaid/due invoices to yourself and not to your customer, enable the checkbox labelled 'Send all payment reminders to these email addresses only.'

<br/>
**<u>Schedule Reminders</u>**
<br/>
Here, you can set how often the reminder email should be sent by entering a certain number of days in the 'Send reminder every X days'. You can also choose to send the reminder email before or after the due date by selecting from the 'Send reminder' dropdown below.

Make sure to click 'Save Changes' after you've selected your settings.

<br/>
<hr/>
<br/>

#### 4. Automatically track unpaid orders and send payment reminders
![an image alt text]({{ site.baseurl }}/assets/img/payments/reminder-automatic.png "Automatically track unpaid orders and send payment reminders")

Enable this setting to let Invoice Falcon track your every order in your store in the background and automatically send payment reminders for orders that are not fully paid.

<br/>
<hr/>
<br/>

#### 5. Send a payment link in all payment reminder emails
![an image alt text]({{ site.baseurl }}/assets/img/payments/reminder-payment-link.png "Send a payment link in all payment reminder emails")

Enable/disable this setting to show a Stripe payment link in all reminder emails sent to your customers. Please note that this feature requires a Stripe account connected to Invoice Falcon.

After enabling this setting, a snippet of code needs to be added to your reminder email template. Please see '#2 - Add your reminder email template' section above to add the required snippet to your template.
