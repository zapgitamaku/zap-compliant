# Add Bank

### POST /v1/banks <a href="#top" id="top"></a>

Allows the Site Admin to add a new Bank to the platform.

#### HTTP Method <a href="#top" id="top"></a>

POST

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to add a bank.

#### **Sample request** URL <a href="#top" id="top"></a>

```json
https://{hostname}/v1/banks
```

#### &#x20;**Sample request headers** <a href="#top" id="top"></a>

```
'Content-Type: application/json'
'Authorization: Bearer  <Bearer Token>'
```

#### &#x20;**Sample request body** <a href="#top" id="top"></a>

```json
{
      "name": "Private Racks bank",
      "sortCode": 147174,
}
```

## Request Header <a href="#samplerequest" id="samplerequest"></a>

| Header        | Description                                                                                                   |
| ------------- | ------------------------------------------------------------------------------------------------------------- |
| Content-type  | application/json                                                                                              |
| Authorization | This is the ZAP API Platform authorization token, and must be sent with every API request that requires login |

## Request Body <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="237">Parameter</th><th>Parm Type</th><th>Data Type</th><th>Required</th><th>Description</th></tr></thead><tbody><tr><td>Bank</td><td>Body</td><td>Bank</td><td>Required</td><td>Contains information about  supported banks on ZAP platform name, shortName, sortCode and BrassId are required.</td></tr></tbody></table>

#### Bank Object

Contains information about ZAP's platform bank.

This object is used by the following operations:

* #### POST /v1/banks
* #### GET  /v1/banks/:id
* #### GET  /v1/banks/
* #### PUT  /v1/banks/:id
* #### DELETE  /v1/banks/:id

The properties included in the **Bank** object are listed below.

| Property  | Type   | Description                                      |
| --------- | ------ | ------------------------------------------------ |
| id        | string | The unique ID for a specific bank.               |
| name      | string | The name of the bank.                            |
| shortName | string | The unique case-sensitive shortName of the bank. |
| sortCode  | string | The bank's sort code.                            |
| brassId   | string | The unique Brass bank id                         |

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 201, with information about the newly added bank.

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
    "success": true,
    "data": {
        "name": "Private Racks bank",
        "shortName": "PRB",
        "sortCode": 147174,
        "icon": "https://iconurl.com/hostedhere",
        "brassId": "privateBrassId",
        "createdAt": "2023-02-28T12:52:50.345Z",
        "updatedAt": "2023-02-28T12:52:50.345Z",
        "id": "63fdf9229c58e23ee6f80de1"
    }
}
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description                     |
| ------------ | ------------------------------- |
| Content-Type | application/json; charset=utf-8 |

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

