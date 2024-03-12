# Create Business Bank Details

### POST /v1/product <a href="#top" id="top"></a>

Allows the Site Admin to add business bank details to the platform.

#### HTTP Method <a href="#top" id="top"></a>

POST

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to add a new business bank details.

#### **Sample request** URL <a href="#top" id="top"></a>

```json
https://{hostname}/v1/bankdetails
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
    "accountNumber":"1234567890",
    "accountName":"JOHN DOE ANONYMOUS",
    "bankId":"64afd58f177653c33d9a4220"
}
```

## Request Header <a href="#samplerequest" id="samplerequest"></a>

| Header        | Description                                                                                                             |
| ------------- | ----------------------------------------------------------------------------------------------------------------------- |
| Content-type  | application/json                                                                                                        |
| Authorization | This is the ZAP Business API Platform authorization token, and must be sent with every API request that requires login. |

## Request Body <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="122">Parameter</th><th width="73">Param Type</th><th width="86">Data Type</th><th width="100">Required</th><th>Description</th></tr></thead><tbody><tr><td>BankDetails</td><td>Body</td><td>Object</td><td>Required</td><td>Contains information about ZAP platform business owner. businessId, accountName, accountNumber, bankId are required.</td></tr></tbody></table>

#### Business Product

Contains information about ZAP's business user's bank details.

The properties included in the **BankDetails** object are listed below. All properties are **required** in the request message.

| Property      | Type   | Description                           |
| ------------- | ------ | ------------------------------------- |
| businessId    | string | The unique id of the business user.   |
| accountName   | string | The business user's account  name     |
| accountNumber | string | The  business user's account  number. |
| bankId        | number | The bank id.                          |

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 201, with information about the newly created business product.

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
        "primaryAccount": false,
        "createdAt": "2024-03-11T13:40:56.889Z",
        "updatedAt": "2024-03-11T13:40:56.889Z",
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
