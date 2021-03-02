---
layout: post
title:  "Add links to invoices in Customer account page"
category: [Include links to invoices]
teaser: "Let customers download the invoice for any order in their account history."
---

With Invoice Falcon, you can add a link to your customer's account page so that they can download the invoice for their orders anytime.

When your customer clicks on this link, they will be redirected to a PDF version of the invoice & they can choose to print the invoice or download it to their device.

To add the links to your customer account page, you will need to make a few small changes to your theme files -

1. Click on __Online Store__ -> __Themes__ in your Shopify admin dashboard.
2. Click on __Actions__, and then click __Edit Code__.
3. Next, you'll need to enter this snippet of code into your theme files.

<br/>
#### Templates -> customers/account.liquid
Here, you'll need to add a new column called "Download Invoice" for each order. Each row in this column will have a link and clicking on the link will take the customer to a new tab with their invoice ready to print or download.

Look for this line of code in the file - `<td data-label="{{ 'customer.orders.total' | t }}">{{ "{{ order.total_price | money " }}}}</td>`

Press Enter and right underneath this line, add the below snippet of code to the file -

`<td><a href='https://app.invoicefalcon.com/pdfs/{{ "{{ order.id " }}}}.pdf?shopify_domain=invoicefalconstore.myshopify.com&uuid={{ "{{ order.order_number " }}}}'>Download Invoice</a></td>`

Note - _Replace 'invoicefalconstore.myshopify.com' with your store's myshopify link._  

Click _Save_ and that's it! Your customer account page will be automatically updated to include the new column. :)
