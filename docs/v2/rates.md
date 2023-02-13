---
title: "rates"
parent: v2
---

# rates

`/v2/rates`: GET

Query parameters:

* (Optional) `base`: the base symbol *(default value: XMR)*
* (Optional) `quote`: the quote symbol *(default value: USDT)*
* (Optional) `interval_minutes`: the amount of time in minutes to use between price points. *(default value: 60)*
* (Optional) `interval_count`: the number of historical time points to return *(default value: 24)*
* (Optional) `date`: [ISO8601 formatted date](https://en.wikipedia.org/wiki/ISO_8601) which represents the starting point that `interval_count` and `interval_minutes` will move backwards in time from. *(default value: [NOW] - 90 seconds)*

Response with the default parameters:

```
{
	"base": "XMR",
	"errors": {},
	"interval_count": 24,
	"interval_minutes": 60,
	"quote": "USDT",
	"results": {
		"2023-02-12T22:56:17Z": 159.72736850859434,
		"2023-02-12T23:56:17Z": 159.35432528130482,
		"2023-02-13T00:56:17Z": 160.28824321922957,
		"2023-02-13T01:56:17Z": 159.96987373151427,
		"2023-02-13T02:56:17Z": 161.5738270603009,
		"2023-02-13T03:56:17Z": 161.62273587408225,
		"2023-02-13T04:56:17Z": 161.2508164783178,
		"2023-02-13T05:56:17Z": 161.01000401092526,
		"2023-02-13T06:56:17Z": 160.00469110273278,
		"2023-02-13T07:56:17Z": 160.81826861947016,
		"2023-02-13T08:56:17Z": 160.24286014783567,
		"2023-02-13T09:56:17Z": 159.23920126182335,
		"2023-02-13T10:56:17Z": 159.79736352134424,
		"2023-02-13T11:56:17Z": 160.77708802585397,
		"2023-02-13T12:56:17Z": 159.0152030436119,
		"2023-02-13T13:56:17Z": 159.89804147498023,
		"2023-02-13T14:56:17Z": 158.48865706035042,
		"2023-02-13T15:56:17Z": 156.2463930714004,
		"2023-02-13T16:56:17Z": 155.3362341529936,
		"2023-02-13T17:56:17Z": 154.6550613636999,
		"2023-02-13T18:56:17Z": 154.98719323309012,
		"2023-02-13T19:56:17Z": 155.4492368723453,
		"2023-02-13T20:56:17Z": 155.23562502275396,
		"2023-02-13T21:56:17Z": 154.99967347482527
	},
	"timestamp": "2023-02-13T21:57:47Z"
}
```

