# Fetch Banks

### GET /v1/banks <a href="#top" id="top"></a>

Allows a User to get a list of Banks on the platform.

#### HTTP Method <a href="#top" id="top"></a>

GET

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to fetch a list of banks.

#### **Sample request** URL <a href="#top" id="top"></a>

```
https://{hostname}/v1/banks
```

#### **Sample request query** <a href="#top" id="top"></a>

<table><thead><tr><th width="203">Key</th><th width="260">Value</th><th>Description</th></tr></thead><tbody><tr><td>bodyLimit</td><td>1</td><td>Optional query parameter that specifies the number of banks in the response body</td></tr><tr><td>pageLimit</td><td>3</td><td>Optional query parameter that paginates the list of banks in the response body</td></tr><tr><td>startDate</td><td></td><td>Optional query parameter that adds a start date range to the list of banks in the response body</td></tr><tr><td>endDate</td><td></td><td>Optional query parameter that adds a end date range to the list of banks in the response body</td></tr></tbody></table>

## &#x20; <a href="#samplerequest" id="samplerequest"></a>

#### **Sample request headers** <a href="#top" id="top"></a>

```
'Content-Type: application/json'
'Authorization: Bearer  <Bearer Token>'
```

## Request Header <a href="#samplerequest" id="samplerequest"></a>

| Header        | Description                                                                                                   |
| ------------- | ------------------------------------------------------------------------------------------------------------- |
| Content-type  | application/json                                                                                              |
| Authorization | This is the ZAP API Platform authorization token, and must be sent with every API request that requires login |



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
        "bankData": [
            {
                "name": "Private Racks bank",
                "shortName": "PRB",
                "sortCode": 147174,
                "icon": "https://iconurl.com/hostedhere",
                "brassId": "privateBrassId",
                "createdAt": "2023-02-28T12:52:50.345Z",
                "updatedAt": "2023-02-28T12:52:50.345Z",
                "id": "63fdf9229c58e23ee6f80de1"
            },
            {
                "name": "Tron bank",
                "shortName": "TOOOO",
                "sortCode": 1,
                "icon": "https://iconurl.com/hostedhere",
                "brassId": "testBrassIdg",
                "createdAt": "2023-02-22T10:51:56.451Z",
                "updatedAt": "2023-02-22T10:51:56.451Z",
                "id": "63f5f3cc114e386aeebe0345"
            }
        ],
        "bodyLimit": 2,
        "pageLimit": 1,
        "dataCount": 4
    }
}
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description                    |
| ------------ | ------------------------------ |
| Content-Type | application/json charset=utf-8 |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name     | Type  | Description                                                                         |
| -------- | ----- | ----------------------------------------------------------------------------------- |
| BankData | array | Contains bankobjects containing information  about supported banks on ZAP platform. |

#### Bank Object&#x20;

Contains information about banks on ZAP's platform.

This object is used by the following operations:

* #### POST /v1/banks
* #### GET  /v1/banks/
* #### GET  /v1/banks/:id
* #### PUT  /v1/banks/:id
* #### DELETE  /v1/banks/:id

The properties included in the **Bank** object are listed below.

| Property  | Type     | Description                                                                            |
| --------- | -------- | -------------------------------------------------------------------------------------- |
| id        | string   | The unique ID for a specific user.                                                     |
| name      | string   | The name of the bank.                                                                  |
| shortName | string   | The unique case-sensitive shortName of the bank.                                       |
| sortCode  | string   | The banks sort code.                                                                   |
| icon      | string   | bank icon                                                                              |
| brassId   | string   | The bank's  unique brass ID                                                            |
| createdAt | dateTime | This property displays when the bank was created. Used only in response messages.      |
| updatedAt | dateTime | This property displays when the bank was last updated. Used only in response messages. |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                   |
| ---- | --------------------------------------- |
| 404  | The resource could not be found.        |
| 500  | An error occured processing the request |

