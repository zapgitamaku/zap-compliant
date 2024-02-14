# Fetch Bank Details by UserId\*

### GET /v1/bankdetails/users/:userId <a href="#top" id="top"></a>

Allows a User to get Bank details by userId on the platform.

#### HTTP Method <a href="#top" id="top"></a>

GET

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to fetch a bank by Id.

#### **Sample request** URL <a href="#top" id="top"></a>

```
https://{hostname}/v1/bankdetails/users/:userId
```

#### &#x20;**Sample request headers** <a href="#top" id="top"></a>

```
'Content-Type: application/json'
'Authorization: Bearer  <Bearer Token>'
```

## Request Header <a href="#samplerequest" id="samplerequest"></a>

| Header        | Description                                                                                                   |
| ------------- | ------------------------------------------------------------------------------------------------------------- |
| Content-type  | application/json                                                                                              |
| Authorization | This is the ZAP API Platform authorization token, and must be sent with every API request that requires login |

## Request Params <a href="#samplerequest" id="samplerequest"></a>

| Key | Value  | Description                                |
| --- | ------ | ------------------------------------------ |
| Id  | \<Id>  | The unique ID for a specific bank detail.  |

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200, with information about the new bank.

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
        "bankDetailsData": [
            {
            "bankId": "63f6282458e5240a054b4d4b",
            "userId": "63e0f4da81979dcc3b9ee123",
            "accountNumber": "9109417147",
            "accountName": "Aderonke Saudat"
            "createdAt": "2023-02-22T15:05:59.274Z",
            "updatedAt": "2023-02-22T15:05:59.274Z",
            "id": "63f62f576948a75e61839cb0"
            }
        ],
        "bodyLimit": 10,
        "pageLimit": 1,
        "dataCount": 1,
    }
}
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name        | Type                | Description                                                          |
| ----------- | ------------------- | -------------------------------------------------------------------- |
| BankDetails | Bank Details Object | Contains information about the User's bank details on ZAP  platform. |

#### Bank Details Object

Contains information about ZAP's platform bank details.

This object is used by the following operations:

* #### PUT  /v1/bank/:id
* #### GET  /v1/bank/:id
* #### GET  /v1/bank/
* #### POST /v1/bank

The properties included in the **BankDetails** object are listed below.

<table><thead><tr><th width="190.33333333333331">Property</th><th width="333">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td>String</td><td>The unique ID for a specific bank detail. Used in response message.</td></tr><tr><td>bankId</td><td>String</td><td>The unique ID for a specific bank. </td></tr><tr><td>userId</td><td>String</td><td>The unique ID for a specific user. </td></tr><tr><td>accountNumber</td><td>String</td><td>The user's bank account Number.</td></tr><tr><td>accountName</td><td>String</td><td>The bank account name associated with the account number. (optional)</td></tr><tr><td>bvn</td><td>String</td><td>The Bank Verification Number associated with the bank account</td></tr><tr><td>createdAt</td><td>dateTime</td><td>This property displays when the bank detail was created. Used only in response messages.</td></tr><tr><td>updatedAt</td><td>dateTime</td><td>This property displays when the bank detail was last updated. Used only in response messages.</td></tr></tbody></table>

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                   |
| ---- | --------------------------------------- |
| 404  | The resource could not be found.        |
| 500  | An error occured processing the request |

