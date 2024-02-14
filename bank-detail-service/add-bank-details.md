# Add Bank Details

### POST /v1/bankdetails <a href="#top" id="top"></a>

Allows a User to add a new Bank detail to the platform.

#### HTTP Method <a href="#top" id="top"></a>

POST

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to add a bank detail.

#### **Sample request** URL <a href="#top" id="top"></a>

```json
https://{hostname}/v1/bankdetails
```

#### &#x20;**Sample request headers** <a href="#top" id="top"></a>

```
'Content-Type: application/json'
'Authorization: Bearer  <Bearer Token>'
```

#### &#x20;**Sample request body** <a href="#top" id="top"></a>

```json
{
      "accountNumber": "1234567890",
      "accountName": "Zap Africa"
      "bankId": "63d1d994256a94a2f832a08f",
      "userId": "63d02e0bc8c116c1308d39fe",
}
```

## Request Header <a href="#samplerequest" id="samplerequest"></a>

| Header        | Description                                                                                                   |
| ------------- | ------------------------------------------------------------------------------------------------------------- |
| Content-type  | application/json                                                                                              |
| Authorization | This is the ZAP API Platform authorization token, and must be sent with every API request that requires login |

## Request Body <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="237">Parameter</th><th>Parm Type</th><th>Data Type</th><th>Required</th><th>Description</th></tr></thead><tbody><tr><td>BankDetail</td><td>Body</td><td>bankDetail</td><td>Required</td><td>Contains information about a users bank details on ZAP platform bvn, accountNumber are required.</td></tr></tbody></table>

#### bankDetail Object

Contains information about ZAP's platform bank.

This object is used by the following operations:

* #### POST /v1/bankdetails
* #### GET  /v1/bankdetails/:id
* #### GET  /v1/bankdetails/
* #### DELETE  /v1/bankdetails/:id
* #### PUT  /v1/bankdetails/:id

The properties included in the **BankDetails** object are listed below. All properties are **required**.

<table><thead><tr><th width="190.33333333333331">Property</th><th width="333">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td>String</td><td>The unique ID for a specific bank detail. Used in response message.</td></tr><tr><td>bankId</td><td>String</td><td>The unique ID for a specific bank. </td></tr><tr><td>userId</td><td>String</td><td>The unique ID for a specific user. </td></tr><tr><td>accountNumber</td><td>String</td><td>The user's bank account Number.</td></tr><tr><td>accountName</td><td>String</td><td>The bank account name associated with the account number. (optional)</td></tr><tr><td>bvn</td><td>String</td><td>The Bank Verification Number associated with the bank account</td></tr><tr><td>createdAt</td><td>dateTime</td><td>This property displays when the bank detail was created. Used only in response messages.</td></tr><tr><td>updatedAt</td><td>dateTime</td><td>This property displays when the bank detail was last updated. Used only in response messages.</td></tr></tbody></table>

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 201, with information about the new bank.

### Sample Response <a href="#samplerequest" id="samplerequest"></a>

The sample responses below shows successful completion of this operation.

#### **Sample** Response Header <a href="#top" id="top"></a>

```
HTTP/1.1 201 OK
Date: Wed, 25 Jan 2023 23:14:31 GMT
Content-Type: application/json; charset=utf-8
```

#### **Sample** Response Body <a href="#top" id="top"></a>

```json
{
  success: true,
    data: {
        "bankId": "63d4f7a03a678d014c3c499a",
        "userId": "63d4f7a03a678d014c3c4996",
        "accountNumber": "1234567890",
        "accountName": "Zap Africa",
        "createdAt": "2023-01-28T10:23:29.259Z",
        "updatedAt": "2023-01-28T10:23:29.259Z",
        "id": "63d4f7a13a678d014c3c499f"
  }
}
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name       | Type       | Description                                                                                      |
| ---------- | ---------- | ------------------------------------------------------------------------------------------------ |
| BankDetail | bankDetail | Contains information about a users bank details on ZAP platform bvn, accountNumber are required. |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 500  | An error occured processing the request                                                                                                                                                                                                                                                                                           |

