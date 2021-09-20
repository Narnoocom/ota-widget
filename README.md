# ota-widget
Our OTA inspired embeddable widget

# Installation Process
There are two widgets that need to be embedded into a website to make the booking flow work.
1. The availability widget which determines the availability of the product and any pickups or extras. This widget creates the information for the cart.
2. The cart widget which displays the customer's products and continues with the payment process.

## The Availability Widget
This widget is displayed on the listings page or anywhere that you require a product to be booked.

### Source Files
The CSS and JS files need to be added to the pages:
CSS::https://d2amq67wh0wnea.cloudfront.net/availability/tours/css/app.css
JS::https://d2amq67wh0wnea.cloudfront.net/availability/tours/js/app.js

To render the widget we use a component tag.

<narnoo-availability-widget
access_key = ""
operator_id = ""
Booking_id = ""
checkout_url = "" //Required - used to send customer to checkout page after item added to cart. example: 'cart.html'
booking_code = "" //optional - used for products with multiple booking options per product. ( common with Respax )
></narnoo-availability-widget>

## The Cart Widget
This widget is used to manage the product cart and continue with the booking process. It requires it's own page on the website.

### Source Files
The CSS and JS files need to be added to the pages:
CSS::https://d2amq67wh0wnea.cloudfront.net/cart/ota/css/app.css
JS::https://d2amq67wh0wnea.cloudfront.net/cart/ota/js/app.js

To render the widget we use a component tag.

<narnoo-cart-widget></narnoo-cart-widget>