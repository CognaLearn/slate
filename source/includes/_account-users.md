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
            "id": 2,
            "accountName": "sample-account",
            "organisationName": "Sample Account",
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
            "accountAdmins": [
                {
                    "uuid": "51a66105-ac8f-4c85-99e2-38104acdd93a",
                    "identity": "mbsoliven",
                    "displayName": "Michael Angelo Soliven"
                }
            ]
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

This resource allows to list all account users.




### HTTP Request

`GET [BASE_URL]/accounts/`**account-uuid**

URI Parameter | Type | Description
--------- | ------- | -----------
account-uuid | string | The generated UUID of the selected user.

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
        "id": 2,
        "accountName": "sample-account",
        "organisationName": "Sample Account",
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
        "accountAdmins": [
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
    "account": [
      "The account field is required."
    ]
  },
  "status_code": 422
}
```

This resource create new account user.

### HTTP Request

`POST [BASE_URL]/accounts`

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
accountName <br /> `required`| **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
organisationName <br /> `required`| **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
paymentMethod <br /> `required`| **enum[string]** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
type <br /> `required`| **enum[string]** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
firstname <br /> `required`| **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
lastname | **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
identity <br /> `required`| **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
email <br /> `required`| **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
                

<aside class="info">
When an Account is created by a Superuser and the Admin Teacher is created, the Admin Teacher receives an invitation email with a link for them to set their password and access their Account.
</aside>



## Retrieve Account User

> 200

```json
{
    "data": {
        "id": 2,
        "accountName": "sample-account",
        "organisationName": "Sample Account",
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
        "accountAdmins": [
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

This resource retrieve specific account user.

### HTTP Request

`GET [BASE_URL]/accounts/`**uuid**

### HTTP Get Parameters

Parameter | Type | Description
--------- | ------- | -----------
uuid | string | The generated UUID of the selected account user.

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
        "id": 2,
        "accountName": "sample-account",
        "organisationName": "Sample Account",
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
        "accountAdmins": [
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
    "identity": [
      "The account field is required."
    ]
  },
  "status_code": 422
}
```

This resource update selected account user.

### HTTP Request

`PUT [BASE_URL]/accounts/`**uuid**

### HTTP Get Parameters

Parameter | Type | Description
--------- | ------- | -----------
uuid | string | The generated UUID of the selected account user.

### Request Headers
Key | Value | Description
--------- | ------- | -----------
`Content-Type` | **application/json** | Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
`Authorization` | **Bearer $token** | Lorem ipsum dolor sit amet, consectetur adipiscing elit.


### HTTP Post Parameters
Parameter | Description
--------- | -----------
accountName <br /> `required`| **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
organisationName <br /> `required`| **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
paymentMethod <br /> `required`| **enum[string]** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
type <br /> `required`| **enum[string]** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
isActive| **boolean** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
isPaid| **boolean** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
isGeneric| **boolean** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
expiryDate | **date** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.






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
        "id": 2,
        "accountName": "sample-account",
        "organisationName": "Sample Account",
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
        "accountAdmins": [
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

This resource archive/unarchive selected account user.

### HTTP Request

`PATCH [BASE_URL]/accounts/`**uuid**

### HTTP Get Parameters

Parameter | Type | Description
--------- | ------- | -----------
uuid | string | The generated UUID of the selected account user.

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

This resource trash selected account user.

### HTTP Request

`DELETE [BASE_URL]/accounts/`**uuid**

### HTTP Get Parameters

Parameter | Type | Description
--------- | ------- | -----------
uuid | string | The generated UUID of the selected account user.

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
        "id": 2,
        "accountName": "sample-account",
        "organisationName": "Sample Account",
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
        "accountAdmins": [
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

This resource untrash trashed account user.

### HTTP Request

`GET [BASE_URL]/accounts/`**uuid**`/restore`

### HTTP Get Parameters

Parameter | Type | Description
--------- | ------- | -----------
uuid | string | The generated UUID of the selected account user.

### Request Headers
Key | Value | Description
--------- | ------- | -----------
`Content-Type` | **application/json** | Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
`Authorization` | **Bearer $token** | Lorem ipsum dolor sit amet, consectetur adipiscing elit.


### HTTP Post Parameters

`No HTTP post parameters required.`