# Create Affiliate Payout

### POST /v1/affiliate/payout/:id <a href="#top" id="top"></a>

Allows an <mark style="color:red;">**affiliate**</mark> to request payout on the platform.

#### HTTP Method <a href="#top" id="top"></a>

POST

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to create a payout request.

#### **Sample request** URL <a href="#top" id="top"></a>

```
https://{hostname}/v1/affiliate/payout/:id
```

#### &#x20;**Sample request headers** <a href="#top" id="top"></a>

```
'Content-Type: application/json'
'Authorization: Bearer  <Bearer Token>'
```

#### &#x20;**Sample request body** <a href="#top" id="top"></a>

```json
{
    "amount":200,
    "marketId": "64fee956a6accfe5b30d18d2",
    "withdrawalBankAccount": "64afdbf6ca858ec953e3bf0e",
    "userId": "647dea2605647ed1d5193b0a",
    // "withdrawalPublicKey": "",
    "isFiatWithdrawal": true
}
```

## Request Header <a href="#samplerequest" id="samplerequest"></a>

| Header        | Description                                                                                                   |
| ------------- | ------------------------------------------------------------------------------------------------------------- |
| Content-type  | application/json                                                                                              |
| Authorization | This is the ZAP API Platform authorization token, and must be sent with every API request that requires login |

## Request Parameters <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="241">Parameter</th><th width="120">Parm Type</th><th width="99">Data Type</th><th width="103">Required</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td>path</td><td>string</td><td>Required</td><td>The userId of the requester</td></tr><tr><td>userId</td><td>Body</td><td>string</td><td>Required</td><td>the UserId of the requester</td></tr><tr><td>amount</td><td>Body</td><td>number</td><td>Required</td><td>The amount of earnings the user is requesting payout for</td></tr><tr><td>marketId</td><td>Body</td><td>string</td><td>Required</td><td>The marketId of the transaction pair e.g NGN-NGN or NGN-Crypto</td></tr><tr><td>withdrawalBankAccount</td><td>Body</td><td>string</td><td>Optional</td><td>The Id of the bank account the user will be paid into. for NGN-NGN</td></tr><tr><td>withdrawalPublicKey</td><td>Body</td><td>string</td><td>Optional</td><td>The wallet address the user will be paid into, for NGN-Crypto</td></tr><tr><td>isFiatWithdrawal</td><td>Body</td><td>boolean</td><td>required</td><td>if the request is a fiat withdrawal or a crypto withdrawal</td></tr></tbody></table>

#### Payout Object

Contains information about ZAP's platform user payout data.

This object is used by the following operations:

* #### POST /v1/referrer/payout
* #### POST /v1/affiliate/payout

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 201, with information about the payout status.

### Sample Response <a href="#samplerequest" id="samplerequest"></a>

The sample responses below shows successful completion of this operation.

#### **Sample** Response Header <a href="#top" id="top"></a>

```
HTTP/1.1 201 OK
Date: Tue, 28 Feb 2023 02:10:15 GMT
Content-Type: application/json; charset=utf-8
```

#### **Sample** Response Body <a href="#top" id="top"></a>

```json
{
    "success": true,
    "data": "Affiliate payout in fiat successful"
}
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name | Type   | Description                                                                  |
| ---- | ------ | ---------------------------------------------------------------------------- |
| data | string | Contains information about  Status of the payout requested on ZAP  platform. |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 401  | Unauthorized                                                                                                                                                                                                                                                                                                                      |
| 404  | Not Found: Returned if the request                                                                                                                                                                                                                                                                                                |
| 500  | An error occured processing the request                                                                                                                                                                                                                                                                                           |

