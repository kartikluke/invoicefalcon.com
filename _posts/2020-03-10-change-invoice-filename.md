---
layout: post
title:  "Change the attachment/download filename for your invoices"
category: [Send Invoices]
teaser: "Set up the filename that you or your customers will see when an invoice is downloaded/sent."
---

When you download an invoice or send it to your customer from Invoice Falcon, the invoice is sent as a PDF with the file name being the name of the order. That is, if the order for which you are generating the invoice is '#1089', then the filename will be '#1089.pdf'. In this article, we'll walk you through how you can change this to a name of your choice.

Click on **Invoice Settings** in the left menu bar of our application. You'll see a few settings that look like this -

![an image alt text]({{ site.baseurl }}/assets/img/send-invoice/filename.png "Change filename")

In the section labelled "Download/attachment filename", you'll find a text field where you can change the name of the PDF file. We've exposed a few liquid variables that you can use to further customise the name.

<br/>
**<u>{%raw%}{{shop.name}}{%endraw%}</u>**
<br/>
This will resolve to the name of your Shopify store in the file name.


<br/>
**<u>{%raw%}{{order.name}}{%endraw%}</u>**
<br/>
This variable will resolve to the name of the order for which the invoice was generated. For example - 'IFS-1080-EN', '#1089' etc.

<br/>
**<u>{%raw%}{{invoice.number}}{%endraw%}</u>**
<br/>
This variable will resolve to the specific number of the invoice. Use this variable if you have a custom invoice numbering sequence or if you're using a number prefix. For example - 'ABRN1239090', 'INV-987899'

<br/>

Example - if you'd like your filename to 'FalconStore - Invoice ABRNH12340 for Order #1089', then you can set up the text in the field as - '{%raw%}{{shop.name}}{%endraw%} - Invoice {%raw%}{{invoice.number}}{%endraw%} for Order {%raw%}{{order.name}}{%endraw%}'

<br/>
<hr/>
<br/>

Make sure to click 'Save' after you're done! Your existing invoices will be automatically updated to include the changes you made here the next time it's printed, sent or downloaded. :)
