# Questions

<aside class="success">
Resources related to <code>question builder management</code>.
</aside>






## List

> 200

```json
{
    "data": [
        {
            "id": 1,
            "accountID": 1,
            "ownerID": 1,
            "question": "<p>Why did the chicken cross the road?</p>",
            "questionIsHTML": true,
            "type": "mcqs",
            "attachments": {
                "test": true
            },
            "options": {
                "test": true
            },
            "labels": null,
            "remarks": "Notes",
            "tags": null,
            "canAllowStudentAttachments": 0,
            "dateCreated": "2018-07-13T06:54:41Z",
            "lastModified": "2018-07-13T06:54:41Z",
            "regexRestriction": "Question #1",
            "settings": {
                "test": false
            },
            "isRequired": true,
            "uuid": "8e0fcc9d-f4e9-4a0f-a9e3-f382fc3401c4",
            "isArchived": false,
            "isTrashed": false
        }
    ],
    "meta": {
        "pagination": {
            "total": 9,
            "count": 3,
            "per_page": 3,
            "current_page": 1,
            "total_pages": 3,
            "links": {
                "next": "http://localhost:8041/api/v1/questions?page=2"
            }
        }
    }
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

This resource allows to list all questions.




### HTTP Request

`GET [BASE_URL]/questions`

### HTTP Get Parameters

[Standard HTTP Get Parameters](#principles)

`i.e. [BASE_URL]/questions?page=1&per_page=3`

### Request Headers
Key | Value | Description
--------- | ------- | -----------
`Content-Type` | **application/json** | Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
`Authorization` | **Bearer $token** | Lorem ipsum dolor sit amet, consectetur adipiscing elit.


### HTTP Post Parameters

`No HTTP post parameters required.`











## Create

> 201

```json
{
    "data": {
        "id": 6,
        "accountID": 1,
        "ownerID": 1,
        "question": "<p>Why did the chicken cross the road?</p>",
        "questionIsHTML": true,
        "type": "mcqs",
        "attachments": {
            "test": true
        },
        "options": {
            "test": true
        },
        "labels": null,
        "remarks": "Notes",
        "tags": null,
        "canAllowStudentAttachments": 0,
        "dateCreated": "2018-07-13T07:14:46Z",
        "lastModified": "2018-07-19T06:19:14Z",
        "regexRestriction": "Question #1",
        "settings": {
            "test": false
        },
        "isRequired": true,
        "uuid": "afcbd354-f1a9-4f27-a915-32f59c5237e0",
        "isArchived": false,
        "isTrashed": false
    }
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

### HTTP Get Parameters

`No HTTP get parameters required.`

### Request Headers
Key | Value | Description
--------- | ------- | -----------
`Content-Type` | **application/json** | Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
`Authorization` | **Bearer $token** | Lorem ipsum dolor sit amet, consectetur adipiscing elit.


### HTTP Post Parameters
Parameter | Description
--------- | -----------
question <br /> `required`| **json** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
type <br /> `required`| **enum[string]** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
isRequired| **boolean** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
canAllowStudentAttachments| **boolean** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
regexRestriction| **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
notes| **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
tags| **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique. 
attachments| **json** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
options| **json** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
labels| **json** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique. 
settings| **json** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
                




## Retrieve

> 200

```json
{
    "data": {
        "id": 6,
        "accountID": 1,
        "ownerID": 1,
        "question": "<p>Why did the chicken cross the road?</p>",
        "questionIsHTML": true,
        "type": "mcqs",
        "attachments": {
            "test": true
        },
        "options": {
            "test": true
        },
        "labels": null,
        "remarks": "Notes",
        "tags": null,
        "canAllowStudentAttachments": 0,
        "dateCreated": "2018-07-13T07:14:46Z",
        "lastModified": "2018-07-19T06:19:14Z",
        "regexRestriction": "Question #1",
        "settings": {
            "test": false
        },
        "isRequired": true,
        "uuid": "afcbd354-f1a9-4f27-a915-32f59c5237e0",
        "isArchived": false,
        "isTrashed": false
    }
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

### HTTP Get Parameters

Parameter | Type | Description
--------- | ------- | -----------
uuid | string | The generated UUID of the selected question.

### Request Headers
Key | Value | Description
--------- | ------- | -----------
`Content-Type` | **application/json** | Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
`Authorization` | **Bearer $token** | Lorem ipsum dolor sit amet, consectetur adipiscing elit.


### HTTP Post Parameters

`No HTTP post parameters required.`









## Update

> 200

```json
{
    "data": {
        "id": 6,
        "accountID": 1,
        "ownerID": 1,
        "question": "<p>Why did the chicken cross the road?</p>",
        "questionIsHTML": true,
        "type": "mcqs",
        "attachments": {
            "test": true
        },
        "options": {
            "test": true
        },
        "labels": null,
        "remarks": "Notes",
        "tags": null,
        "canAllowStudentAttachments": 0,
        "dateCreated": "2018-07-13T07:14:46Z",
        "lastModified": "2018-07-19T06:19:14Z",
        "regexRestriction": "Question #1",
        "settings": {
            "test": false
        },
        "isRequired": true,
        "uuid": "afcbd354-f1a9-4f27-a915-32f59c5237e0",
        "isArchived": false,
        "isTrashed": false
    }
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

### HTTP Get Parameters

Parameter | Type | Description
--------- | ------- | -----------
uuid | string | The generated UUID of the selected question.

### Request Headers
Key | Value | Description
--------- | ------- | -----------
`Content-Type` | **application/json** | Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
`Authorization` | **Bearer $token** | Lorem ipsum dolor sit amet, consectetur adipiscing elit.


### HTTP Post Parameters
Parameter | Description
--------- | -----------
question <br /> `required`| **json** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
type <br /> `required`| **enum[string]** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
isRequired| **boolean** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
canAllowStudentAttachments| **boolean** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
regexRestriction| **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
notes| **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
tags| **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique. 
attachments| **json** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
options| **json** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
labels| **json** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique. 
settings| **json** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.









## Archive

> 200 (Archived)

```json
{
  "archived": true
}
```

> 200 (Unarchived)

```json
{
    "data": {
        "id": 6,
        "accountID": 1,
        "ownerID": 1,
        "question": "<p>Why did the chicken cross the road?</p>",
        "questionIsHTML": true,
        "type": "mcqs",
        "attachments": {
            "test": true
        },
        "options": {
            "test": true
        },
        "labels": null,
        "remarks": "Notes",
        "tags": null,
        "canAllowStudentAttachments": 0,
        "dateCreated": "2018-07-13T07:14:46Z",
        "lastModified": "2018-07-19T06:19:14Z",
        "regexRestriction": "Question #1",
        "settings": {
            "test": false
        },
        "isRequired": true,
        "uuid": "afcbd354-f1a9-4f27-a915-32f59c5237e0",
        "isArchived": false,
        "isTrashed": false
    }
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

This resource archive/unarchive selected question.

### HTTP Request

`PATCH [BASE_URL]/questions/`**uuid**

### HTTP Get Parameters

Parameter | Type | Description
--------- | ------- | -----------
uuid | string | The generated UUID of the selected question.

### Request Headers
Key | Value | Description
--------- | ------- | -----------
`Content-Type` | **application/json** | Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
`Authorization` | **Bearer $token** | Lorem ipsum dolor sit amet, consectetur adipiscing elit.


### HTTP Post Parameters

`No HTTP post parameters required.`









## Trash

> 200

```json
{
  "trashed": true
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

This resource trash selected question.

### HTTP Request

`DELETE [BASE_URL]/questions/`**uuid**

### HTTP Get Parameters

Parameter | Type | Description
--------- | ------- | -----------
uuid | string | The generated UUID of the selected question.

### Request Headers
Key | Value | Description
--------- | ------- | -----------
`Content-Type` | **application/json** | Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
`Authorization` | **Bearer $token** | Lorem ipsum dolor sit amet, consectetur adipiscing elit.


### HTTP Post Parameters

`No HTTP post parameters required.`






## Untrash

> 200

```json
{
    "data": {
        "id": 6,
        "accountID": 1,
        "ownerID": 1,
        "question": "<p>Why did the chicken cross the road?</p>",
        "questionIsHTML": true,
        "type": "mcqs",
        "attachments": {
            "test": true
        },
        "options": {
            "test": true
        },
        "labels": null,
        "remarks": "Notes",
        "tags": null,
        "canAllowStudentAttachments": 0,
        "dateCreated": "2018-07-13T07:14:46Z",
        "lastModified": "2018-07-19T06:19:14Z",
        "regexRestriction": "Question #1",
        "settings": {
            "test": false
        },
        "isRequired": true,
        "uuid": "afcbd354-f1a9-4f27-a915-32f59c5237e0",
        "isArchived": false,
        "isTrashed": false
    }
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

This resource untrash trashed question.

### HTTP Request

`GET [BASE_URL]/questions/`**uuid**`/restore`

### HTTP Get Parameters

Parameter | Type | Description
--------- | ------- | -----------
uuid | string | The generated UUID of the selected question.

### Request Headers
Key | Value | Description
--------- | ------- | -----------
`Content-Type` | **application/json** | Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
`Authorization` | **Bearer $token** | Lorem ipsum dolor sit amet, consectetur adipiscing elit.


### HTTP Post Parameters

`No HTTP post parameters required.`