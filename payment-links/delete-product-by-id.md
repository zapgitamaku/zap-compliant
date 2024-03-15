# Delete Product by Id

### PUT /v1/product/delete/:id <a href="#top" id="top"></a>

Allows only the Site Admin to delete business user product on the platform.

#### HTTP Method <a href="#top" id="top"></a>

PUT

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to delete a product.

#### **Sample request** URL <a href="#top" id="top"></a>

```json
https://{hostname}/v1/product/delete/:id
```

### **Sample request headers** <a href="#top" id="top"></a>

```
'Content-Type: multipart/form-data'
'Authorization: Bearer  <Bearer Token>'
```



## Request Parameter



| Parameter | Description                   |
| --------- | ----------------------------- |
| id        | The unique id of the Product. |

## Request Header <a href="#samplerequest" id="samplerequest"></a>

| Header        | Description                                                                                                             |
| ------------- | ----------------------------------------------------------------------------------------------------------------------- |
| Content-type  | application/json                                                                                                        |
| Authorization | This is the ZAP Business API Platform authorization token, and must be sent with every API request that requires login. |

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200, with information about the newly created business product.

### Sample Response <a href="#samplerequest" id="samplerequest"></a>

The sample responses below shows successful completion of this operation.

#### **Sample** Response Header <a href="#top" id="top"></a>

```
HTTP/1.1 201 OK
Date: Wed, 08 Feb 2024 13:14:31 GMT
Content-Type: application/json; charset=utf-8
```

#### **Sample** Response Body <a href="#top" id="top"></a>

```
{
    "success": true,
    "data": "Business user product deleted successfully!"
}
```

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 500  | An error occured processing the request                                                                                                                                                                                                                                                                                           |
