# Fetch Currency by Id

### GET /v1/currencies/:Id <a href="#top" id="top"></a>

Allows a User to fetch a currency by Id on the platform.

#### HTTP Method <a href="#top" id="top"></a>

GET

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to get a currency by ID.

#### **Sample request** URL <a href="#top" id="top"></a>

```
https://{hostname}/v1/currencies/:Id
```

#### &#x20;**Sample request headers** <a href="#top" id="top"></a>

```
'Content-Type: application/json'
'Authorization: Bearer  <Bearer Token>'
```

## Request Header <a href="#samplerequest" id="samplerequest"></a>

| Header        | Description                                                                                                    |
| ------------- | -------------------------------------------------------------------------------------------------------------- |
| Content-type  | application/json                                                                                               |
| Authorization | This is the ZAP API Platform authorization token, and must be sent with every API request that requires login. |

## Request Parameters <a href="#samplerequest" id="samplerequest"></a>

| Key | Value  | Description                             |
| --- | ------ | --------------------------------------- |
| Id  | \<Id>  | The unique ID for a specific currency.  |

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200, with information about the currency.

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
              "icon": "https://iconurl.com/hostedhere",
              "createdAt": "2023-01-27T16:24:02.098Z",
              "updatedAt": "2023-01-27T16:24:02.098Z",
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

#### Currency Object

Contains information about ZAP's platform currency.

This object is used by the following operations:

* #### POST /v1/currencies
* #### GET /v1/currencies
* #### GET /v1/currencies/:Id
* #### PUT /v1/currencies/:Id
* #### DELETE /v1/currencies/:Id

The properties included in the **Currency** object are listed below.

<table><thead><tr><th width="250.33333333333331">Property</th><th>Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td>string</td><td>The unique ID for a specific user. </td></tr><tr><td>name</td><td>string</td><td>The unique name of the currency.</td></tr><tr><td>ticker</td><td>string</td><td>The unique currency ticker. Required in request.</td></tr><tr><td>icon</td><td>string</td><td>The icon url for the currency</td></tr><tr><td>createdAt</td><td>dateTime</td><td>This property displays when the currency was created. Used only in response messages.</td></tr><tr><td>updatedAt</td><td>dateTime</td><td>This property displays when the currency was last updated. Used only in response messages.</td></tr></tbody></table>

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                    |
| ---- | ---------------------------------------- |
| 404  | The resource could not be found.         |
| 500  | An error occurred processing the request |

