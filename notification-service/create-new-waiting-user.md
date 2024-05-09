# Mobile Crash Notification

### POST /v1/notification/mobileCrash <a href="#top" id="top"></a>

Push a slack notification when a crash occurs on mobile app

#### HTTP Method <a href="#top" id="top"></a>

POST

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to create notifier for mobile crash.

#### **Sample request** URL <a href="#top" id="top"></a>

```
https://{hostname}/v1/notification/mobileCrash
```

#### **Sample request headers** <a href="#top" id="top"></a>

```
'Content-Type: application/json'
"crash-request": "ZAP_MOBILE"
```

#### **Sample request body** <a href="#top" id="top"></a>

<pre class="language-json"><code class="lang-json"><strong>{
</strong>      "errorLog": "Error from mobile app",
      "isFatal" : false
};
</code></pre>

## Request Header <a href="#samplerequest" id="samplerequest"></a>

| Header       | Description      |
| ------------ | ---------------- |
| Content-type | application/json |

## Request Parameters <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="142">Parameter</th><th width="124">Parm Type</th><th width="101">Required</th><th>Description</th></tr></thead><tbody><tr><td>Notification</td><td>Body</td><td>Required</td><td>Contains information the crash notification. errorLog and isFatal are required.</td></tr></tbody></table>

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200 | 201, with message.

### Sample Response <a href="#samplerequest" id="samplerequest"></a>

The sample responses below shows successful completion of this operation.

#### **Sample** Response Header <a href="#top" id="top"></a>

```
HTTP/1.1 200 OK
Date: Thur, 18 Apr 2024 13:14:31 GMT
Content-Type: application/json; charset=utf-8
```

#### **Sample** Response Body <a href="#top" id="top"></a>

```json
{
      "success": true,
      "data": "Mobile app crash notification sent successfully"
    }
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 500  | An error occured processing the request                                                                                                                                                                                                                                                                                           |
