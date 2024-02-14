# Fetch Bank by Id

### GET /v1/banks/:id <a href="#top" id="top"></a>

Allows a User to get a Bank by Id on the platform.

#### HTTP Method <a href="#top" id="top"></a>

GET

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to fetch a bank by Id.

#### **Sample request** URL <a href="#top" id="top"></a>

```
https://{hostname}/v1/banks/:id
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

| Key | Value  | Description                         |
| --- | ------ | ----------------------------------- |
| Id  | \<Id>  | The unique ID for a specific bank.  |

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
        "name": "ZAP Bank",
        "shortName": "ZAP",
        "sortCode": 1,
        "icon": "https://iconurl.com/hostedhere",
        "brassId": "testBrassIdzap",
        "createdAt": "2023-01-13T19:37:06.503Z",
        "updatedAt": "2023-01-13T19:37:06.504Z",
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

#### Bank Object

Contains information about ZAP's platform bank.

This object is used by the following operations:

* #### DELETE  /v1/banks/:id
* #### PUT  /v1/banks/:id
* #### GET  /v1/banks/:id
* #### GET  /v1/banks/
* #### POST /v1/banks

The properties included in the **Bank** object are listed below.

| Property  | Type     | Description                                                                            |
| --------- | -------- | -------------------------------------------------------------------------------------- |
| id        | string   | The unique ID for a specific bank.                                                     |
| name      | string   | The name of the bank.                                                                  |
| shortName | string   | The unique case-sensitive shortName of the bank.                                       |
| sortCode  | string   | The banks sort code.                                                                   |
| icon      | string   | bank icon                                                                              |
| brassId   | string   | The bank's unique brassId                                                              |
| createdAt | dateTime | This property displays when the bank was created. Used only in response messages.      |
| updatedAt | dateTime | This property displays when the bank was last updated. Used only in response messages. |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                   |
| ---- | --------------------------------------- |
| 404  | The resource could not be found.        |
| 500  | An error occured processing the request |

