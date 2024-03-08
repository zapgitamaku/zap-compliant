# Create Product

### POST /v1/product <a href="#top" id="top"></a>

Allows the Site Admin and zap pay business to add products to the platform.

#### HTTP Method <a href="#top" id="top"></a>

POST

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to add a new product.

#### **Sample request** URL <a href="#top" id="top"></a>

```json
https://{hostname}/v1/product
```

### **Sample request headers** <a href="#top" id="top"></a>

```
'Content-Type: multipart/form-data'
'Authorization: Bearer  <Bearer Token>'
```

#### For zap pay: <a href="#top" id="top"></a>

```
'Content-Type: multipart/form-data'
'api-key: wjjmaesvms37w30sdoneox2l3homvbytlhf320s2
```

#### **Sample request body** <a href="#top" id="top"></a>

```json
it takes both file data and body data

{
      "image": productImage.jpg
}

{
    "businessId": "65c4e4945d2869e8324210d8",
    "price": 2000,
    "name": "test",
    "description": "test product"
}
```

## Request Header <a href="#samplerequest" id="samplerequest"></a>

| Header        | Description                                                                                                             |
| ------------- | ----------------------------------------------------------------------------------------------------------------------- |
| Content-type  | application/json                                                                                                        |
| Authorization | This is the ZAP Business API Platform authorization token, and must be sent with every API request that requires login. |
| api-key       | This is the api key for the zap pay communication with the platform.                                                    |

## Request Parameters <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="99">Parameter</th><th width="91">Parm Type</th><th width="75">Data Type</th><th width="101">Required</th><th>Description</th></tr></thead><tbody><tr><td>image</td><td>Body</td><td>file</td><td>Required</td><td> jpg and png file formats supported</td></tr></tbody></table>

## Request Body <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="122">Parameter</th><th width="73">Param Type</th><th width="86">Data Type</th><th width="100">Required</th><th>Description</th></tr></thead><tbody><tr><td>Product</td><td>Body</td><td>Object</td><td>Required</td><td>Contains information about ZAP platform business owner. businessId, price, name, description.</td></tr></tbody></table>

#### Business Product

Contains information about ZAP's business product.

The properties included in the **Product** object are listed below. All properties are **required** in the request message.

| Property    | Type   | Description                         |
| ----------- | ------ | ----------------------------------- |
| businessId  | string | The unique id of the business user. |
| name        | string | The product  name                   |
| description | string | The product description.            |
| price       | number | The price of the product.           |

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 201, with information about the newly created business product.

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
    "data": {
        "businessId": "65e71840973f0e97fb99849d",
        "name": "test Product",
        "description": "testing product",
        "image": "https://res.cloudinary.com/dukdbbrbc/image/upload/v1709659340/business-verification-production/45e61817-b8c4-446c-8513-b74728a79bf9.png",
        "price": 1000,
        "createdAt": "2024-03-05T17:22:22.175Z",
        "updatedAt": "2024-03-05T17:22:22.175Z",
        "id": "65e754ce2b2a2d15c1dadca7"
    }
}
```

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 500  | An error occured processing the request                                                                                                                                                                                                                                                                                           |
