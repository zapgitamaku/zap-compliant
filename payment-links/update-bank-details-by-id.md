# Update Bank Details By Id

### PUT /v1/product/:id <a href="#top" id="top"></a>

Allows only the Site Admin to update business bank details by id on the platform.

#### HTTP Method <a href="#top" id="top"></a>

PUT

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to update a business bank details.

#### **Sample request** URL <a href="#top" id="top"></a>

```json
https://{hostname}/v1/product/:id
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
    "bankId":"64afd58f177653c33d9a4228"
}
```

## Request Header <a href="#samplerequest" id="samplerequest"></a>

| Header        | Description                                                                                                             |
| ------------- | ----------------------------------------------------------------------------------------------------------------------- |
| Content-type  | application/json                                                                                                        |
| Authorization | This is the ZAP Business API Platform authorization token, and must be sent with every API request that requires login. |

## Request Parameters <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="99">Parameter</th><th width="91">Parm Type</th><th width="75">Data Type</th><th width="101">Required</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td>Params</td><td>String</td><td>Required</td><td>unique product id</td></tr></tbody></table>

## Request Body <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="122">Parameter</th><th width="73">Param Type</th><th width="86">Data Type</th><th width="100">Required</th><th>Description</th></tr></thead><tbody><tr><td>Bank details</td><td>Body</td><td>Object</td><td>Required</td><td>Contains information about ZAP platform business owner. businessId, and bankId are required while accountName, and accountNumber .are optional.</td></tr></tbody></table>

#### Business Product

Contains information about ZAP's business bank details.

The properties included in the B**ank details** object are listed below. All properties are **required** in the request message.

| Property      | Type   | Description                         |
| ------------- | ------ | ----------------------------------- |
| businessId    | string | The unique id of the business user. |
| accountName   | string | The user's account  name            |
| accountNumber | string | The user's account number.          |
| bankId        | string | The unique bank id.                 |

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200, with information about the newly created business bank details.

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
            "name": "JOHN DOE",
            "sortCode": "123456",
            "id": "64afd58f177653c33d9a4228"
        },
        "businessId": {
            "businessName": "JOHN DOE ltd.",
            "id": "65eef259501d4e3cbc2cff1d"
        },
        "accountNumber": "1234567899",
        "accountName": "JOHN DOE DON",
        "primaryAccount": true,
        "createdAt": "2024-03-11T13:40:56.889Z",
        "updatedAt": "2024-03-12T09:43:06.971Z",
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
