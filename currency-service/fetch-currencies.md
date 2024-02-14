# Fetch Currencies

### GET /v1/currencies <a href="#top" id="top"></a>

Allows a User to get a list of currencies on the platform.

#### HTTP Method <a href="#top" id="top"></a>

GET

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to get a list of currencies.

#### **Sample request** URL <a href="#top" id="top"></a>

```
https://{hostname}/v1/currencies/?
```

#### **Sample request query** <a href="#top" id="top"></a>

<table><thead><tr><th width="225">Key</th><th>Value</th><th>Description</th></tr></thead><tbody><tr><td>bodyLimit</td><td>1</td><td>Optional query parameter that specifies the number of Bank details in the response body</td></tr><tr><td>pageLimit</td><td>3</td><td>Optional query parameter that paginates the list of bank details in the response body</td></tr><tr><td>startDate</td><td></td><td>Optional query parameter that adds a start date range to the list of bank details in the response body</td></tr><tr><td>endDate</td><td></td><td>Optional query parameter that adds a end date range to the list of bank details in the response body</td></tr></tbody></table>



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

#### Currency Object

Contains information about ZAP's platform currency.

This object is used by the following operations:

* #### POST /v1/currencies
* #### GET /v1/currencies
* #### GET /v1/currencies/:Id
* #### PUT /v1/currencies/:Id
* #### DELETE /v1/currencies/:Id

The properties included in the **Currency** object are listed below.

| Property  | Type     | Description                                                                                |
| --------- | -------- | ------------------------------------------------------------------------------------------ |
| id        | string   | The unique ID for a specific user.                                                         |
| name      | string   | The unique name of the currency.                                                           |
| ticker    | string   | The unique currency ticker.                                                                |
| icon      | string   | currency icon                                                                              |
| createdAt | dateTime | This property displays when the currency was created. Used only in response messages.      |
| updatedAt | dateTime | This property displays when the currency was last updated. Used only in response messages. |

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200, with information about the currencies.

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
      data: { currencyData: [
        {
       "name": "Test Currency",
       "ticker": "TCA",
       "createdAt": "2023-01-27T16:24:02.098Z",
       "updatedAt": "2023-01-27T16:24:02.098Z",
       "id": "63d3faa23eb4ebbdb0e5fdf6"
     },
     {
       "name": "Test Currency 2",
       "ticker": "TCB",,
       "createdAt": "2023-01-27T16:24:02.098Z",
       "updatedAt": "2023-01-27T16:24:02.098Z",
       "id": "63d3faa23eb4ebbdb0e5fdf9"
     }
    ],
    "bodyLimit": 10,
    "pageLimit": 1,
    "dataCount": 2
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

| Item | Value                                   |
| ---- | --------------------------------------- |
| 404  | The resource could not be found.        |
| 500  | An error occured processing the request |

