# Resolve Bank Details

### GET /v1/bankdetails/resolve <a href="#top" id="top"></a>

Allows a User to resolve bank account name on the platform.

#### HTTP Method <a href="#top" id="top"></a>

GET

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to resolve a bank detail.

#### **Sample request** URL <a href="#top" id="top"></a>

<pre class="language-json"><code class="lang-json"><strong>https://{hostname}/v1/bankdetails/resolve
</strong>https://{hostname}/v1/bankdetails/resolve?bankId=_zap_bank_id&#x26;accountNumber=_user_account_number_
</code></pre>

#### &#x20;**Sample request headers** <a href="#top" id="top"></a>

```
'Content-Type: application/json'
'Authorization: Bearer  <Bearer Token>'
```

#### &#x20;**Sample query params** <a href="#top" id="top"></a>

```
    bankId: "64031879dd16edbf649658ec",
    accountNumber: "8106681998"
```

## Request Header <a href="#samplerequest" id="samplerequest"></a>

| Header        | Description                                                                                                   |
| ------------- | ------------------------------------------------------------------------------------------------------------- |
| Content-type  | application/json                                                                                              |
| Authorization | This is the ZAP API Platform authorization token, and must be sent with every API request that requires login |

## Query Parameters <a href="#samplerequest" id="samplerequest"></a>



The properties included in the **Resolve** params are listed below. All properties are **required**.

<table><thead><tr><th width="190.33333333333331">Property</th><th width="333">Type</th><th>Description</th></tr></thead><tbody><tr><td>bankId</td><td>String</td><td>The unique ID for a specific bank. </td></tr><tr><td>accountNumber</td><td>String</td><td>The user's bank account Number.</td></tr></tbody></table>

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200, with the account name.

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
    "success": true,
    "data": "Agent Da Rhodes"
}
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name | Type   | Description                        |
| ---- | ------ | ---------------------------------- |
| Data | string | Contains the resolved account name |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 500  | An error occured processing the request                                                                                                                                                                                                                                                                                           |

