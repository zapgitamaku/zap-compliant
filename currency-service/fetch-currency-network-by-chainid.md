# Fetch Currency Network by ChainId

### GET /api/v1/currencies/chainId/:chainId <a href="#top" id="top"></a>

Allows a User to fetch a currency network by chainId on the platform.

#### HTTP Method <a href="#top" id="top"></a>

GET

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to get a currency network by chainId.

#### **Sample request** URL <a href="#top" id="top"></a>

```
https://{hostname}/api/v1/currencies/chainId/:chainId
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

| Key     | Value       | Description                                  |
| ------- | ----------- | -------------------------------------------- |
| chainId | \<chainId>  | The unique chainId for a specific currency.  |

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200, with information about the currency network.

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
    data: "Bitcoin"
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

* GET /v1/currencies/chainId/:chainId

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                   |
| ---- | --------------------------------------- |
| 404  | The resource could not be found.        |
| 500  | An error occured processing the request |

