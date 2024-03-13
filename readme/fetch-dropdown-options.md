# Fetch Dropdown Options

### GET /v1/business/dropdown <a href="#top" id="top"></a>

Allows the Site Admin to get dropdown options on the platform.

#### HTTP Method <a href="#top" id="top"></a>

GET

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to fetch dropdown options.

#### **Sample request** URL <a href="#top" id="top"></a>

```json
https://{hostname}/v1/business/dropdown
```

#### **Sample request headers** <a href="#top" id="top"></a>

```javascript
'Content-Type: application/json'
'Authorization: Bearer  <Bearer Token>'
```

## Request Header <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="241">Header</th><th>Description</th></tr></thead><tbody><tr><td>Content-type</td><td>application/json</td></tr><tr><td>Authorization</td><td>This is the ZAP Business API Platform authorization token, and must be sent with every API request that requires login.</td></tr></tbody></table>

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200, with dropdown options.

### Sample Response <a href="#samplerequest" id="samplerequest"></a>

The sample responses below shows successful completion of this operation.

#### **Sample** Response Header <a href="#top" id="top"></a>

```
HTTP/1.1 200 OK
Date: Wed, 09 Feb 2024 23:14:31 GMT
Content-Type: application/json; charset=utf-8
```

#### **Sample** Response Body <a href="#top" id="top"></a>

```json
{
    "success": true,
    "data": {
        "industries": [
            {
                "code": "ag",
                "industry": "Agriculture"
            },
            {
                "code": "ard",
                "industry": "Art & Design"
            },
            {
                "code": "au",
                "industry": "Automotive"
            },
            {
                "code": "bus",
                "industry": "Business Services"
            },
            {
                "code": "co",
                "industry": "Construction"
            },
            {
                "code": "ed",
                "industry": "Education"
            },
            {
                "code": "en",
                "industry": "Entertainment"
            },
            {
                "code": "fi",
                "industry": "Finance"
            },
            {
                "code": "fo",
                "industry": "Food & Beverage"
            },
            {
                "code": "he",
                "industry": "Health"
            },
            {
                "code": "ho",
                "industry": "Hospitality"
            },
            {
                "code": "it",
                "industry": "Information Technology"
            },
            {
                "code": "le",
                "industry": "Legal"
            },
            {
                "code": "ma",
                "industry": "Manufacturing"
            },
            {
                "code": "mak",
                "industry": "Marketing"
            },
            {
                "code": "me",
                "industry": "Media"
            },
            {
                "code": "no",
                "industry": "Nonprofit"
            },
            {
                "code": "re",
                "industry": "Real Estate"
            },
            {
                "code": "ret",
                "industry": "Retail"
            },
            {
                "code": "tr",
                "industry": "Transportation"
            },
            {
                "code": "other",
                "industry": "Other"
            }
        ],
        "states": [
            {
                "code": "ab",
                "state": "Abia"
            },
            {
                "code": "ad",
                "state": "Adamawa"
            },
            {
                "code": "ak",
                "state": "Akwa Ibom"
            },
            {
                "code": "an",
                "state": "Anambra"
            },
            {
                "code": "bau",
                "state": "Bauchi"
            },
            {
                "code": "bay",
                "state": "Bayelsa"
            },
            {
                "code": "ben",
                "state": "Benue"
            },
            {
                "code": "bor",
                "state": "Borno"
            },
            {
                "code": "cro",
                "state": "Cross River"
            },
            {
                "code": "del",
                "state": "Delta"
            },
            {
                "code": "ebo",
                "state": "Ebonyi"
            },
            {
                "code": "ed",
                "state": "Edo"
            },
            {
                "code": "ek",
                "state": "Ekiti"
            },
            {
                "code": "en",
                "state": "Enugu"
            },
            {
                "code": "gom",
                "state": "Gombe"
            },
            {
                "code": "im",
                "state": "Imo"
            },
            {
                "code": "ji",
                "state": "Jigawa"
            },
            {
                "code": "kad",
                "state": "Kaduna"
            },
            {
                "code": "kan",
                "state": "Kano"
            },
            {
                "code": "kat",
                "state": "Katsina"
            },
            {
                "code": "keb",
                "state": "Kebbi"
            },
            {
                "code": "kog",
                "state": "Kogi"
            },
            {
                "code": "kwa",
                "state": "Kwara"
            },
            {
                "code": "lag",
                "state": "Lagos"
            },
            {
                "code": "nas",
                "state": "Nasarawa"
            },
            {
                "code": "nig",
                "state": "Niger"
            },
            {
                "code": "og",
                "state": "Ogun"
            },
            {
                "code": "on",
                "state": "Ondo"
            },
            {
                "code": "os",
                "state": "Osun"
            },
            {
                "code": "oy",
                "state": "Oyo"
            },
            {
                "code": "pl",
                "state": "Plateau"
            },
            {
                "code": "ri",
                "state": "Rivers"
            },
            {
                "code": "so",
                "state": "Sokoto"
            },
            {
                "code": "ta",
                "state": "Taraba"
            },
            {
                "code": "yo",
                "state": "Yobe"
            },
            {
                "code": "za",
                "state": "Zamfara"
            },
            {
                "code": "abj",
                "state": "Abuja (FCT)"
            }
        ],
        "countries": [
            {
                "code": "ng",
                "country": "Nigeria"
            }
        ],
        "utilityBill": [
            {
                "code": "elec",
                "bill": "Electricity bill"
            },
            {
                "code": "water",
                "bill": "Water bill"
            },
            {
                "code": "waste",
                "bill": "Waste disposal bill"
            },
            {
                "code": "others",
                "bill": "Others"
            }
        ],
        "gender": [
            {
                "code": "ma",
                "gender": "Male"
            },
            {
                "code": "fe",
                "gender": "Female"
            },
            {
                "code": "rather",
                "gender": "Rather not say"
            }
        ]
    }
}
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name             | Type   | Description                                                            |
| ---------------- | ------ | ---------------------------------------------------------------------- |
| dropdown options | Object | Contains information about the ZAP platform business dropdown options. |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 500  | An error occured while processing the request                                                                                                                                                                                                                                                                                     |
