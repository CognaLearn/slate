# Questions

<aside class="success">
Resources related to <code>question builder management</code>.
</aside>






## List

> 200

```json
[
  {
    "id": 1,
    "accountID": 1,
    "ownerID": 1,
    
    "question": "What is API Documentation?",
    "questionIsHTML": true,
    "type": "mcqs",
    "attachments": { },
    "options": { },
    "remarks": "Lorem Ipsum",
    "tags": "Lorem Ipsum",
    "canAllowStudentAttachments": true,
    "dateCreated": "2018-05-25T06:01:04Z",
    "lastModified": "2018-05-25T06:01:04Z",
    
    "regexRestriction": "32dfsvdsa234",
    "settings": { },
    "isRequired": true,
    
    "uuid": "d60629e6"
  }
]
```

> 403

```json
{
  "error": {
    "message": "Permission denied.",
    "status_code": 403
  }
}
```

This resource allows to list all questions.

### HTTP Request

`GET [BASE_URL]/questions`

### URL Parameters

`No URL parameters required.`

### Request Header
Key | Value | Description
--------- | ------- | -----------
Content-Type | application/json | Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
Authorization | Bearer $token | Lorem ipsum dolor sit amet, consectetur adipiscing elit.


### Request Parameters

`No request parameters required.`











## Create

> 200

```json
{
  "id": 1,
  "accountID": 1,
  "ownerID": 1,
  
  "question": "What is API Documentation?",
  "questionIsHTML": true,
  "type": "mcqs",
  "attachments": { },
  "options": { },
  "remarks": "Lorem Ipsum",
  "tags": "Lorem Ipsum",
  "canAllowStudentAttachments": true,
  "dateCreated": "2018-05-25T06:01:04Z",
  "lastModified": "2018-05-25T06:01:04Z",
  
  "regexRestriction": "32dfsvdsa234",
  "settings": { },
  "isRequired": true,
    
  "uuid": "d60629e6"
}
```

> 403

```json
{
  "error": {
    "message": "Permission denied.",
    "status_code": 403
  }
}
```

> 404

```json
{
  "error": {
    "message": "No account attached to user.",
    "status_code": 404
  }
}
```

> 422

```json
{
  "message": "422 Unprocessable Entity",
  "errors": {
    "identity": [
      "The question field is required."
    ]
  },
  "status_code": 422
}
```

This resource create new question.

### HTTP Request

`POST [BASE_URL]/questions`

### URL Parameters

`No URL parameters required.`

### Request Header
Key | Value | Description
--------- | ------- | -----------
Content-Type | application/json | Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
Authorization | Bearer $token | Lorem ipsum dolor sit amet, consectetur adipiscing elit.


### Request Parameters
Parameter | Type | Values | Description
--------- | ------- | ------- | -----------
question `required`| json | {"isHTML": true, "question": "<p>5Why did the chicken cross the road?</p>"} | Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
type `required`| enum[string] | mcqs, mcqm, openended, rating, binary | Lorem ipsum dolor sit amet, consectetur adipiscing elit.
isRequired| boolean | true, false | Lorem ipsum dolor sit amet, consectetur adipiscing elit.
canAllowStudentAttachments| boolean | true, false | Lorem ipsum dolor sit amet, consectetur adipiscing elit.
regexRestriction| string | (?=.*\d)(?=.*[a-z])(?=.*[A-Z]).{8,} | Lorem ipsum dolor sit amet, consectetur adipiscing elit.
notes| string | Lorem ipsum dolor sit amet | Lorem ipsum dolor sit amet, consectetur adipiscing elit.
tags| string |  | 
attachments| json | { "key": "value"} | Lorem ipsum dolor sit amet, consectetur adipiscing elit.
options| json | { "key": "value"} | Lorem ipsum dolor sit amet, consectetur adipiscing elit.
labels| json | { "key": "value"} | 
settings| json | { "key": "value"} | Lorem ipsum dolor sit amet, consectetur adipiscing elit.
                




## Retrieve

> 200

```json
{
  "id": 1,
  "accountID": 1,
  "ownerID": 1,
  
  "question": "What is API Documentation?",
  "questionIsHTML": true,
  "type": "mcqs",
  "attachments": { },
  "options": { },
  "remarks": "Lorem Ipsum",
  "tags": "Lorem Ipsum",
  "canAllowStudentAttachments": true,
  "dateCreated": "2018-05-25T06:01:04Z",
  "lastModified": "2018-05-25T06:01:04Z",
  
  "regexRestriction": "32dfsvdsa234",
  "settings": { },
  "isRequired": true,
    
  "uuid": "d60629e6"
}
```

> 403

```json
{
  "error": {
    "message": "Permission denied.",
    "status_code": 403
  }
}
```

> 404

```json
{
  "error": {
    "message": "Not found.",
    "status_code": 404
  }
}
```

This resource retrieve specific question.

### HTTP Request

`GET [BASE_URL]/questions/`**uuid**

### URL Parameters

Parameter | Type | Description
--------- | ------- | -----------
uuid | string | The generated UUID of the selected question.

