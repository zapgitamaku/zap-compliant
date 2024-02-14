# Update Verifications Provider status

### PUT /v1/verifications/provider/status <a href="#top" id="top"></a>

Allows a User to update verification provider status data on the platform.

#### HTTP Method <a href="#top" id="top"></a>

PUT

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to get update verification provider status data.

#### **Sample request** URL <a href="#top" id="top"></a>

```
https://{hostname}/v1/verifications/provider/status
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

#### **Sample** Request Body <a href="#top" id="top"></a>

```
{
    "passport": true,
    "nin": true,
    "vnin": false,
    "votercard": true,
    "driverlicense": true
}
```

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200, with information about the status of the update.

### Sample Response <a href="#samplerequest" id="samplerequest"></a>

The sample responses below shows successful completion of this operation.

#### **Sample** Response Header <a href="#top" id="top"></a>

```
HTTP/1.1 200 OK
Date: Wed, 01 Mar 2023 00:48:10 GMT
Content-Type: application/json; charset=utf-8
```

#### **Sample** Response Body <a href="#top" id="top"></a>

<pre class="language-json"><code class="lang-json"><strong>{
</strong>    "success": true,
    "data": "Verification Status updated"
}
</code></pre>

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name         | Type         | Description                                                                            |
| ------------ | ------------ | -------------------------------------------------------------------------------------- |
| Verification | Verification | Contains information about the updated verification providers status on ZAP  platform. |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                   |
| ---- | --------------------------------------- |
| 404  | The resource could not be found.        |
| 500  | An error occured processing the request |

