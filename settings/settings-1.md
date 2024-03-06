---
description: >-
  Detailed therein are the endpoints required for a constructing a personalised
  configuration.
---

# Fetch Business Key Management by BusinessUserId



### POST /v1/key <a href="#top" id="top"></a>

Allows the Business Users to create a new business key management on the platform.

#### HTTP Method

POST

### Sample Request

The example below shows a request to create a new business key management.

#### Sample request URL

```
https://{hostname}/v1/key/business/:businessId
```

#### Sample request headers

```
'Content-Type: application/json'
'Authorization: Bearer  <Bearer Token>'
```



## Request Header

| Header        | Description                                                                                                             |
| ------------- | ----------------------------------------------------------------------------------------------------------------------- |
| Content-type  | application/json                                                                                                        |
| Authorization | This is the ZAP Business API Platform authorization token, and must be sent with every API request that requires login. |

####

## Response

If successful, this operation returns HTTP status code 200, with a business.

## Sample Response

The sample responses below shows successful completion of this operation.

### Sample Respones Header

```
HTTP/1.1 200 OK
Date: Wed, 09 Feb 2024 23:14:31 GMT
Content-Type: application/json; charset=utf-8
```

### Sample Response body

```
{
    "success": true,
    "data": [
        {
            "businessId": "65e72d7229fb3ceae58b3224",
            "apiKeyName": "testtest",
            "webhookUrl": "https://www.google.com",
            "redirectUrl": "https://www.redirecturl.example",
            "apiKeyHash": "$2b$10$8iW6vPTHghIAjjPauGRcOu.EjmT5Bh6mbIqhDj2LrrRWC3fNL3joC",
            "createdAt": "2024-03-05T17:06:26.758Z",
            "updatedAt": "2024-03-05T17:06:26.758Z",
            "id": "65e751126324a14bfd57c1df"
        }
    ]
}
```

## Response Header

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

## Response Body

| Name | Type   | Description                                             |
| ---- | ------ | ------------------------------------------------------- |
| key  | Object | Contains information about the business key management. |

### Error Codes

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 500  | An error occured processing the request                                                                                                                                                                                                                                                                                           |
