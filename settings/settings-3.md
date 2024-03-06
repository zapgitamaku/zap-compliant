---
description: >-
  Detailed therein are the endpoints required for a constructing a personalised
  configuration.
---

# Update  Business Key Management



### POST /v1/key <a href="#top" id="top"></a>

Allows the Business Users to create a new business key management on the platform.

#### HTTP Method

POST

### Sample Request

The example below shows a request to create a new business key management.

#### Sample request URL

```
https://{hostname}/v1/key/:id
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
    "apiKeyName":  "Google"
}
```



## Request Header

| Header        | Description            |
| ------------- | ---------------------- |
| Content-type  | application/json       |
| Authorization | Bearer \<Bearer token> |

####

### Request Body

| Parameter | Param Type | Data Type | Required | Description                                                                                                          |
| --------- | ---------- | --------- | -------- | -------------------------------------------------------------------------------------------------------------------- |
| Business  | Body       | Object    | Partly   | Contains information about ZAP platform business key management. businessId is required, and apiKeyName is optional. |



#### Business Object

Contains information about ZAP's platform business key management.

The properties included in the **Business** object are listed below. Some properties are **required** while some are optional in the request message.

| Property   | Type   | Description                         |
| ---------- | ------ | ----------------------------------- |
| businessId | String | The unique id of the business user. |
| apiKeyName | String | The Api Key name                    |

### Sample Response body

```
{
    "success": true,
    "data": {
        "businessId": "65e72d7229fb3ceae58b3224",
        "apiKeyName": "Google",
        "webhookUrl": "https://www.google.com",
        "redirectUrl": "https://www.redirecturl.example",
        "apiKeyHash": "$2b$10$8iW6vPTHghIAjjPauGRcOu.EjmT5Bh6mbIqhDj2LrrRWC3fNL3joC",
        "createdAt": "2024-03-05T17:06:26.758Z",
        "updatedAt": "2024-03-05T17:36:21.591Z",
        "id": "65e751126324a14bfd57c1df"
    }
}
```

### Error Codes

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 500  | An error occured processing the request                                                                                                                                                                                                                                                                                           |
