---
description: >-
  Detailed therein are the endpoints required for a constructing a personalised
  configuration.
---

# Create Business Key Management



### POST /v1/key <a href="#top" id="top"></a>

Allows the Business Users to create a new business key management on the platform.

#### HTTP Method

POST

### Sample Request

The example below shows a request to create a new business key management.

#### Sample request URL

```
https://{hostname}/v1/KEY
```

#### Sample request headers

```
'Content-Type: application/json'
'Authorization: Bearer  <Bearer Token>'
```

#### Sample request body

```
{
    "businessId":  "65e72d7229fb3ceae58b3224",
    "apiKeyName":  "testtest",
    "webhookUrl":  "https://www.google.com"
    "redirectUrl": "https://redirectlink.example"
}
```



## Request Header

| Header        | Description            |
| ------------- | ---------------------- |
| Content-type  | application/json       |
| Authorization | Bearer \<Bearer token> |

####

### Request Body

| Parameter | Param Type | Data Type | Required | Description                                                                                                                                         |
| --------- | ---------- | --------- | -------- | --------------------------------------------------------------------------------------------------------------------------------------------------- |
| Business  | Body       | Object    | Required | Contains information about ZAP platform business key management. businessId, and apiKeyName are required. webhookUrl, and redirectUrl are optional. |



#### Business Object

Contains information about ZAP's platform business key management.

The properties included in the **Business** object are listed below. Some properties are **required** while some are optional in the request message.

| Property    | Type    | Description                         |
| ----------- | ------- | ----------------------------------- |
| businessId  | String  | The unique id of the business user. |
| apiKeyName  | String  | The API Key name                    |
| webhookUrl  | String  | This contains a url to the webhook. |
| redirectUrl | String  | This contains a redirect url        |

### Sample Response body

```
{
    "success": true,
    "data": {
        "businessId": "65e72d7229fb3ceae58b3224",
        "apiKeyName": "testtest",
        "webhookUrl": "https://www.google.com",
        "redirectUrl": "https://www.redirectlink.example",
        "apiKeyHash": "$2b$10$E.w4lvE5awZoHFgka/OoxOAwNWoPSmdMzsItDj43lHJ7E/otkSluq",
        "createdAt": "2024-03-05T14:36:53.815Z",
        "updatedAt": "2024-03-05T14:36:53.815Z",
        "id": "65e72e0529fb3ceae58b3231",
        "apiKey": "b2dx8to38vci56yxyma8t3oe4543l787khmeowpj"
    }
}
```

### Error Codes

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 500  | An error occured processing the request                                                                                                                                                                                                                                                                                           |
