# Courses

<aside class="success">
Resources related to <code>course management</code>.
</aside>






## List of Courses

> 200

```json
{
    "data": [
        {
            "id": 1,
            "accountID": 2,
            "ownerID": 2,
            "description": "<p>Sample Description1</p>",
            "descriptionIsHTML": true,
            "consumerKeyLTI": "KSsFLCicxWQ7X9J1wHg0",
            "sharedSecretLTI": "DiHguLhr1vj5TVwQNopc",
            "code": "S-CODE-112",
            "startDate": "2018-08-23T00:00:00Z",
            "endDate": "2018-08-26T00:00:00Z",
            "isPublished": true,
            "configURLLTI": "http://localhost:8041/lti/config/KSsFLCicxWQ7X9J1wHg0",
            "launchURLLTI": "http://localhost:8041/lti/launch/KSsFLCicxWQ7X9J1wHg0",
            "uuid": "de4d9088-1b6d-4080-ae7a-ec6b7bb8b101",
            "isArchived": false,
            "isTrashed": false,
            "dateCreated": "2018-07-23T10:30:43Z",
            "lastModified": "2018-07-23T14:41:12Z"
        }
    ],
    "meta": {
        "pagination": {
            "total": 1,
            "count": 1,
            "per_page": 10,
            "current_page": 1,
            "total_pages": 1,
            "links": []
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

This resource allows to list all courses.




### HTTP Request

`GET [BASE_URL]/courses`

### HTTP Get Parameters

[Standard HTTP Get Parameters](#principles)

`i.e. [BASE_URL]/courses?page=1&per_page=3`

### Request Headers
Key | Value | Description
--------- | ------- | -----------
`Content-Type` | **application/json** | Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
`Authorization` | **Bearer $token** | Lorem ipsum dolor sit amet, consectetur adipiscing elit.


### HTTP Post Parameters

`No HTTP post parameters required.`











## Create Course

> 201

```json
{
    "data": {
        "id": 2,
        "accountID": 2,
        "ownerID": 2,
        "description": "<p>Sample Description</p>",
        "descriptionIsHTML": true,
        "consumerKeyLTI": "7jaqP8ZSwsAXVfWM3emN",
        "sharedSecretLTI": "pwWjBIslrRoq4vGxhU3f",
        "code": "S-CODE-2",
        "startDate": "2018-07-23T00:00:00Z",
        "endDate": "2018-07-26T00:00:00Z",
        "isPublished": false,
        "configURLLTI": "http://localhost:8041/lti/config/7jaqP8ZSwsAXVfWM3emN",
        "launchURLLTI": "http://localhost:8041/lti/launch/7jaqP8ZSwsAXVfWM3emN",
        "uuid": "d11281dd-8105-4d7a-a56a-9febeb16a215",
        "isArchived": false,
        "isTrashed": false,
        "dateCreated": "2018-07-24T05:32:48Z",
        "lastModified": "2018-07-24T05:32:48Z"
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
      "The name field is required."
    ]
  },
  "status_code": 422
}
```

This resource create new course.

### HTTP Request

`POST [BASE_URL]/courses`

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
name <br /> `required`| **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
code| **json** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
startDate <br /> `required`| **date** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
endDate <br /> `required`| **date** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
description| **json** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.





## Retrieve Course

> 200

```json
{
    "data": {
        "id": 2,
        "accountID": 2,
        "ownerID": 2,
        "description": "<p>Sample Description</p>",
        "descriptionIsHTML": true,
        "consumerKeyLTI": "7jaqP8ZSwsAXVfWM3emN",
        "sharedSecretLTI": "pwWjBIslrRoq4vGxhU3f",
        "code": "S-CODE-2",
        "startDate": "2018-07-23T00:00:00Z",
        "endDate": "2018-07-26T00:00:00Z",
        "isPublished": true,
        "configURLLTI": "http://localhost:8041/lti/config/7jaqP8ZSwsAXVfWM3emN",
        "launchURLLTI": "http://localhost:8041/lti/launch/7jaqP8ZSwsAXVfWM3emN",
        "uuid": "d11281dd-8105-4d7a-a56a-9febeb16a215",
        "isArchived": false,
        "isTrashed": false,
        "dateCreated": "2018-07-24T05:32:48Z",
        "lastModified": "2018-07-24T05:32:48Z"
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

This resource retrieve specific course.

### HTTP Request

`GET [BASE_URL]/courses/`**uuid**

URI Parameter | Type | Description
--------- | ------- | -----------
uuid | string | The generated UUID of the selected course.

### HTTP Get Parameters

`No HTTP get parameters required.`

### Request Headers
Key | Value | Description
--------- | ------- | -----------
`Content-Type` | **application/json** | Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
`Authorization` | **Bearer $token** | Lorem ipsum dolor sit amet, consectetur adipiscing elit.


### HTTP Post Parameters

`No HTTP post parameters required.`









## Update Course

> 200

```json
{
    "data": {
        "id": 2,
        "accountID": 2,
        "ownerID": 2,
        "description": "<p>Sample Description</p>",
        "descriptionIsHTML": true,
        "consumerKeyLTI": "7jaqP8ZSwsAXVfWM3emN",
        "sharedSecretLTI": "pwWjBIslrRoq4vGxhU3f",
        "code": "S-CODE-2",
        "startDate": "2018-08-23T00:00:00Z",
        "endDate": "2018-08-26T00:00:00Z",
        "isPublished": true,
        "configURLLTI": "http://localhost:8041/lti/config/7jaqP8ZSwsAXVfWM3emN",
        "launchURLLTI": "http://localhost:8041/lti/launch/7jaqP8ZSwsAXVfWM3emN",
        "uuid": "d11281dd-8105-4d7a-a56a-9febeb16a215",
        "isArchived": false,
        "isTrashed": false,
        "dateCreated": "2018-07-24T05:32:48Z",
        "lastModified": "2018-07-24T05:42:01Z"
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
      "The name field is required."
    ]
  },
  "status_code": 422
}
```

This resource update selected course.

### HTTP Request

`PUT [BASE_URL]/courses/`**uuid**

URI Parameter | Type | Description
--------- | ------- | -----------
uuid | string | The generated UUID of the selected course.

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
name <br /> `required`| **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
code| **json** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
startDate <br /> `required`| **date** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
endDate <br /> `required`| **date** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
description| **json** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.









## Archive/Unarchive Course

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
        "id": 2,
        "accountID": 2,
        "ownerID": 2,
        "description": "<p>Sample Description</p>",
        "descriptionIsHTML": true,
        "consumerKeyLTI": "7jaqP8ZSwsAXVfWM3emN",
        "sharedSecretLTI": "pwWjBIslrRoq4vGxhU3f",
        "code": "S-CODE-2",
        "startDate": "2018-08-23T00:00:00Z",
        "endDate": "2018-08-26T00:00:00Z",
        "isPublished": true,
        "configURLLTI": "http://localhost:8041/lti/config/7jaqP8ZSwsAXVfWM3emN",
        "launchURLLTI": "http://localhost:8041/lti/launch/7jaqP8ZSwsAXVfWM3emN",
        "uuid": "d11281dd-8105-4d7a-a56a-9febeb16a215",
        "isArchived": false,
        "isTrashed": false,
        "dateCreated": "2018-07-24T05:32:48Z",
        "lastModified": "2018-07-24T05:42:01Z"
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

This resource archive/unarchive selected course.

### HTTP Request

`PATCH [BASE_URL]/courses/`**uuid**

URI Parameter | Type | Description
--------- | ------- | -----------
uuid | string | The generated UUID of the selected course.

### HTTP Get Parameters

`No HTTP get parameters required.`

### Request Headers
Key | Value | Description
--------- | ------- | -----------
`Content-Type` | **application/json** | Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
`Authorization` | **Bearer $token** | Lorem ipsum dolor sit amet, consectetur adipiscing elit.


### HTTP Post Parameters

`No HTTP post parameters required.`









## Trash Course

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

This resource trash selected course.

### HTTP Request

`DELETE [BASE_URL]/courses/`**uuid**

URI Parameter | Type | Description
--------- | ------- | -----------
uuid | string | The generated UUID of the selected course.

### HTTP Get Parameters

`No HTTP get parameters required.`

### Request Headers
Key | Value | Description
--------- | ------- | -----------
`Content-Type` | **application/json** | Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
`Authorization` | **Bearer $token** | Lorem ipsum dolor sit amet, consectetur adipiscing elit.


### HTTP Post Parameters

`No HTTP post parameters required.`






## Untrash Course

> 200

```json
{
    "data": {
        "id": 2,
        "accountID": 2,
        "ownerID": 2,
        "description": "<p>Sample Description</p>",
        "descriptionIsHTML": true,
        "consumerKeyLTI": "7jaqP8ZSwsAXVfWM3emN",
        "sharedSecretLTI": "pwWjBIslrRoq4vGxhU3f",
        "code": "S-CODE-2",
        "startDate": "2018-08-23T00:00:00Z",
        "endDate": "2018-08-26T00:00:00Z",
        "isPublished": true,
        "configURLLTI": "http://localhost:8041/lti/config/7jaqP8ZSwsAXVfWM3emN",
        "launchURLLTI": "http://localhost:8041/lti/launch/7jaqP8ZSwsAXVfWM3emN",
        "uuid": "d11281dd-8105-4d7a-a56a-9febeb16a215",
        "isArchived": false,
        "isTrashed": false,
        "dateCreated": "2018-07-24T05:32:48Z",
        "lastModified": "2018-07-24T05:42:01Z"
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

This resource untrash trashed course.

### HTTP Request

`GET [BASE_URL]/courses/`**uuid**`/restore`

URI Parameter | Type | Description
--------- | ------- | -----------
uuid | string | The generated UUID of the selected course.

### HTTP Get Parameters

`No HTTP get parameters required.`

### Request Headers
Key | Value | Description
--------- | ------- | -----------
`Content-Type` | **application/json** | Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
`Authorization` | **Bearer $token** | Lorem ipsum dolor sit amet, consectetur adipiscing elit.


### HTTP Post Parameters

`No HTTP post parameters required.`