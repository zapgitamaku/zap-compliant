# Edit Bank Details By Id

### PUT /v1/bankdetails/:id <a href="#top" id="top"></a>

Allows the Regular user to modify an existing own bank details on the platform.

#### HTTP Method <a href="#top" id="top"></a>

PUT

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to modify a specified bank detail object.

#### **Sample request** URL <a href="#top" id="top"></a>

```json
https://{hostname}/v1/bankdetails/:id
```

#### **Sample request headers** <a href="#top" id="top"></a>

```javascript
'Content-Type: application/json'
```

#### **Sample** Request Body <a href="#top" id="top"></a>

```json
{
      "accountNumber": "0987654321",
      "bankId": "63f6282458e5240a054b4d4b",
      "userId": "63fcedad5ab92b52bfbf5125"
}
```

## Request Header <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="241">Header</th><th>Description</th></tr></thead><tbody><tr><td>Content-type</td><td>application/json</td></tr><tr><td>Authorization</td><td>This is the ZAP API Platform authorization token, and must be sent with every API request that requires login</td></tr></tbody></table>

*

## Request Body <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="150">Parameter</th><th width="162">Param Type</th><th>Data Type</th><th>Required</th><th>Description</th></tr></thead><tbody><tr><td>BankDetails</td><td>Body</td><td>Object</td><td>Required</td><td>Contains information about ZAP platform bank details. Account Number, Bank Id, User Id, BVN.</td></tr></tbody></table>

#### BankDetails Object

Contains updated information about the particular ZAP platform bank Details.

This object is returned by the following operations:

* #### PUT /api/v1/bankDetails/:id





<table><thead><tr><th width="190.33333333333331">Property</th><th width="333">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td>String</td><td>The unique ID for a specific bank detail. Used in response message.</td></tr><tr><td>bankId</td><td>String</td><td>The unique ID for a specific bank. </td></tr><tr><td>userId</td><td>String</td><td>The unique ID for a specific user. </td></tr><tr><td>accountNumber</td><td>String</td><td>The user's bank account Number.</td></tr><tr><td>accountName</td><td>String</td><td>The bank account name associated with the account number. (optional)</td></tr><tr><td>bvn</td><td>String</td><td>The Bank Verification Number associated with the bank account</td></tr><tr><td>createdAt</td><td>dateTime</td><td>This property displays when the bank detail was created. Used only in response messages.</td></tr><tr><td>updatedAt</td><td>dateTime</td><td>This property displays when the bank detail was last updated. Used only in response messages.</td></tr></tbody></table>

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200, with an updated user details.

If the request body contains email, the operation returns a HTTP status code 200, and an otp is generated and sent to the new email. emailVerified is set to false, returns updated user details

### Sample Response <a href="#samplerequest" id="samplerequest"></a>

The sample responses below shows successful completion of this operation.

#### **Sample** Response Header <a href="#top" id="top"></a>

```
HTTP/1.1 200 OK
Date: Wed, 25 Jan 2023 23:14:31 GMT
Content-Type: application/json; charset=utf-8
```

#### **Sample** Response Body <a href="#top" id="top"></a>

```json
{
    "success": true,
    "data": {
        "bankId": "63fdf9229c58e23ee6f80de1",
        "userId": "63fcedad5ab92b52bfbf5125",
        "accountNumber": "9109417147",
        "createdAt": "2023-03-01T20:51:13.425Z",
        "updatedAt": "2023-03-01T20:51:13.425Z",
        "id": "63ffbac161aace822a4cc962"
    }
}
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name              | Type   | Description                                                              |
| ----------------- | ------ | ------------------------------------------------------------------------ |
| Bank Details Data | Object | Contains information about the user's updated ZAP platform bank details. |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 500  | An error occured while processing the request                                                                                                                                                                                                                                                                                     |

