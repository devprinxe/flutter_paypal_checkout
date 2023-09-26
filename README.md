# ✨ Flutter Paypal Easy Checkout

Flutter Easy Checkout is a flutter plugin that makes it easy to integrate paypal checkout in your flutter application.

## 🎖 Installing

```yaml
dependencies:
  flutter_paypal_easy_checkout: ^1.0.4
```

### ⚡️ Import

```dart
import 'package:flutter_paypal_easy_checkout/flutter_paypal_checkout.dart';
```

## 🎮 How To Use

```dart
Navigator.of(context).push(
MaterialPageRoute(
builder: (BuildContext context) => PaypalEasyCheckout(
sandboxMode: sandbox,
clientId: paypalClientId,
secretKey: paypalClientSecret,
returnURL: "https://samplesite.com/return",
cancelURL: "https://samplesite.com/cancel",
transactions: [
{
"amount": {
"total": "100.99",
"currency": "USD",
"details": {
"subtotal": "100.99",
"shipping": '0',
"shipping_discount": 0
}
},
"description": "Purchase For something",
"payment_options": {
  "allowed_payment_method":
      "INSTANT_FUNDING_SOURCE"
},
"item_list": {
"items": [
{
"name": "Product name",
"quantity": 1,
"price": "100.99",
"currency": "USD",
}
],
}
}
],
note: "Contact us for any questions on your order.",
onSuccess: (Map params) async {
print(params);
},
onError: (error) {
print(error);
},
onCancel: (params) {
print(params);
}),
),
);
```


## 🐛 Bugs/Requests

If you encounter any problems feel free to open an issue. If you feel the library is
missing a feature, please raise a ticket on Github and I'll look into it.
Pull request are also welcome.



## ⭐️ License

MIT License