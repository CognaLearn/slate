# Account Users

<aside class="success">
Resources related to <code>account user management</code>.
</aside>






## List of Account Users

> 200

```json
{
    "data": [
        {
            "account": null,
            "accountUuid": null,
            "identity": "bodwyer",
            "email": "brian@cognalearn.com",
            "firstname": "Brian",
            "lastname": "O’Dwyer",
            "displayName": "",
            "isActive": false,
            "isDeletable": false,
            "roleId": 1,
            "role": "Account Admin",
            "uuid": "06999d47-4dcb-4c9e-9c21-2f88d9c1b06d",
            "isArchived": false,
            "isTrashed": false,
            "dateCreated": null,
            "createBy": null,
            "lastModified": "2018-08-02T05:09:21Z",
            "lastUpdatedBy": null,
            "authorisations": []
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

This resource allows to list all account users.




### HTTP Request

`GET [BASE_URL]/accounts/`**account-uuid**`/account-users/`

URI Parameter | Type | Description
--------- | ------- | -----------
account-uuid | string | The generated UUID of the selected account.

### HTTP Get Parameters

[Standard HTTP Get Parameters](#principles)

`i.e. [BASE_URL]/accounts?page=1&per_page=3`

#### Additional Get Parameters
Parameter | Type | Description
--------- | ------- | -----------
`role` | **int or string** | Role ID or name listed [above](#standard-roles).

### Request Headers
Key | Value | Description
--------- | ------- | -----------
`Content-Type` | **application/json** | Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
`Authorization` | **Bearer $token** | Lorem ipsum dolor sit amet, consectetur adipiscing elit.


### HTTP Post Parameters

`No HTTP post parameters required.`











## Create Account User

> 201

```json
{
    "data": {
        "account": null,
        "accountUuid": null,
        "identity": "bodwyer",
        "email": "brian@cognalearn.com",
        "firstname": "Brian",
        "lastname": "O’Dwyer",
        "displayName": "",
        "isActive": false,
        "isDeletable": false,
        "roleId": 1,
        "role": "Superuser",
        "uuid": "06999d47-4dcb-4c9e-9c21-2f88d9c1b06d",
        "isArchived": false,
        "isTrashed": false,
        "dateCreated": null,
        "createBy": null,
        "lastModified": "2018-08-02T05:09:21Z",
        "lastUpdatedBy": null,
        "authorisations": []
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
    "email": [
      "The email field is required."
    ]
  },
  "status_code": 422
}
```

This resource create new account user.

### HTTP Request

`POST [BASE_URL]/accounts/`**account-uuid**`/account-users/`

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
identity <br /> `required`| **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
email <br /> `required`| **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
firstname <br /> `required`| **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
lastname | **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
accountType <br /> `required`| **enum[string]** <br /> `Admin, Full Access, Read Only` <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
roleId <br /> `required`| **int** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
                

<aside class="info">
When an Account is created, the User receives an invitation email with a link for them to set their password and access their Account.
</aside>



## Retrieve Account User

> 200

```json
{
    "data": {
        "account": null,
        "accountUuid": null,
        "identity": "bodwyer",
        "email": "brian@cognalearn.com",
        "firstname": "Brian",
        "lastname": "O’Dwyer",
        "displayName": "",
        "isActive": false,
        "isDeletable": false,
        "roleId": 1,
        "role": "Superuser",
        "uuid": "06999d47-4dcb-4c9e-9c21-2f88d9c1b06d",
        "isArchived": false,
        "isTrashed": false,
        "dateCreated": null,
        "createBy": null,
        "lastModified": "2018-08-02T05:09:21Z",
        "lastUpdatedBy": null,
        "authorisations": []
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

This resource retrieve specific account user.

### HTTP Request

`GET [BASE_URL]/accounts/`**account-uuid**`/account-users/`**uuid**

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









## Update Account User

> 200

```json
{
    "data": {
        "account": null,
        "accountUuid": null,
        "identity": "bodwyer",
        "email": "brian@cognalearn.com",
        "firstname": "Brian",
        "lastname": "O’Dwyer",
        "displayName": "",
        "isActive": false,
        "isDeletable": false,
        "roleId": 1,
        "role": "Superuser",
        "uuid": "06999d47-4dcb-4c9e-9c21-2f88d9c1b06d",
        "isArchived": false,
        "isTrashed": false,
        "dateCreated": null,
        "createBy": null,
        "lastModified": "2018-08-02T05:09:21Z",
        "lastUpdatedBy": null,
        "authorisations": []
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
    "email": [
      "The email has already been taken."
    ]
  },
  "status_code": 422
}
```

This resource update selected account user.

### HTTP Request

`PUT [BASE_URL]/accounts/`**account-uuid**`/account-users/`**uuid**

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
Parameter | Description
--------- | -----------
identity <br /> `required`| **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
email <br /> `required`| **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
firstname <br /> `required`| **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
lastname | **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
accountType <br /> `required`| **enum[string]** <br /> `Admin, Full Access, Read Only` <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
roleId <br /> `required`| **int** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.






## Archive/Unarchive Account User

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
        "account": null,
        "accountUuid": null,
        "identity": "bodwyer",
        "email": "brian@cognalearn.com",
        "firstname": "Brian",
        "lastname": "O’Dwyer",
        "displayName": "",
        "isActive": false,
        "isDeletable": false,
        "roleId": 1,
        "role": "Superuser",
        "uuid": "06999d47-4dcb-4c9e-9c21-2f88d9c1b06d",
        "isArchived": false,
        "isTrashed": false,
        "dateCreated": null,
        "createBy": null,
        "lastModified": "2018-08-02T05:09:21Z",
        "lastUpdatedBy": null,
        "authorisations": []
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

This resource archive/unarchive selected account user.

### HTTP Request

`PATCH [BASE_URL]/accounts/`**account-uuid**`/account-users/`**uuid**

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









## Trash Account User

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

`DELETE [BASE_URL]/accounts/`**account-uuid**`/account-users/`**uuid**

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






## Untrash Account User

> 200

```json
{
    "data": {
        "account": null,
        "accountUuid": null,
        "identity": "bodwyer",
        "email": "brian@cognalearn.com",
        "firstname": "Brian",
        "lastname": "O’Dwyer",
        "displayName": "",
        "isActive": false,
        "isDeletable": false,
        "roleId": 1,
        "role": "Superuser",
        "uuid": "06999d47-4dcb-4c9e-9c21-2f88d9c1b06d",
        "isArchived": false,
        "isTrashed": false,
        "dateCreated": null,
        "createBy": null,
        "lastModified": "2018-08-02T05:09:21Z",
        "lastUpdatedBy": null,
        "authorisations": []
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

`GET [BASE_URL]/accounts/`**account-uuid**`/account-users/`**uuid**`/restore`

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