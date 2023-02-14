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

## Requesting a spot crypto/fiat quote

Example using XMR and USD:

> https://fiat-api.cakewallet.com/v2/rates?interval_count=1&base=XMR&quote=USD

Response:

```
{
	"base":"XMR",
	"errors":{},
	"interval_count":1,
	"interval_minutes":60,
	"quote":"USD",
	"results":{
		"2023-02-14T16:00:06Z":158.49
	},
	"timestamp":"2023-02-14T16:01:36Z"
}
```

## Requesting a spot crypto/crypto fiat quote

Example using XMR and BTC:

> https://fiat-api.cakewallet.com/v2/rates?interval_count=1&base=XMR&quote=BTC

Response:

```
{
	"base":"XMR",
	"errors":{},
	"interval_count":1,
	"interval_minutes":60,
	"quote":"BTC",
	"results":{
		"2023-02-14T16:06:36Z":0.007182635424822883
	},
	"timestamp":"2023-02-14T16:08:06Z"
}
```

## Getting daily pricing for the last 30 days

Example using BTC and JPY:

> https://fiat-api.cakewallet.com/v2/rates?interval_minutes=1440&interval_count=30&base=BTC&quote=JPY

Response:

```
{
	"base":"BTC",
	"errors":{},
	"interval_count":30,
	"interval_minutes":1440,
	"quote":"JPY",
	"results":{
		"2023-01-16T16:13:44Z":2949930,
		"2023-01-17T16:13:44Z":2949930,
		"2023-01-18T16:13:44Z":2949930,
		"2023-01-19T16:13:44Z":2949930,
		"2023-01-20T16:13:44Z":2949930,
		"2023-01-21T16:13:44Z":2999784.5,
		"2023-01-22T16:13:44Z":2950202.5,
		"2023-01-23T16:13:44Z":2992359,
		"2023-01-24T16:13:44Z":2977552,
		"2023-01-25T16:13:44Z":2937814.5,
		"2023-01-26T16:13:44Z":2995734.5,
		"2023-01-27T16:13:44Z":2991849,
		"2023-01-28T16:13:44Z":2993742,
		"2023-01-29T16:13:44Z":3058439,
		"2023-01-30T16:13:44Z":3028999,
		"2023-01-31T16:13:44Z":3012731,
		"2023-02-01T16:13:44Z":2978868.5,
		"2023-02-02T16:13:44Z":3056331,
		"2023-02-03T16:13:44Z":3098853,
		"2023-02-04T16:13:44Z":3073615,
		"2023-02-05T16:13:44Z":3029889.5,
		"2023-02-06T16:13:44Z":3060673,
		"2023-02-07T16:13:44Z":3007616.5,
		"2023-02-08T16:13:44Z":2997724.5,
		"2023-02-09T16:13:44Z":2959453,
		"2023-02-10T16:13:44Z":2849967,
		"2023-02-11T16:13:44Z":2856813,
		"2023-02-12T16:13:44Z":2887219.5,
		"2023-02-13T16:13:44Z":2877421,
		"2023-02-14T16:13:44Z":2929963
	},
	"timestamp":"2023-02-14T16:15:14Z"
}
```
