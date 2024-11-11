# Add Wallet Details

### POST /v1/walletDetails <a href="#top" id="top"></a>

Allows a User to add a new Wallet detail to the platform.

#### HTTP Method <a href="#top" id="top"></a>

POST

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to add a wallet detail.

#### **Sample request** URL <a href="#top" id="top"></a>

```json
https://{hostname}/v1/walletDetails
```

#### **Sample request headers** <a href="#top" id="top"></a>

```
'Content-Type: application/json'
'Authorization: Bearer  <Bearer Token>'
```

#### **Sample request body** <a href="#top" id="top"></a>

```json
{
      "address": "0x483293A1Dc64A7589C994e633a03e66AE52DD130",
      "name": "Zap Africa",
      "chainId": "1",
      "userId": "63d02e0bc8c116c1308d39fe",
}
```

## Request Header <a href="#samplerequest" id="samplerequest"></a>

| Header        | Description                                                                                                   |
| ------------- | ------------------------------------------------------------------------------------------------------------- |
| Content-type  | application/json                                                                                              |
| Authorization | This is the ZAP API Platform authorization token, and must be sent with every API request that requires login |

## Request Body <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="237">Parameter</th><th>Parm Type</th><th>Data Type</th><th>Required</th><th>Description</th></tr></thead><tbody><tr><td>WalletDetail</td><td>Body</td><td>walletDetail</td><td>Required</td><td>Contains information about a users wallet details on ZAP platform name, address are required.</td></tr></tbody></table>

#### walletDetails Object

Contains information about ZAP's platform wallet.

This object is used by the following operations:

* **POST /v1/walletDetails**
* **GET /v1/walletDetails/:id**
* **GET /v1/walletDetails**
* **DELETE /v1/walletDetails/:id**
* **PUT /v1/walletDetails/:id**

The properties included in the **WalletDetails** object are listed below.

<table><thead><tr><th width="190.33333333333331">Property</th><th width="333">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td>String</td><td>The unique ID for a specific wallet detail. Used in response message.</td></tr><tr><td>chainId</td><td>String</td><td>The ID for a specific chain.</td></tr><tr><td>userId</td><td>String</td><td>The unique ID for a specific user.</td></tr><tr><td>name</td><td>String</td><td>The name of the wallet.</td></tr><tr><td>address</td><td>String</td><td>The public address of the wallet</td></tr><tr><td>isDeleted</td><td>Boolean</td><td>A flag indicating whether the wallet has been deleted.</td></tr><tr><td>deletedAt</td><td>dateTime</td><td>The timestamp when the wallet was marked as deleted.</td></tr><tr><td>createdAt</td><td>dateTime</td><td>This property displays when the wallet detail was created. Used only in response messages.</td></tr><tr><td>updatedAt</td><td>dateTime</td><td>This property displays when the wallet detail was last updated. Used only in response messages.</td></tr></tbody></table>

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 201, with information about the new wallet.

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
        "chainId": "1",
        "userId": "63d4f7a03a678d014c3c4996",
        "address": "0x483293A1Dc64A7589C994e633a03e66AE52DD130",
        "name": "Zap Africa",
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

| Name         | Type         | Description                                                                                   |
| ------------ | ------------ | --------------------------------------------------------------------------------------------- |
| WalletDetail | walletDetail | Contains information about a users wallet details on ZAP platform name, address are required. |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 500  | An error occured processing the request                                                                                                                                                                                                                                                                                           |
