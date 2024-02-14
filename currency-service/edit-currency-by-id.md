# Edit Currency by Id

### PUT /v1/currencies/:Id <a href="#top" id="top"></a>

Allows the site admin User to modify a currency by Id on the platform.

#### HTTP Method <a href="#top" id="top"></a>

PUT

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to modify a currency by Id.

#### **Sample request** URL <a href="#top" id="top"></a>

```
https://{hostname}/v1/currencies/:Id
```

#### &#x20;**Sample request headers** <a href="#top" id="top"></a>

```
'Content-Type: application/json'
'Authorization: Bearer  <Bearer Token>'
```

#### &#x20;**Sample request body** <a href="#top" id="top"></a>

```json
{
      "name": "Test Currency",
      "ticker": "TCA"
}
```

## Request Header <a href="#samplerequest" id="samplerequest"></a>

| Header        | Description                                                                                                   |
| ------------- | ------------------------------------------------------------------------------------------------------------- |
| Content-type  | application/json                                                                                              |
| Authorization | This is the ZAP API Platform authorization token, and must be sent with every API request that requires login |

## Request Parameters <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="237">Parameter</th><th>Parm Type</th><th>Data Type</th><th>Required</th><th>Description</th></tr></thead><tbody><tr><td>Currency</td><td>Body</td><td>Currency</td><td>Required</td><td>Contains information about  currencies on ZAP platform name and ticker are required.</td></tr></tbody></table>

#### Currency Object

Contains information about ZAP's platform currencies.

This object is used by the following operations:

* #### POST /v1/currencies
* #### GET /v1/currencies
* #### GET /v1/currencies/:id
* #### GET /v1/currencies/ticker/:ticker
* #### PUT /v1/currencies/:Id
* #### DELETE /v1/currencies/:Id

The properties included in the **Currency** object are listed below. All property are **Required**.

| Property  | Type     | Description                                                                                |
| --------- | -------- | ------------------------------------------------------------------------------------------ |
| id        | string   | The unique ID for a specific user.                                                         |
| name      | string   | The unique name of the currency.                                                           |
| ticker    | string   | The unique currency ticker.                                                                |
| createdAt | dateTime | This property displays when the currency was created. Used only in response messages.      |
| updatedAt | dateTime | This property displays when the currency was last updated. Used only in response messages. |

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200, with information about the updated currency.

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
     success: true,
    data: {
       "name": "Test Currency",
       "ticker": "TCCY",
       "createdAt": "2023-01-27T16:24:02.098Z",
       "updatedAt": "2023-01-27T17:06:54.318Z",
       "id": "63d3faa23eb4ebbdb0e5fdf6"
     }
}
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name     | Type     | Description                                              |
| -------- | -------- | -------------------------------------------------------- |
| Currency | Currency | Contains information about  Currencies on ZAP  platform. |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 500  | An error occured processing the request                                                                                                                                                                                                                                                                                           |

