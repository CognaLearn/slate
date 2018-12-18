# Account Courses

<aside class="success">
Resources related to <code>account course management</code>.
</aside>






## List of Account Courses

> 200

```json
{
    "data": [
        {
            "id": 1,
            "accountID": 1,
            "ownerID": 3,
            "description": "<p>Sample Description 1</p>",
            "descriptionIsHTML": true,
            "consumerKeyLTI": "265szBZ0YnjwmeEqhpul",
            "sharedSecretLTI": "uN62UIfapkV0dGS3BlMO",
            "code": "S-CODE-1",
            "startDate": "2018-08-23T00:00:00Z",
            "endDate": "2018-08-26T00:00:00Z",
            "isPublished": true,
            "objectives": null,
            "configURLLTI": "http://localhost:8041/lti/config/265szBZ0YnjwmeEqhpul",
            "launchURLLTI": "http://localhost:8041/lti/launch/265szBZ0YnjwmeEqhpul",
            "uuid": "f5a17fa7-f4b7-4b27-ab1b-83b9664506a2",
            "isArchived": false,
            "isTrashed": false,
            "dateCreated": "2018-08-13T08:11:20Z",
            "lastModified": "2018-08-13T09:01:30Z"
        },
        {
            "id": 2,
            "accountID": 1,
            "ownerID": 3,
            "description": "<p>Sample Description 2</p>",
            "descriptionIsHTML": true,
            "consumerKeyLTI": "FjGbsnkwLX6rJEdOgSlP",
            "sharedSecretLTI": "sULwpxMqHCInE3Vg8tXl",
            "code": "S-CODE-2",
            "startDate": "2018-07-23T00:00:00Z",
            "endDate": "2018-07-26T00:00:00Z",
            "isPublished": true,
            "objectives": null,
            "configURLLTI": "http://localhost:8041/lti/config/FjGbsnkwLX6rJEdOgSlP",
            "launchURLLTI": "http://localhost:8041/lti/launch/FjGbsnkwLX6rJEdOgSlP",
            "uuid": "dfa75ed5-5b69-4c27-8923-3a1250106ca5",
            "isArchived": false,
            "isTrashed": false,
            "dateCreated": "2018-08-14T03:08:39Z",
            "lastModified": "2018-08-14T03:08:39Z"
        }
    ],
    "meta": {
        "pagination": {
            "total": 2,
            "count": 2,
            "per_page": 10,
            "current_page": 1,
            "total_pages": 1,
            "links": []
        }
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

> 403

```json
{
  "error": {
    "message": [
      "Permission denied.",
      "Ownership denied."
    ],
    "status_code": 403
  }
}
```

This resource allows to list all account courses.




### HTTP Request

`GET [BASE_URL]/accounts/`**account-uuid**`/accounts-courses/`

URI Parameter | Type | Description
--------- | ------- | -----------
account-uuid | string | The generated UUID of the selected account.

### HTTP Get Parameters

[Standard HTTP Get Parameters](#principles)

`i.e. [BASE_URL]/accounts?page=1&per_page=3`

### Request Headers
Key | Value | Description
--------- | ------- | -----------
`Content-Type` | **application/json** | Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
`Authorization` | **Bearer $token** | Lorem ipsum dolor sit amet, consectetur adipiscing elit.


### HTTP Post Parameters

`No HTTP post parameters required.`











## Create Account Course

> 201

```json
{
    "data": {
        "id": 1,
        "accountID": 1,
        "ownerID": 3,
        "description": "<p>Sample Description 1</p>",
        "descriptionIsHTML": true,
        "consumerKeyLTI": "265szBZ0YnjwmeEqhpul",
        "sharedSecretLTI": "uN62UIfapkV0dGS3BlMO",
        "code": "S-CODE-1",
        "startDate": "2018-08-23T00:00:00Z",
        "endDate": "2018-08-26T00:00:00Z",
        "isPublished": true,
        "objectives": null,
        "configURLLTI": "http://localhost:8041/lti/config/265szBZ0YnjwmeEqhpul",
        "launchURLLTI": "http://localhost:8041/lti/launch/265szBZ0YnjwmeEqhpul",
        "uuid": "f5a17fa7-f4b7-4b27-ab1b-83b9664506a2",
        "isArchived": false,
        "isTrashed": false,
        "dateCreated": "2018-08-13T08:11:20Z",
        "lastModified": "2018-08-13T09:01:30Z"
    }
}
```

> 403

```json
{
  "error": {
    "message": [
      "Permission denied.",
      "Ownership denied."
    ],
    "status_code": 403
  }
}
```

> 422

```json
{
  "message": "422 Unprocessable Entity",
  "errors": {
    "name": [
      "The name field is required."
    ]
  },
  "status_code": 422
}
```

This resource create new account course.

### HTTP Request

`POST [BASE_URL]/accounts/`**account-uuid**`/accounts-courses/`

URI Parameter | Type | Description
--------- | ------- | -----------
account-uuid | string | The generated UUID of the selected account.

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
code| **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
startDate <br /> `required`| **date** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
endDate <br /> `required`| **date** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
description| **json** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
objectives| **json** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
                

<aside class="info">
Teachers who create Courses are known as the Course Admin Teacher for that Course.
</aside>



## Retrieve Account Course

> 200

```json
{
    "data": {
        "id": 1,
        "accountID": 1,
        "ownerID": 3,
        "description": "<p>Sample Description 1</p>",
        "descriptionIsHTML": true,
        "consumerKeyLTI": "265szBZ0YnjwmeEqhpul",
        "sharedSecretLTI": "uN62UIfapkV0dGS3BlMO",
        "code": "S-CODE-1",
        "startDate": "2018-08-23T00:00:00Z",
        "endDate": "2018-08-26T00:00:00Z",
        "isPublished": true,
        "objectives": null,
        "configURLLTI": "http://localhost:8041/lti/config/265szBZ0YnjwmeEqhpul",
        "launchURLLTI": "http://localhost:8041/lti/launch/265szBZ0YnjwmeEqhpul",
        "uuid": "f5a17fa7-f4b7-4b27-ab1b-83b9664506a2",
        "isArchived": false,
        "isTrashed": false,
        "dateCreated": "2018-08-13T08:11:20Z",
        "lastModified": "2018-08-13T09:01:30Z"
    }
}
```

> 403

```json
{
  "error": {
    "message": [
      "Permission denied.",
      "Ownership denied."
    ],
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

This resource retrieve specific account course.

### HTTP Request

`GET [BASE_URL]/accounts/`**account-uuid**`/account-courses/`**uuid**

URI Parameter | Type | Description
--------- | ------- | -----------
account-uuid | string | The generated UUID of the selected account.
uuid | string | The generated UUID of the selected account course.

### HTTP Get Parameters

`No HTTP get parameters required.`

### Request Headers
Key | Value | Description
--------- | ------- | -----------
`Content-Type` | **application/json** | Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
`Authorization` | **Bearer $token** | Lorem ipsum dolor sit amet, consectetur adipiscing elit.


### HTTP Post Parameters

`No HTTP post parameters required.`









## Update Account Course

> 200

```json
{
    "data": {
        "id": 1,
        "accountID": 1,
        "ownerID": 3,
        "description": "<p>Sample Description</p>",
        "descriptionIsHTML": true,
        "consumerKeyLTI": "265szBZ0YnjwmeEqhpul",
        "sharedSecretLTI": "uN62UIfapkV0dGS3BlMO",
        "code": "S-CODE-1",
        "startDate": "2018-08-23T00:00:00Z",
        "endDate": "2018-08-26T00:00:00Z",
        "isPublished": true,
        "objectives": null,
        "configURLLTI": "http://localhost:8041/lti/config/265szBZ0YnjwmeEqhpul",
        "launchURLLTI": "http://localhost:8041/lti/launch/265szBZ0YnjwmeEqhpul",
        "uuid": "f5a17fa7-f4b7-4b27-ab1b-83b9664506a2",
        "isArchived": false,
        "isTrashed": false,
        "dateCreated": "2018-08-13T08:11:20Z",
        "lastModified": "2018-08-14T03:44:32Z"
    }
}
```

> 403

```json
{
  "error": {
    "message": [
      "Permission denied.",
      "Ownership denied."
    ],
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
    "code": [
      "The code has already been taken."
    ]
  },
  "status_code": 422
}
```

This resource update selected account course.

### HTTP Request

`PUT [BASE_URL]/accounts/`**account-uuid**`/account-courses/`**uuid**

URI Parameter | Type | Description
--------- | ------- | -----------
account-uuid | string | The generated UUID of the selected account.
uuid | string | The generated UUID of the selected account course.

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
code| **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
startDate <br /> `required`| **date** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
endDate <br /> `required`| **date** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
description| **json** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
objectives| **json** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
isPublished| **boolen** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.






## Archive/Unarchive Account Course

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
        "id": 1,
        "accountID": 1,
        "ownerID": 3,
        "description": "<p>Sample Description</p>",
        "descriptionIsHTML": true,
        "consumerKeyLTI": "265szBZ0YnjwmeEqhpul",
        "sharedSecretLTI": "uN62UIfapkV0dGS3BlMO",
        "code": "S-CODE-1",
        "startDate": "2018-08-23T00:00:00Z",
        "endDate": "2018-08-26T00:00:00Z",
        "isPublished": true,
        "objectives": null,
        "configURLLTI": "http://localhost:8041/lti/config/265szBZ0YnjwmeEqhpul",
        "launchURLLTI": "http://localhost:8041/lti/launch/265szBZ0YnjwmeEqhpul",
        "uuid": "f5a17fa7-f4b7-4b27-ab1b-83b9664506a2",
        "isArchived": false,
        "isTrashed": false,
        "dateCreated": "2018-08-13T08:11:20Z",
        "lastModified": "2018-08-14T03:44:32Z"
    }
}
```


> 403

```json
{
  "error": {
    "message": [
      "Permission denied.",
      "Ownership denied."
    ],
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

This resource archive/unarchive selected account course.

### HTTP Request

`PATCH [BASE_URL]/accounts/`**account-uuid**`/account-courses/`**uuid**

URI Parameter | Type | Description
--------- | ------- | -----------
account-uuid | string | The generated UUID of the selected account.
uuid | string | The generated UUID of the selected account course.

### HTTP Get Parameters

`No HTTP get parameters required.`

### Request Headers
Key | Value | Description
--------- | ------- | -----------
`Content-Type` | **application/json** | Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
`Authorization` | **Bearer $token** | Lorem ipsum dolor sit amet, consectetur adipiscing elit.


### HTTP Post Parameters

`No HTTP post parameters required.`









## Trash Account Course

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
    "message": [
      "Permission denied.",
      "Ownership denied."
    ],
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

This resource trash selected account user.

### HTTP Request

`DELETE [BASE_URL]/accounts/`**account-uuid**`/account-courses/`**uuid**

URI Parameter | Type | Description
--------- | ------- | -----------
account-uuid | string | The generated UUID of the selected account.
uuid | string | The generated UUID of the selected account course.

### HTTP Get Parameters

`No HTTP get parameters required.`

### Request Headers
Key | Value | Description
--------- | ------- | -----------
`Content-Type` | **application/json** | Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
`Authorization` | **Bearer $token** | Lorem ipsum dolor sit amet, consectetur adipiscing elit.


### HTTP Post Parameters

`No HTTP post parameters required.`






## Untrash Account Course

> 200

```json
{
    "data": {
        "id": 1,
        "accountID": 1,
        "ownerID": 3,
        "description": "<p>Sample Description</p>",
        "descriptionIsHTML": true,
        "consumerKeyLTI": "265szBZ0YnjwmeEqhpul",
        "sharedSecretLTI": "uN62UIfapkV0dGS3BlMO",
        "code": "S-CODE-1",
        "startDate": "2018-08-23T00:00:00Z",
        "endDate": "2018-08-26T00:00:00Z",
        "isPublished": true,
        "objectives": null,
        "configURLLTI": "http://localhost:8041/lti/config/265szBZ0YnjwmeEqhpul",
        "launchURLLTI": "http://localhost:8041/lti/launch/265szBZ0YnjwmeEqhpul",
        "uuid": "f5a17fa7-f4b7-4b27-ab1b-83b9664506a2",
        "isArchived": false,
        "isTrashed": false,
        "dateCreated": "2018-08-13T08:11:20Z",
        "lastModified": "2018-08-14T03:44:32Z"
    }
}
```

> 403

```json
{
  "error": {
    "message": [
      "Permission denied.",
      "Ownership denied."
    ],
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

This resource untrash trashed account user.

### HTTP Request

`GET [BASE_URL]/accounts/`**account-uuid**`/account-courses/`**uuid**`/restore`

URI Parameter | Type | Description
--------- | ------- | -----------
account-uuid | string | The generated UUID of the selected account.
uuid | string | The generated UUID of the selected account user.

### HTTP Get Parameters

`No HTTP get parameters required.`

### Request Headers
Key | Value | Description
--------- | ------- | -----------
`Content-Type` | **application/json** | Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
`Authorization` | **Bearer $token** | Lorem ipsum dolor sit amet, consectetur adipiscing elit.


### HTTP Post Parameters

`No HTTP post parameters required.`