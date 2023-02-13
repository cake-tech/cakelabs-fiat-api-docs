---
title: "rates"
parent: v1 (Deprecated)
---

# rates

The API available at `/v1/rates` accepts a fiat currency as a parameter and returns information for that fiat currency.

This v1 delivery is not optimized.

Example request:

> https://fiat-api.cakewallet.com/v1/rates?convert=usd

Exemple response:

```
{"data":[{"symbol":"LTC","quote":{"USD":{"price":89.20870293130763}}},{"symbol":"XMR","quote":{"USD":{"price":154.10500000000002}}},{"symbol":"XHV","quote":{"USD":{"price":0.5545586317974199}}},{"symbol":"BTC","quote":{"USD":{"price":21619.867766156218}}}]}
```

You are not allowed to use this API endpoint for any applications.
