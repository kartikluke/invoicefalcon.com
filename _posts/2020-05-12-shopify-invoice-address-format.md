---
layout: post
title:  "Change the address format in your invoice"
category: [Design your invoice]
teaser: "Learn how to change the default address format by setting up an address template"
---

Click on **Invoice Design** in the left menu bar of our application & click on **Supplier, Shipping & Billing Addresses** section in this page. Scroll down till you find the 'Address Template' section, where you'll find a field that looks like this -

![an image alt text]({{ site.baseurl }}/assets/img/design-invoice/address-format.png "Set up your address template")

<br/>
**<u>Address template</u>**
<br/>

In this field, you can enter a custom address template based on your region's address system. The address is split into multiple parts like the Address line 1, Address line 2, country, city, pin code etc. For each of these parts, we support a liquid variable that you can place in combination with any other variable.

For example, if you'd like to show your addresses without the country, you can enter and save a template like this -

{% raw %}
    {{first_name}} {{last_name}}
    {{address1}}
    {{address2}}
    {{city}}
    {{province}}, {{zip}}
{% endraw %}

<br/>
Here's a full list of liquid variables available for setting up your address template -


Variable | Type
--- | ---
{% raw %}{{first_name}}{% endraw %} | Customer's first name
{% raw %}{{last_name}}{% endraw %} | Customer's first name
{% raw %}{{address1}}{% endraw %} | Address line 1
{% raw %}{{address2}}{% endraw %} | Address line 2
{% raw %}{{city}}{% endraw %} | City
{% raw %}{{province}}{% endraw %} | Province/State
{% raw %}{{country}}{% endraw %} | Country
{% raw %}{{zip}}{% endraw %} | Zipcode/Pincode

Note - if there's an error with using your custom address template, your invoices will use the default address template.

<br/>
<hr/>
<br/>

Make sure to click 'Save Changes' after you're done! Your existing invoices will be automatically updated to include the changes you made here the next time it's printed, sent or downloaded. :)
