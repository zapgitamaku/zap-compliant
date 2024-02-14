# Add FAQ Article

### POST /v1/faq <a href="#top" id="top"></a>

Allows the site admin user to create a FAQ article on the platform.

#### HTTP Method <a href="#top" id="top"></a>

POST

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows an admin request to Create a FAQ article.

#### **Sample request** URL <a href="#top" id="top"></a>

```
https://{hostname}/v1/faq
```

#### &#x20;**Sample request headers** <a href="#top" id="top"></a>

```
'Content-Type: application/json'
'Authorization: Bearer  <Bearer Token>'
```

#### &#x20;**Sample request body** <a href="#top" id="top"></a>

```json
{
      "question": "What is cryptocurrency?",
      "answer": "Cryptocurrency is a digital or virtual currency that uses cryptography for security and operates independently of a central bank.",
      "category": "Getting-Started",
      "writtenBy": "64412084a5a11fc764c24083"
};
```

## Request Header <a href="#samplerequest" id="samplerequest"></a>

| Header        | Description                                                                                                   |
| ------------- | ------------------------------------------------------------------------------------------------------------- |
| Content-type  | application/json                                                                                              |
| Authorization | This is the ZAP API Platform authorization token, and must be sent with every API request that requires login |

## Request Parameters <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="131">Parameter</th><th width="91">Parm Type</th><th width="92">Data Type</th><th width="101">Required</th><th>Description</th></tr></thead><tbody><tr><td>Faq Article</td><td>Body</td><td>FAQ</td><td>Required</td><td>Contains information about  faq article on ZAP platform. Question, writtenBy, answer and category are required.</td></tr></tbody></table>

#### FAQ Article Object

Contains information about ZAP's platform FAQ articles.

This object is used by the following operations:

* #### POST /v1/faq
* #### GET /v1/faq
* #### GET /v1/faq/:id
* #### GET /v1/faq/:category
* #### PUT /v1/faq/:Id
* #### DELETE /v1/faq/:Id

The properties included in the FAQ Article object are listed below.&#x20;

| Property  | Type     | Description                                                                                   |
| --------- | -------- | --------------------------------------------------------------------------------------------- |
| id        | string   | The faq article unique ID.                                                                    |
| question  | string   | The question the faq article is giving an  answer.                                            |
| answer    | string   | The faq article answer to the question.                                                       |
| category  | string   | The category the faq article questions and answer falls into.                                 |
| writtenBy | string   | The ID of the faq article writer (site admin)                                                 |
| createdAt | dateTime | This property displays when the faq article was created. Used only in response messages.      |
| updatedAt | dateTime | This property displays when the faq article was last updated. Used only in response messages. |

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200 | 201, with information about the new faq article.

### Sample Response <a href="#samplerequest" id="samplerequest"></a>

The sample responses below shows successful completion of this operation.

#### **Sample** Response Header <a href="#top" id="top"></a>

```
HTTP/1.1 201 OK
Date: Thur, 20 Apr 2023 23:14:31 GMT
Content-Type: application/json; charset=utf-8
```

#### **Sample** Response Body <a href="#top" id="top"></a>

```json
{
      success: true,
      data: {
        "question": "What is cryptocurrency?",
        "answer": "Cryptocurrency is a digital or virtual currency that uses cryptography for security and operates independently of a central bank.",
        "category": "Getting-Started",
        "writtenBy": "64412084a5a11fc764c24083",
        "createdAt": "2023-04-20T11:22:44.840Z",
        "updatedAt": "2023-04-20T11:22:44.840Z",
        "id": "64412084a5a11fc764c24093"
      }
    }
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name        | Type        | Description                                               |
| ----------- | ----------- | --------------------------------------------------------- |
| FAQ Article | FAQ Article | Contains information about  FAQ Article on ZAP  platform. |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 500  | An error occured processing the request                                                                                                                                                                                                                                                                                           |