### Request Header
Key | Value | Description
--------- | ------- | -----------
Content-Type | application/json | Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
Authorization | Bearer $token | Lorem ipsum dolor sit amet, consectetur adipiscing elit.


### Request Parameters

`No request parameters required.`









## Update

> 200

```json
{
  "id": 1,
  "accountID": 1,
  "ownerID": 1,
  
  "question": "What is API Documentation?",
  "questionIsHTML": true,
  "type": "mcqs",
  "attachments": { },
  "options": { },
  "remarks": "Lorem Ipsum",
  "tags": "Lorem Ipsum",
  "canAllowStudentAttachments": true,
  "dateCreated": "2018-05-25T06:01:04Z",
  "lastModified": "2018-05-25T06:01:04Z",
  
  "regexRestriction": "32dfsvdsa234",
  "settings": { },
  "isRequired": true,
    
  "uuid": "d60629e6"
}
```

> 403

```json
{
  "error": {
    "message": "Permission denied.",
    "status_code": 403
  }
}
```

> 404

```json
{
  "error": {
    "message": "Not found.",
    "status_code": 404
  }
}
```

> 422

```json
{
  "message": "422 Unprocessable Entity",
  "errors": {
    "identity": [
      "The question field is required."
    ]
  },
  "status_code": 422
}
```

This resource update selected question.

### HTTP Request

`PUT [BASE_URL]/questions/`**uuid**

### URL Parameters

Parameter | Type | Description
--------- | ------- | -----------
uuid | string | The generated UUID of the selected question.

### Request Header
Key | Value | Description
--------- | ------- | -----------
Content-Type | application/json | Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
Authorization | Bearer $token | Lorem ipsum dolor sit amet, consectetur adipiscing elit.


### Request Parameters
Parameter | Type | Values | Description
--------- | ------- | ------- | -----------
question `required`| json | {"isHTML": true, "question": "<p>5Why did the chicken cross the road?</p>"} | Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
type `required`| enum[string] | mcqs, mcqm, openended, rating, binary | Lorem ipsum dolor sit amet, consectetur adipiscing elit.
isRequired| boolean | true, false | Lorem ipsum dolor sit amet, consectetur adipiscing elit.
canAllowStudentAttachments| boolean | true, false | Lorem ipsum dolor sit amet, consectetur adipiscing elit.
regexRestriction| string | (?=.*\d)(?=.*[a-z])(?=.*[A-Z]).{8,} | Lorem ipsum dolor sit amet, consectetur adipiscing elit.
notes| string | Lorem ipsum dolor sit amet | Lorem ipsum dolor sit amet, consectetur adipiscing elit.
tags| string |  | 
attachments| json | { "key": "value"} | Lorem ipsum dolor sit amet, consectetur adipiscing elit.
options| json | { "key": "value"} | Lorem ipsum dolor sit amet, consectetur adipiscing elit.
labels| json | { "key": "value"} | 
settings| json | { "key": "value"} | Lorem ipsum dolor sit amet, consectetur adipiscing elit.








## Archive

> 200

```json
{
  "deleted": true
}
```

> 403

```json
{
  "error": {
    "message": "Permission denied.",
    "status_code": 403
  }
}
```

> 404

```json
{
  "error": {
    "message": "Not found.",
    "status_code": 404
  }
}
```

This resource archive selected question.

### HTTP Request

`DELETE [BASE_URL]/questions/`**uuid**

### URL Parameters

Parameter | Type | Description
--------- | ------- | -----------
uuid | string | The generated UUID of the selected question.

### Request Header
Key | Value | Description
--------- | ------- | -----------
Content-Type | application/json | Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
Authorization | Bearer $token | Lorem ipsum dolor sit amet, consectetur adipiscing elit.


### Request Parameters

`No request parameters required.`







## Restore

> 200

```json
{
  "id": 1,
  "accountID": 1,
  "ownerID": 1,
  
  "question": "What is API Documentation?",
  "questionIsHTML": true,
  "type": "mcqs",
  "attachments": { },
  "options": { },
  "remarks": "Lorem Ipsum",
  "tags": "Lorem Ipsum",
  "canAllowStudentAttachments": true,
  "dateCreated": "2018-05-25T06:01:04Z",
  "lastModified": "2018-05-25T06:01:04Z",
  
  "regexRestriction": "32dfsvdsa234",
  "settings": { },
  "isRequired": true,
    
  "uuid": "d60629e6"
}
```

> 403

```json
{
  "error": {
    "message": "Permission denied.",
    "status_code": 403
  }
}
```

> 404

```json
{
  "error": {
    "message": "Not found.",
    "status_code": 404
  }
}
```

This resource restore archived question.

### HTTP Request

`GET [BASE_URL]/questions/`**uuid**`/restore`

### URL Parameters

Parameter | Type | Description
--------- | ------- | -----------
uuid | string | The generated UUID of the selected question.

### Request Header
Key | Value | Description
--------- | ------- | -----------
Content-Type | application/json | Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
Authorization | Bearer $token | Lorem ipsum dolor sit amet, consectetur adipiscing elit.


### Request Parameters

`No request parameters required.`