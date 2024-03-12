# Update Payment Status By Id

### PUT /v1/payment/:id <a href="#top" id="top"></a>

Allows only the Site Admin to update payment status by id on the platform.

#### HTTP Method <a href="#top" id="top"></a>

PUT

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to update a business payment.

#### **Sample request** URL <a href="#top" id="top"></a>

```json
https://{hostname}/v1/payment/status/:id
```

### **Sample request headers** <a href="#top" id="top"></a>

```
'Content-Type: multipart/form-data'
'Authorization: Bearer  <Bearer Token>'
```

#### **Sample request body** <a href="#top" id="top"></a>

```json
{
    "active" : false
}
```

## Request Header <a href="#samplerequest" id="samplerequest"></a>

| Header        | Description                                                                                                             |
| ------------- | ----------------------------------------------------------------------------------------------------------------------- |
| Content-type  | application/json                                                                                                        |
| Authorization | This is the ZAP Business API Platform authorization token, and must be sent with every API request that requires login. |

## Request Parameters <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="99">Parameter</th><th width="91">Parm Type</th><th width="75">Data Type</th><th width="101">Required</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td>Params</td><td></td><td>Required</td><td>unique product id</td></tr></tbody></table>

## Request Body <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="122">Parameter</th><th width="73">Param Type</th><th width="86">Data Type</th><th width="100">Required</th><th>Description</th></tr></thead><tbody><tr><td>Payment</td><td>Body</td><td>Object</td><td>Required</td><td>Contains information about ZAP platform payment. active, is required..</td></tr></tbody></table>

#### Business Product

Contains information about ZAP's  payment.

The properties included in the **Payment** object are listed below. All properties are **required** in the request message.

| Property | Type    | Description         |
| -------- | ------- | ------------------- |
| active   | boolean | The payment status. |

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200, with information about the newly created Payment.

### Sample Response <a href="#samplerequest" id="samplerequest"></a>

The sample responses below shows successful completion of this operation.

#### **Sample** Response Header <a href="#top" id="top"></a>

```
HTTP/1.1 201 OK
Date: Wed, 08 Feb 2024 13:14:31 GMT
Content-Type: application/json; charset=utf-8
```

#### **Sample** Response Body <a href="#top" id="top"></a>

```
{
    "success": true,
    "data": {
        "businessId": "65eef259501d4e3cbc2cff1d",
        "productId": [
            "65f0283b76a7659c692808ec",
            "65f027d28ad58339210ce254",
            "65f0281ab34eff81de0cd16c"
        ],
        "settlementBankDetails": "65ef09e8e3c4c66cdc380afd",
        "description": "test payment",
        "paymentType": "oneTime",
        "paymentLink": "https://pay.business.zap.africa/eapq1k36ku",
        "paymentToken": "eapq1k36ku",
        "customerId": [],
        "amount": 927,
        "deliverReceipt": true,
        "isApi": false,
        "status": "inactive",
        "isDeleted": false,
        "createdAt": "2024-03-12T10:09:49.339Z",
        "updatedAt": "2024-03-12T11:52:14.009Z",
        "id": "65f029ed76a7659c692808f8"
    }
}
```

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 500  | An error occured processing the request                                                                                                                                                                                                                                                                                           |
