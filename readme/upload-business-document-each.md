# Upload Business Document Each

### POST /v1/business/upload <a href="#top" id="top"></a>

Allows a Business user to upload each business document on the platform.

#### HTTP Method <a href="#top" id="top"></a>

POST

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to uspload a business user document.

#### **Sample request** URL <a href="#top" id="top"></a>

```
https://{hostname}/v1/business/upload
```

#### **Sample request headers** <a href="#top" id="top"></a>

```
'Content-Type: application/json'
'Authorization: Bearer  <Bearer Token>'
```

#### **Sample request body - form data** <a href="#top" id="top"></a>

<pre class="language-json"><code class="lang-json"><strong>{
</strong>      "doc": cac.pdf
}
</code></pre>

## Request Header <a href="#samplerequest" id="samplerequest"></a>

| Header        | Description                                                                                                             |
| ------------- | ----------------------------------------------------------------------------------------------------------------------- |
| Content-type  | application/json                                                                                                        |
| Authorization | This is the ZAP Business API Platform authorization token, and must be sent with every API request that requires login. |

## Request Parameters <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="91">Parameter</th><th width="91">Parm Type</th><th width="75">Data Type</th><th width="101">Required</th><th>Description</th></tr></thead><tbody><tr><td>doc</td><td>Body</td><td>file</td><td>Required</td><td>pdf, jpg, and png file formats supported</td></tr></tbody></table>

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200, with information about the uploaded document.

### Sample Response <a href="#samplerequest" id="samplerequest"></a>

The sample responses below shows successful completion of this operation.

#### **Sample** Response Header <a href="#top" id="top"></a>

```
HTTP/1.1 200 OK
Date: Tue, 09 Feb 2024 12:10:15 GMT
Content-Type: application/json; charset=utf-8
```

#### **Sample** Response Body <a href="#top" id="top"></a>

<pre class="language-json"><code class="lang-json">{
    "success": true,
    "data":
<strong>        {
</strong>        "name": "cac.pdf",
        "url": "https://amazon.s3.bucket/19093848293444",
    }
}
</code></pre>

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name | Type | Description                   |
| ---- | ---- | ----------------------------- |
| doc  | doc  | Uploaded document information |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 401  | Unauthorized                                                                                                                                                                                                                                                                                                                      |
| 404  | Not Found: Returned if the request                                                                                                                                                                                                                                                                                                |
| 500  | An error occured processing the request                                                                                                                                                                                                                                                                                           |
