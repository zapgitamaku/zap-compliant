# Fetch Business Order Stats

### GET /v1/order/stats/:businessId <a href="#top" id="top"></a>

Allows the Site Admin to get the business user related stats on the first dashboard analytics card on the platform.

#### HTTP Method <a href="#top" id="top"></a>

GET

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to fetch a business user stats.

#### **Sample request** URL <a href="#top" id="top"></a>

```json
https://{hostname}/v1/order/stats/:businessId
```

### **Sample request headers** <a href="#top" id="top"></a>

```
'Content-Type: application/json'
'Authorization: Bearer  <Bearer Token>'
```

## Request Parameter <a href="#samplerequest" id="samplerequest"></a>

| Paramater  | Description                    |
| ---------- | ------------------------------ |
| businessId | The unique id of the business. |

## Request Header <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="182">Header</th><th>Description</th></tr></thead><tbody><tr><td>Content-type</td><td>application/json</td></tr><tr><td>Authorization</td><td>This is the ZAP Business API Platform authorization token, and must be sent with every API request that requires login.</td></tr></tbody></table>

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200, with stats.

### Sample Response <a href="#samplerequest" id="samplerequest"></a>

The sample responses below shows successful completion of this operation.

#### **Sample** Response Header <a href="#top" id="top"></a>

```
HTTP/1.1 200 OK
Date: Wed, 09 Feb 2024 23:14:31 GMT
Content-Type: application/json; charset=utf-8
```

#### **Sample** Response Body <a href="#top" id="top"></a>

