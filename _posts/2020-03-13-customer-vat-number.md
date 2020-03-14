---
layout: post
title:  "Add your customer's tax/VAT number to the invoice"
category: [Manage Customers]
teaser: "Learn how you can add your customer's tax/VAT number to your documents."
---

#### From Invoice Falcon
When you generate an invoice for an order with Invoice Falcon, your customer's details get automatically saved into our app. After your customer is visible in the 'Customers' list of our app, you can add their tax registration/VAT number and it will be shown on the invoices for all their future purchases.

![an image alt text]({{ site.baseurl }}/assets/img/print-invoice/customer-tax.png "Add your customer's tax/VAT number to the invoice")

<br/>
1. Search for the customer for whom you'd like to add the tax registraation/VAT number in the 'Customers' tab.
2. Click 'Edit Details' button on the right side of the row containing the customer's name.
3. In the field labelled 'VAT/Tax number', enter the customer's tax registration/VAT number like this - 'VAT: XXXX123456'.
4. Click 'Save Changes'
5. Your existing invoices will be automatically updated to show the customer's number underneath their billing address.

<br/>
<hr/>
<br/>

#### During checkout
You can include a VAT/Tax Number field on your cart page so that your customers can enter their VAT number just before checkout. These numbers will be stored as cart attributes. We will then automatically pick up this number saved in the order and show it in the invoice.

To add this field to your cart page, please follow these steps below -

1. Click on 'Online Store' -> 'Themes' in your Shopify dashboard.
2. Next, click on 'Actions' -> 'Edit Code'
3. Search for and click on the file labelled **cart.liquid** or **cart-template.liquid** (depending on your theme file)
4. Insert this snippet of code into this file in the section containing the 'Update' & 'Checkout' buttons -

{% raw %}
    `<!-- Invoice Falcon VAT code START -->
    <input type="text" name="attributes[vat-id]" placeholder="Enter your VAT #" value="{{ cart.attributes['vat-id'] }}" />
    <!-- Invoice Falcon VAT code END -->`
{% endraw %}

5. Click 'Save' in the file editor. That's it!

Here is what the code will look like in your file after you add the snippet -

![an image alt text]({{ site.baseurl }}/assets/img/print-invoice/customer-tax-code.png "Add your customer's tax/VAT number to the invoice")

<br/>
<hr/>
<br/>

#### Using Exemptify
If you'd like to avoid the hassle of modifying your theme files, we'd highly recommend that you check out Exemptify ([Link](https://apps.shopify.com/exemptify)) from our friends at Modules4U! Exemptify contains plenty of features that automatically captures and validates your customer's VAT IDs. These IDs are then sent in your Shopify order details to us and they will automatically appear on the order's invoices when you generate them.
