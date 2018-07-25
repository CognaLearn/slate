# Modules

<aside class="success">
Resources related to <code>module management</code>.
</aside>






## List

> 200

```json
{
    "data": [
        {
            "id": 2,
            "accountID": 2,
            "courseID": 2,
            "ownerID": 2,
            "description": "<p>Sample Description</p>",
            "descriptionIsHTML": true,
            "startDate": "2018-07-23T00:00:00Z",
            "endDate": "2018-07-26T00:00:00Z",
            "isPublished": true,
            "uuid": "9050ff6f-ca67-4022-8552-57dc94f4533c",
            "isArchived": false,
            "isTrashed": false,
            "dateCreated": "2018-07-25T13:38:18Z",
            "lastModified": "2018-07-25T13:53:45Z"
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

This resource allows to list all modules.




### HTTP Request

`GET [BASE_URL]/modules`

### HTTP Get Parameters

[Standard HTTP Get Parameters](#principles)

`i.e. [BASE_URL]/modules?page=1&per_page=3`

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
        "id": 2,
        "accountID": 2,
        "ownerID": 2,
        "description": "<p>Sample Description</p>",
        "descriptionIsHTML": true,
        "startDate": "2018-07-23T00:00:00Z",
        "endDate": "2018-07-26T00:00:00Z",
        "isPublished": false,
        "uuid": "9050ff6f-ca67-4022-8552-57dc94f4533c",
        "isArchived": false,
        "isTrashed": false,
        "dateCreated": "2018-07-25T13:38:18Z",
        "lastModified": "2018-07-25T13:38:18Z"
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

This resource create new module.

### HTTP Request

`POST [BASE_URL]/modules`

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
courseId <br /> `required`| **string** <br /> Selected course UUID.
startDate <br /> `required`| **date** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
endDate <br /> `required`| **date** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
description| **json** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.





## Retrieve

> 200

```json
{
    "data": {
        "id": 2,
        "accountID": 2,
        "courseID": 2,
        "ownerID": 2,
        "description": "<p>Sample Description</p>",
        "descriptionIsHTML": true,
        "startDate": "2018-07-23T00:00:00Z",
        "endDate": "2018-07-26T00:00:00Z",
        "isPublished": true,
        "uuid": "9050ff6f-ca67-4022-8552-57dc94f4533c",
        "isArchived": false,
        "isTrashed": false,
        "dateCreated": "2018-07-25T13:38:18Z",
        "lastModified": "2018-07-25T13:38:18Z"
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

This resource retrieve specific module.

### HTTP Request

`GET [BASE_URL]/modules/`**uuid**

### HTTP Get Parameters

Parameter | Type | Description
--------- | ------- | -----------
uuid | string | The generated UUID of the selected module.

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
        "id": 2,
        "accountID": 2,
        "courseID": 2,
        "ownerID": 2,
        "description": "<p>Sample Description</p>",
        "descriptionIsHTML": true,
        "startDate": "2018-07-23T00:00:00Z",
        "endDate": "2018-07-26T00:00:00Z",
        "isPublished": true,
        "uuid": "9050ff6f-ca67-4022-8552-57dc94f4533c",
        "isArchived": false,
        "isTrashed": false,
        "dateCreated": "2018-07-25T13:38:18Z",
        "lastModified": "2018-07-25T13:50:30Z"
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

This resource update selected module.

### HTTP Request

`PUT [BASE_URL]/modules/`**uuid**

### HTTP Get Parameters

Parameter | Type | Description
--------- | ------- | -----------
uuid | string | The generated UUID of the selected module.

### Request Headers
Key | Value | Description
--------- | ------- | -----------
`Content-Type` | **application/json** | Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
`Authorization` | **Bearer $token** | Lorem ipsum dolor sit amet, consectetur adipiscing elit.


### HTTP Post Parameters
Parameter | Description
--------- | -----------
name <br /> `required`| **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
courseId <br /> `required`| **string** <br /> Selected course UUID.
startDate <br /> `required`| **date** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
endDate <br /> `required`| **date** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
description| **json** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.









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
        "id": 2,
        "accountID": 2,
        "courseID": 2,
        "ownerID": 2,
        "description": "<p>Sample Description</p>",
        "descriptionIsHTML": true,
        "startDate": "2018-07-23T00:00:00Z",
        "endDate": "2018-07-26T00:00:00Z",
        "isPublished": true,
        "uuid": "9050ff6f-ca67-4022-8552-57dc94f4533c",
        "isArchived": false,
        "isTrashed": false,
        "dateCreated": "2018-07-25T13:38:18Z",
        "lastModified": "2018-07-25T13:50:30Z"
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

This resource archive/unarchive selected module.

### HTTP Request

`PATCH [BASE_URL]/modules/`**uuid**

### HTTP Get Parameters

Parameter | Type | Description
--------- | ------- | -----------
uuid | string | The generated UUID of the selected module.

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

This resource trash selected module.

### HTTP Request

`DELETE [BASE_URL]/modules/`**uuid**

### HTTP Get Parameters

Parameter | Type | Description
--------- | ------- | -----------
uuid | string | The generated UUID of the selected module.

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
        "id": 2,
        "accountID": 2,
        "courseID": 2,
        "ownerID": 2,
        "description": "<p>Sample Description</p>",
        "descriptionIsHTML": true,
        "startDate": "2018-07-23T00:00:00Z",
        "endDate": "2018-07-26T00:00:00Z",
        "isPublished": true,
        "uuid": "9050ff6f-ca67-4022-8552-57dc94f4533c",
        "isArchived": false,
        "isTrashed": false,
        "dateCreated": "2018-07-25T13:38:18Z",
        "lastModified": "2018-07-25T13:50:30Z"
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

This resource untrash trashed module.

### HTTP Request

`GET [BASE_URL]/modules/`**uuid**`/restore`

### HTTP Get Parameters

Parameter | Type | Description
--------- | ------- | -----------
uuid | string | The generated UUID of the selected module.

### Request Headers
Key | Value | Description
--------- | ------- | -----------
`Content-Type` | **application/json** | Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
`Authorization` | **Bearer $token** | Lorem ipsum dolor sit amet, consectetur adipiscing elit.


### HTTP Post Parameters

`No HTTP post parameters required.`