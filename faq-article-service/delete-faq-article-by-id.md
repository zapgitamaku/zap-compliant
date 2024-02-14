# Delete FAQ Article by Id

### DELETE /v1/faq/:Id <a href="#top" id="top"></a>

Allows a site admin User to delete a FAQ Article by Id on the platform. (soft)

#### HTTP Method <a href="#top" id="top"></a>

DELETE

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to delete a FAQ Article by ID.

#### **Sample request** URL <a href="#top" id="top"></a>

```
https://{hostname}/v1/faq/:Id
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

| Key | Value  | Description                                |
| --- | ------ | ------------------------------------------ |
| Id  | \<Id>  | The unique ID for a specific FAQ Article.  |

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200, with the success message.

### Sample Response <a href="#samplerequest" id="samplerequest"></a>

The sample responses below shows successful completion of this operation.

#### **Sample** Response Header <a href="#top" id="top"></a>

```
HTTP/1.1 200 OK
Date: Tue, 25 Apr 2023 13:14:31 GMT
Content-Type: application/json; charset=utf-8
```

#### **Sample** Response Body <a href="#top" id="top"></a>

```json
{
      success: true,
      data: "FAQ Article deleted successfully"
  }
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                   |
| ---- | --------------------------------------- |
| 404  | The resource could not be found.        |
| 500  | An error occured processing the request |