```json
{
    "success": true,
    "data": {
        "revenueStats": {
            "daily": {
                "count": 14082.964359416668,
                "percent": "1408296.44%"
            },
            "weekly": {
                "count": 14082.964359416668,
                "percent": "1408296.44%"
            },
            "monthly": {
                "count": 14082.964359416668,
                "percent": "1408296.44%"
            },
            "yearly": {
                "count": 14082.964359416668,
                "percent": "1408296.44%"
            },
            "allTime": 14082.964359416668
        },
        "transactionStats": {
            "daily": {
                "count": 1,
                "percent": "100.00%"
            },
            "weekly": {
                "count": 1,
                "percent": "100.00%"
            },
            "monthly": {
                "count": 1,
                "percent": "100.00%"
            },
            "yearly": {
                "count": 1,
                "percent": "100.00%"
            },
            "allTime": 1
        },
        "mostReceived": {
            "dailyMostReceivedCrypto": [
                {
                    "totalAmount": 14082.964359416668,
                    "baseCurrency": {
                        "_id": "646369e1e3707ef59b49abe6",
                        "name": "Binance-Tether",
                        "ticker": "USDTBSC",
                        "contract": "0x55d398326f99059ff775485246999027b3197955",
                        "chainId": "56",
                        "isCrypto": true,
                        "icon": "https://res.cloudinary.com/dclh3qo14/image/upload/v1688389863/svg/1688389865907.svg",
                        "createdAt": "2023-05-16T11:32:49.295Z",
                        "updatedAt": "2024-01-04T13:04:20.604Z",
                        "__v": 0,
                        "chainIcon": "https://res.cloudinary.com/dukdbbrbc/image/upload/v1684235730/image/bnb.svg",
                        "network": "BSC"
                    },
                    "marketId": "64c13d0ec5efabf7529bfa79"
                }
            ],
            "weeklyMostReceivedCrypto": [
                {
                    "totalAmount": 14082.964359416668,
                    "baseCurrency": {
                        "_id": "646369e1e3707ef59b49abe6",
                        "name": "Binance-Tether",
                        "ticker": "USDTBSC",
                        "contract": "0x55d398326f99059ff775485246999027b3197955",
                        "chainId": "56",
                        "isCrypto": true,
                        "icon": "https://res.cloudinary.com/dclh3qo14/image/upload/v1688389863/svg/1688389865907.svg",
                        "createdAt": "2023-05-16T11:32:49.295Z",
                        "updatedAt": "2024-01-04T13:04:20.604Z",
                        "__v": 0,
                        "chainIcon": "https://res.cloudinary.com/dukdbbrbc/image/upload/v1684235730/image/bnb.svg",
                        "network": "BSC"
                    },
                    "marketId": "64c13d0ec5efabf7529bfa79"
                }
            ],
            "monthlyMostReceivedCrypto": [
                {
                    "totalAmount": 14082.964359416668,
                    "baseCurrency": {
                        "_id": "646369e1e3707ef59b49abe6",
                        "name": "Binance-Tether",
                        "ticker": "USDTBSC",
                        "contract": "0x55d398326f99059ff775485246999027b3197955",
                        "chainId": "56",
                        "isCrypto": true,
                        "icon": "https://res.cloudinary.com/dclh3qo14/image/upload/v1688389863/svg/1688389865907.svg",
                        "createdAt": "2023-05-16T11:32:49.295Z",
                        "updatedAt": "2024-01-04T13:04:20.604Z",
                        "__v": 0,
                        "chainIcon": "https://res.cloudinary.com/dukdbbrbc/image/upload/v1684235730/image/bnb.svg",
                        "network": "BSC"
                    },
                    "marketId": "64c13d0ec5efabf7529bfa79"
                }
            ],
            "yearlyMostReceivedCrypto": [
                {
                    "totalAmount": 14082.964359416668,
                    "baseCurrency": {
                        "_id": "646369e1e3707ef59b49abe6",
                        "name": "Binance-Tether",
                        "ticker": "USDTBSC",
                        "contract": "0x55d398326f99059ff775485246999027b3197955",
                        "chainId": "56",
                        "isCrypto": true,
                        "icon": "https://res.cloudinary.com/dclh3qo14/image/upload/v1688389863/svg/1688389865907.svg",
                        "createdAt": "2023-05-16T11:32:49.295Z",
                        "updatedAt": "2024-01-04T13:04:20.604Z",
                        "__v": 0,
                        "chainIcon": "https://res.cloudinary.com/dukdbbrbc/image/upload/v1684235730/image/bnb.svg",
                        "network": "BSC"
                    },
                    "marketId": "64c13d0ec5efabf7529bfa79"
                }
            ],
            "allTimeMostReceivedCrypto": [
                {
                    "totalAmount": 14082.964359416668,
                    "baseCurrency": {
                        "_id": "646369e1e3707ef59b49abe6",
                        "name": "Binance-Tether",
                        "ticker": "USDTBSC",
                        "contract": "0x55d398326f99059ff775485246999027b3197955",
                        "chainId": "56",
                        "isCrypto": true,
                        "icon": "https://res.cloudinary.com/dclh3qo14/image/upload/v1688389863/svg/1688389865907.svg",
                        "createdAt": "2023-05-16T11:32:49.295Z",
                        "updatedAt": "2024-01-04T13:04:20.604Z",
                        "__v": 0,
                        "chainIcon": "https://res.cloudinary.com/dukdbbrbc/image/upload/v1684235730/image/bnb.svg",
                        "network": "BSC"
                    },
                    "marketId": "64c13d0ec5efabf7529bfa79"
                }
            ]
        },
        "customerStats": {
            "daily": {
                "count": 0,
                "percent": "N/A"
            },
            "weekly": {
                "count": 0,
                "percent": "N/A"
            },
            "monthly": {
                "count": 0,
                "percent": "N/A"
            },
            "yearly": {
                "count": 0,
                "percent": "N/A"
            },
            "allTime": 0
        }
    }
}
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name  | Type   | Description                       |
| ----- | ------ | --------------------------------- |
| Stats | Object | Contains the business user stats. |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 500  | An error occured while processing the request                                                                                                                                                                                                                                                                                     |
