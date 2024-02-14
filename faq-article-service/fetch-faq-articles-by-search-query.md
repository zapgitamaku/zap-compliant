# Fetch FAQ Articles by search query

### GET /v1/faq/search <a href="#top" id="top"></a>

Allows a User to fetch FAQ Articles by search query on the platform.

#### HTTP Method <a href="#top" id="top"></a>

GET

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to get FAQ Articles by search query.

#### **Sample request** URL <a href="#top" id="top"></a>

```
https://{hostname}/v1/faq/search?search=banks
```

#### &#x20;**Sample request headers** <a href="#top" id="top"></a>

```
'Content-Type: application/json'
```

## Request Header <a href="#samplerequest" id="samplerequest"></a>

| Header       | Description      |
| ------------ | ---------------- |
| Content-type | application/json |

## Request Query <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="162">Key</th><th width="164.33333333333331">Value</th><th>Description</th></tr></thead><tbody><tr><td>search</td><td>&#x3C;search> </td><td>The faq articles questions that contain the search value.</td></tr></tbody></table>

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200, with information about the FAQ Articles.

### Sample Response <a href="#samplerequest" id="samplerequest"></a>

The sample responses below shows successful completion of this operation.

#### **Sample** Response Header <a href="#top" id="top"></a>

```
HTTP/1.1 200 OK
Date: Tue, 20 Jul 2023 13:14:31 GMT
Content-Type: application/json; charset=utf-8
```

#### **Sample** Response Body <a href="#top" id="top"></a>

```json
{
    "success": true,
    "data": {
        "faqArticles": [
            {
                "question": "What Nigerian banks does Zap support?",
                "answer": [
                    "Zap supports all Nigerian banks that are licensed by the CBN."
                ],
                "category": "FAQs",
                "icon": "https://res.cloudinary.com/dukdbbrbc/image/upload/v1689342350/icon/1689342350926.svg",
                "writtenBy": "Zap Support",
                "createdAt": "2023-07-14T14:33:47.180Z",
                "updatedAt": "2023-07-14T14:33:47.180Z",
                "id": "64b15ccb8f5dfd871f25f12e"
            }
        ],
        "bodyLimit": 30,
        "pageLimit": 1,
        "dataCount": 1
    }
}
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name        | Type        | Description                                                    |
| ----------- | ----------- | -------------------------------------------------------------- |
| FAQ Article | FAQ Article | Contains information about  the FAQ Articles on ZAP  platform. |

#### FAQ Article Object

The properties included in the **FAQ Article** object are listed below.

<table><thead><tr><th width="200.33333333333331">Property</th><th width="145">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td>string</td><td>The faq article unique ID. </td></tr><tr><td>question</td><td>string</td><td>The question the faq article is giving an  answer.</td></tr><tr><td>answer</td><td>string</td><td>The faq article answer to the question.</td></tr><tr><td>icon</td><td>string</td><td>The icon of the category the faq question falls into.</td></tr><tr><td>category</td><td>string</td><td>The category the faq article questions and answer falls into.</td></tr><tr><td>writtenBy</td><td>string</td><td>The ID of the faq article writer (site admin)</td></tr><tr><td>createdAt</td><td>dateTime</td><td>This property displays when the faq article was created. Used only in response messages.</td></tr><tr><td>updatedAt</td><td>dateTime</td><td>This property displays when the faq article was last updated. Used only in response messages.</td></tr></tbody></table>

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                   |
| ---- | --------------------------------------- |
| 404  | The resource could not be found.        |
| 500  | An error occured processing the request |

