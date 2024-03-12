# Update Bank Details to primary

### PUT /v1/bankDetails/primary <a href="#top" id="top"></a>

Allows only the Site Admin to update business user bank details on the platform.

#### HTTP Method <a href="#top" id="top"></a>

PUT

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to update a business user bank details.

#### **Sample request** URL <a href="#top" id="top"></a>

```json
https://{hostname}/v1/bankdetails/primary
```

### **Sample request headers** <a href="#top" id="top"></a>

```
'Content-Type: multipart/form-data'
'Authorization: Bearer  <Bearer Token>'
```

#### **Sample request body** <a href="#top" id="top"></a>

```json
{
    "businessId":"65eef259501d4e3cbc2cff1d",
    "bankDetailsId":"65ef09e8e3c4c66cdc380afd",
    "currentPrimaryDetailsId":"65eef614cf9c648ad9b69ba0"
}
```

## Request Header <a href="#samplerequest" id="samplerequest"></a>

| Header        | Description                                                                                                             |
| ------------- | ----------------------------------------------------------------------------------------------------------------------- |
| Content-type  | application/json                                                                                                        |
| Authorization | This is the ZAP Business API Platform authorization token, and must be sent with every API request that requires login. |

## Request Body <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="122">Parameter</th><th width="73">Param Type</th><th width="86">Data Type</th><th width="100">Required</th><th>Description</th></tr></thead><tbody><tr><td>Product</td><td>Body</td><td>Object</td><td>Required</td><td>Contains information about ZAP platform business owner. businessId, currentPrimaryDetailsId, and bankDetailsId are required.</td></tr></tbody></table>

#### Business Product

Contains information about ZAP's business user 'sbank details.

The properties included in the user 's bank details object are listed below. All properties are **required** in the request message.

| Property                | Type   | Description                                   |
| ----------------------- | ------ | --------------------------------------------- |
| businessId              | string | The unique id of the business user.           |
| currentPrimaryDetailsId | string | The unique id of the current primary details. |
| bankDetailsId           | string | The unique id of the new primary details.     |

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200, with information about the newly created business product.

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
        "bankId": {
            "name": "9 PAYMENT SOLUTIONS BANK",
            "sortCode": "123456",
            "icon": "https://res.cloudinary.com/name/image/upload/v1683654423/image/1683654422041.png",
            "id": "64afd58f177653c33d9a4221"
        },
        "businessId": {
            "businessName": "John Ltd.",
            "id": "65eef259501d4e3cbc2cff1d"
        },
        "accountNumber": "1234567890",
        "accountName": "JOHN DOE ANONYMOUS",
        "primaryAccount": true,
        "createdAt": "2024-03-11T13:40:56.889Z",
        "updatedAt": "2024-03-11T14:56:37.399Z",
        "id": "65ef09e8e3c4c66cdc380afd"
    }
}
```

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 500  | An error occured processing the request                                                                                                                                                                                                                                                                                           |
