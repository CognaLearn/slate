# Users

<aside class="success">
Resources related to <code>user management</code>.
</aside>






## List of Users

> 200

```json
{
    "data": [
        {
            "account": null,
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

This resource allows to list all users.




### HTTP Request

`GET [BASE_URL]/users`

### HTTP Get Parameters

[Standard HTTP Get Parameters](#principles)

`i.e. [BASE_URL]/users?page=1&per_page=3`

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











## Create User

> 201

```json
{
    "data": {
        "id": 2,
        "userName": "sample-user",
        "organisationName": "Sample User",
        "paymentMethod": "Free",
        "type": "Free",
        "isActive": false,
        "isPaid": false,
        "isGeneric": false,
        "expiryDate": null,
        "dateExpired": null,
        "uuid": "5355b648-e5bb-4639-b868-b455be661318",
        "isArchived": false,
        "isTrashed": false,
        "dateCreated": "2018-07-23T09:34:52Z",
        "lastModified": "2018-07-23T09:34:52Z",
        "userAdmins": [
            {
                "uuid": "51a66105-ac8f-4c85-99e2-38104acdd93a",
                "identity": "mbsoliven",
                "displayName": "Michael Angelo Soliven"
            }
        ]
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


> 422

```json
{
  "message": "422 Unprocessable Entity",
  "errors": {
    "identity": [
      "The identity field is required."
    ]
  },
  "status_code": 422
}
```

This resource create new user.

### HTTP Request

`POST [BASE_URL]/users`

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
roleId <br /> `required`| **int** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
accountUuid <br /> `required if roleId != 1`| **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
password | **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
password_confirmation <br /> `required if isset(password)`| **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.                

<aside class="notice">
If <code>password</code> is not provided, activation link will be sent to the email.
</aside>

## Retrieve User

> 200

```json
{
    "data": {
        "account": null,
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

This resource retrieve specific user.

### HTTP Request

`GET [BASE_URL]/users/`**uuid**

### HTTP Get Parameters

Parameter | Type | Description
--------- | ------- | -----------
uuid | string | The generated UUID of the selected user.

### Request Headers
Key | Value | Description
--------- | ------- | -----------
`Content-Type` | **application/json** | Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
`Authorization` | **Bearer $token** | Lorem ipsum dolor sit amet, consectetur adipiscing elit.


### HTTP Post Parameters

`No HTTP post parameters required.`









## Update User

> 200

```json
{
    "data": {
        "id": 2,
        "userName": "sample-user",
        "organisationName": "Sample User",
        "paymentMethod": "Free",
        "type": "Free",
        "isActive": false,
        "isPaid": false,
        "isGeneric": false,
        "expiryDate": null,
        "dateExpired": null,
        "uuid": "5355b648-e5bb-4639-b868-b455be661318",
        "isArchived": false,
        "isTrashed": false,
        "dateCreated": "2018-07-23T09:34:52Z",
        "lastModified": "2018-07-23T09:34:52Z",
        "userAdmins": [
            {
                "uuid": "51a66105-ac8f-4c85-99e2-38104acdd93a",
                "identity": "mbsoliven",
                "displayName": "Michael Angelo Soliven"
            }
        ]
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
    "accountUuid": [
      "The account uuid field is required."
    ]
  },
  "status_code": 422
}
```

This resource update selected user.

### HTTP Request

`PUT [BASE_URL]/users/`**uuid**

### HTTP Get Parameters

Parameter | Type | Description
--------- | ------- | -----------
uuid | string | The generated UUID of the selected user.

### Request Headers
Key | Value | Description
--------- | ------- | -----------
`Content-Type` | **application/json** | Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
`Authorization` | **Bearer $token** | Lorem ipsum dolor sit amet, consectetur adipiscing elit.


### HTTP Post Parameters
Parameter | Description
--------- | -----------
identity | **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
email | **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
firstname | **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
roleId | **int** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
accountUuid <br /> `required if roleId != 1`| **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
password | **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
password_confirmation <br /> `required if isset(password)`| **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
isActive | **boolean** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.






## Archive/Unarchive User

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
        "identity": "accountadmin3",
        "email": "accountadmin3@gmail.com",
        "firstname": "Super User 2",
        "lastname": null,
        "displayName": "Account Admin 3",
        "isActive": false,
        "isDeletable": true,
        "roleId": 2,
        "role": "Account Admin",
        "uuid": "4e4062a0-ee60-4612-88a3-aa9075d4028a",
        "isArchived": false,
        "isTrashed": false,
        "dateCreated": "2018-08-01T10:00:22Z",
        "createBy": "Brian O’Dwyer",
        "lastModified": "2018-08-02T06:12:00Z",
        "lastUpdatedBy": "Brian O’Dwyer",
        "authorisations": [
            "App\\Http\\Controllers\\RouterController@index",
            "App\\Http\\Controllers\\UserController@index",
            "App\\Http\\Controllers\\UserController@store",
            "App\\Http\\Controllers\\UserController@show",
            "App\\Http\\Controllers\\UserController@update",
            "App\\Http\\Controllers\\UserController@archive",
            "App\\Http\\Controllers\\UserController@destroy",
            "App\\Http\\Controllers\\UserController@restore"
        ]
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

This resource archive/unarchive selected user.

### HTTP Request

`PATCH [BASE_URL]/users/`**uuid**

### HTTP Get Parameters

Parameter | Type | Description
--------- | ------- | -----------
uuid | string | The generated UUID of the selected user.

### Request Headers
Key | Value | Description
--------- | ------- | -----------
`Content-Type` | **application/json** | Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
`Authorization` | **Bearer $token** | Lorem ipsum dolor sit amet, consectetur adipiscing elit.


### HTTP Post Parameters

`No HTTP post parameters required.`









## Trash User

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

This resource trash selected user.

### HTTP Request

`DELETE [BASE_URL]/users/`**uuid**

### HTTP Get Parameters

Parameter | Type | Description
--------- | ------- | -----------
uuid | string | The generated UUID of the selected user.

### Request Headers
Key | Value | Description
--------- | ------- | -----------
`Content-Type` | **application/json** | Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
`Authorization` | **Bearer $token** | Lorem ipsum dolor sit amet, consectetur adipiscing elit.


### HTTP Post Parameters

`No HTTP post parameters required.`






## Untrash User

> 200

```json
{
    "data": {
        "account": null,
        "identity": "accountadmin3",
        "email": "accountadmin3@gmail.com",
        "firstname": "Super User 2",
        "lastname": null,
        "displayName": "Account Admin 3",
        "isActive": false,
        "isDeletable": true,
        "roleId": 2,
        "role": "Account Admin",
        "uuid": "4e4062a0-ee60-4612-88a3-aa9075d4028a",
        "isArchived": false,
        "isTrashed": false,
        "dateCreated": "2018-08-01T10:00:22Z",
        "createBy": "Brian O’Dwyer",
        "lastModified": "2018-08-02T06:12:35Z",
        "lastUpdatedBy": "Brian O’Dwyer",
        "authorisations": [
            "App\\Http\\Controllers\\RouterController@index",
            "App\\Http\\Controllers\\UserController@index",
            "App\\Http\\Controllers\\UserController@store",
            "App\\Http\\Controllers\\UserController@show",
            "App\\Http\\Controllers\\UserController@update",
            "App\\Http\\Controllers\\UserController@archive",
            "App\\Http\\Controllers\\UserController@destroy",
            "App\\Http\\Controllers\\UserController@restore"
        ]
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

This resource untrash trashed user.

### HTTP Request

`GET [BASE_URL]/users/`**uuid**`/restore`

### HTTP Get Parameters

Parameter | Type | Description
--------- | ------- | -----------
uuid | string | The generated UUID of the selected user.

### Request Headers
Key | Value | Description
--------- | ------- | -----------
`Content-Type` | **application/json** | Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
`Authorization` | **Bearer $token** | Lorem ipsum dolor sit amet, consectetur adipiscing elit.


### HTTP Post Parameters

`No HTTP post parameters required.`