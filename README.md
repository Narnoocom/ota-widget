# ota-widget
Our OTA inspired embeddable widget - V1.0 - Feedback encouraged!

# Installation Process
There are two widgets that need to be embedded into a website to make the booking flow work.
1. The availability widget which determines the availability of the product and any pickups or extras. This widget creates the information for the cart.
2. The cart widget which displays the customer's products and continues with the payment process.

## Demo
[Checkout the demo](https://narnoocom.github.io/ota-widget/product.html "Demo Product Page")

## The Availability Widget
This widget is displayed on the listings page or anywhere that you require a product to be booked.

### Source Files
The CSS and JS files need to be added to the pages:
CSS::https://d2amq67wh0wnea.cloudfront.net/availability/tours/css/app.css
JS::https://d2amq67wh0wnea.cloudfront.net/availability/tours/js/app.js

To render the widget we use a component tag.

```html
<link href="https://d2amq67wh0wnea.cloudfront.net/availability/tours/css/app.css" rel="stylesheet" />
<narnoo-availability-widget
access_key = ""
operator_id = ""
booking_id = ""
checkout_url = ""
booking_code = ""
></narnoo-availability-widget>
<script src="https://d2amq67wh0wnea.cloudfront.net/availability/tours/js/app.js"></script>
```

| Key           | Value         |Description           | Required  |
| ------------- |:-------------:| :--------------------| :---------:|
| access_key    | (string)      | API Access key       | YES |
| operator_id   | (string)      | Narnoo Operator Id   |   YES |
| booking_id    | (string)      | Narnoo Product Booking Id | YES |
| checkout_url  | (string)      | URI to a cart page on the website | YES |
| booking_code  | (string)      | Booking code for a single product when there are multiple products available. Common with Respax integrations.  |    NO |

## The Cart Widget
This widget is used to manage the product cart and continue with the booking process. It requires it's own page on the website.

> This widget uses internal routing, therefore it should be implemented on a server. It can be on your localhost, however you will need to be running a server such as MAMP. It defaults to a 'checkout' page URI. If there are conflicts with this we can look at altering it.

### Source Files
The CSS and JS files need to be added to the pages:
CSS::https://d2amq67wh0wnea.cloudfront.net/cart/ota/css/app.css
JS::https://d2amq67wh0wnea.cloudfront.net/cart/ota/js/app.js

To render the widget we use a component tag.

```html
<link href="https://d2amq67wh0wnea.cloudfront.net/cart/ota/css/app.css" rel="stylesheet" />
<narnoo-cart-widget></narnoo-cart-widget>
<script src="https://d2amq67wh0wnea.cloudfront.net/cart/ota/js/app.js"></script>
```