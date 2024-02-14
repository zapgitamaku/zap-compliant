# Edit Bank by Id

### PUT /v1/banks/:Id <a href="#top" id="top"></a>

Allows the Site Admin to modify an existing Bank on the platform.

#### HTTP Method <a href="#top" id="top"></a>

PUT

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to modify a bank.

#### **Sample request** URL <a href="#top" id="top"></a>

```json
https://{hostname}/v1/banks/:id
```

#### &#x20;**Sample request headers** <a href="#top" id="top"></a>

```
'Content-Type: application/json'
'Authorization: Bearer  <Bearer Token>'
```

#### &#x20;**Sample request body** <a href="#top" id="top"></a>

```json
{
      "name": "Test bank",
      "sortCode": 1,
      "brassId": "testBrassIDzap"
}
```

## Request Header <a href="#samplerequest" id="samplerequest"></a>

| Header        | Description                                                                                                   |
| ------------- | ------------------------------------------------------------------------------------------------------------- |
| Content-type  | application/json                                                                                              |
| Authorization | This is the ZAP API Platform authorization token, and must be sent with every API request that requires login |

## Request Body <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="237">Parameter</th><th>Parm Type</th><th>Data Type</th><th>Required</th><th>Description</th></tr></thead><tbody><tr><td>Bank</td><td>Body</td><td>Bank</td><td>Required</td><td>Contains information about  supported banks on ZAP platform name, shortName and sortCode are required.</td></tr></tbody></table>

#### Bank Object

Contains information about ZAP's platform bank.

This object is used by the following operations:

* #### POST /api/v1/banks

The properties included in the **Bank** object are listed below.

| Property  | Type     | Description                                                                            |
| --------- | -------- | -------------------------------------------------------------------------------------- |
| id        | string   | The unique ID for a specific user.                                                     |
| name      | string   | The name of the bank.                                                                  |
| shortName | string   | The case-sensitive unique shortName of the bank .                                      |
| sortCode  | string   | The bank sort code.                                                                    |
| brassId   | string   | The bank's unique brass Id                                                             |
| createdAt | dateTime | This property displays when the bank was created. Used only in response messages.      |
| updatedAt | dateTime | This property displays when the bank was last updated. Used only in response messages. |

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
    "name": "ZAP bank",
    "shortName": "ZAP",
    "sortCode": 1,
    "icon": "https://iconurl.com/hostedhere",
    "brassId": "testBrassIDzap",
    "createdAt": "2023-01-26T01:38:28.848Z",
    "updatedAt": "2023-01-26T01:38:28.848Z",
    "id": "63d1d994256a94a2f832a08f"
  }
}
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name | Type | Description                                                   |
| ---- | ---- | ------------------------------------------------------------- |
| Bank | Bank | Contains information about  supported banks on ZAP  platform. |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 500  | An error occured processing the request                                                                                                                                                                                                                                                                                           |

