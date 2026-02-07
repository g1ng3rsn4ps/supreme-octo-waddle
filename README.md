# supreme-octo-waddle

Liquid/CSS for Shopify to make a "X Dollars Until Free Shipping" Cart Notification/Sticky Banner.

This code is designed to encourage customers to increase their average order value to your Shopify store's free shipping threshhold. Unlike 3rd party Shopify apps, which can slow your page's load time and performance, this workaround keeps your site snappy while also engaging customers.

The CSS is written so as to automatically match your store's theme settings. The notice and sticky banner are fully mobile-compliant and optimized.

Please note that this will not automatically update the sticky banner at the top of the page without a refresh. If you want it to update automatically without refreshing, you must use JS or AJAX, but it will add additional script processing time, which this workaround aims to avoid.

Also please note that you may need to add these snippets into different locations in your Shopify theme's code; the instructions attached are for two of the most commonly used free themes, Dawn and Crave 15.4.1, which have very similar source code collections.

INSTRUCTIONS:

CART NOTIFICATION:

Start by adding the coundown to in the cart itself. For Crave 15.4.1, I used the main-cart-footer.liquid file to display the coundown after the total value of the order and above the checkout for max visibility. For Crave, that happens to be between <div class="totals"> and <small class="tax-note caption-large rte">. My store's free shipping threshhold is $75.00, which Shopify wants in cents, which is 7,500; you can change this in the {% assign free_shipping_threshold = 7500 %} line. Remember to change the monetary value in the message body as well so that it matches.

Next, go to the component-cart.css file and append the CSS to the very end of the file.

STICKY BANNER:

Navigate to the theme.liquid file. Immediately after the first <body> tag for Crave/Dawn, insert the header liquid.  After, go to base.css and append the CSS to the very end of the file.
