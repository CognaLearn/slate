# Accounts

<aside class="success">
Resources related to <code>account management</code>.
</aside>






## List of Accounts

> 200

```json
{
    "data": [
        {
            "id": 1,
            "accountName": "sample-account1",
            "organisationName": "Sample Account 1",
            "paymentMethod": "Free",
            "type": "Free",
            "isActive": false,
            "isPaid": false,
            "isGeneric": false,
            "expiryDate": null,
            "dateExpired": null,
            "uuid": "04a11db6-2f52-41fe-840d-b1f8662e674b",
            "isArchived": false,
            "isTrashed": false,
            "dateCreated": "2018-08-07T05:57:06Z",
            "lastModified": "2018-08-07T05:57:06Z",
            "accountAdmins": [
                {
                    "uuid": "a6d4634d-9ba4-4a72-a69b-8ddd26f362aa",
                    "identity": "mbsoliven",
                    "email": "ninomichaelangelosoliven@gmail.com",
                    "firstname": "Michael Angelo",
                    "lastname": "Soliven",
                    "displayName": "Michael Angelo Soliven"
                },
                {
                    "uuid": "8646c8d4-f0e0-4f2a-abb0-6d782167901f",
                    "identity": "jseet",
                    "email": "jolene@intedashboard.com",
                    "firstname": "Joleen",
                    "lastname": "Seet",
                    "displayName": "Joleen"
                }
            ]
        },
        {
            "id": 20,
            "accountName": "sample-account2",
            "organisationName": "Sample Account 2",
            "paymentMethod": "Free",
            "type": "Free",
            "isActive": false,
            "isPaid": false,
            "isGeneric": false,
            "expiryDate": null,
            "dateExpired": null,
            "uuid": "45c69f06-edb2-4533-9dcd-a028ee1752b6",
            "isArchived": false,
            "isTrashed": false,
            "dateCreated": "2018-08-07T08:54:15Z",
            "lastModified": "2018-08-07T08:54:15Z",
            "accountAdmins": [
                {
                    "uuid": "b2601c58-f7eb-47fb-8c47-390389731bd9",
                    "identity": "mbsoliven2",
                    "email": "ninomichaelangelosoliven2@gmail.com",
                    "firstname": "Michael Angelo 2",
                    "lastname": "Soliven",
                    "displayName": "Michael Angelo 2 Soliven"
                }
            ]
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

> 403

```json
{
  "error": {
    "message": "Permission denied.",
    "status_code": 403
  }
}
```

This resource allows to list all accounts.




### HTTP Request

`GET [BASE_URL]/accounts`

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











## Create Account

> 201

```json
{
    "data": {
        "id": 1,
        "accountName": "sample-account1",
        "organisationName": "Sample Account 1",
        "paymentMethod": "Free",
        "type": "Free",
        "isActive": false,
        "isPaid": false,
        "isGeneric": false,
        "expiryDate": null,
        "dateExpired": null,
        "uuid": "04a11db6-2f52-41fe-840d-b1f8662e674b",
        "isArchived": false,
        "isTrashed": false,
        "dateCreated": "2018-08-07T05:57:06Z",
        "lastModified": "2018-08-07T05:57:06Z",
        "accountAdmins": [
            {
                "uuid": "a6d4634d-9ba4-4a72-a69b-8ddd26f362aa",
                "identity": "mbsoliven",
                "email": "ninomichaelangelosoliven@gmail.com",
                "firstname": "Michael Angelo",
                "lastname": "Soliven",
                "displayName": "Michael Angelo Soliven"
            },
            {
                "uuid": "8646c8d4-f0e0-4f2a-abb0-6d782167901f",
                "identity": "jseet",
                "email": "jolene@intedashboard.com",
                "firstname": "Joleen",
                "lastname": "Seet",
                "displayName": "Joleen"
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

This resource create new account.

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
paymentMethod <br /> `required`| **enum[string]** <br /> `Demo, Trial, Paid, Free` <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
type <br /> `required`| **enum[string]** <br /> `Institution, Student-paid, Free` <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
firstname <br /> `required`| **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
lastname | **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
identity <br /> `required`| **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
email <br /> `required`| **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
                

<aside class="info">
When an Account is created by a Superuser and the Admin Teacher is created, the Admin Teacher receives an invitation email with a link for them to set their password and access their Account.
</aside>



## Retrieve Account

> 200

```json
{
    "data": {
        "id": 1,
        "accountName": "sample-account1",
        "organisationName": "Sample Account 1",
        "paymentMethod": "Free",
        "type": "Free",
        "isActive": false,
        "isPaid": false,
        "isGeneric": false,
        "expiryDate": null,
        "dateExpired": null,
        "uuid": "04a11db6-2f52-41fe-840d-b1f8662e674b",
        "isArchived": false,
        "isTrashed": false,
        "dateCreated": "2018-08-07T05:57:06Z",
        "lastModified": "2018-08-07T05:57:06Z",
        "accountAdmins": [
            {
                "uuid": "a6d4634d-9ba4-4a72-a69b-8ddd26f362aa",
                "identity": "mbsoliven",
                "email": "ninomichaelangelosoliven@gmail.com",
                "firstname": "Michael Angelo",
                "lastname": "Soliven",
                "displayName": "Michael Angelo Soliven"
            },
            {
                "uuid": "8646c8d4-f0e0-4f2a-abb0-6d782167901f",
                "identity": "jseet",
                "email": "jolene@intedashboard.com",
                "firstname": "Joleen",
                "lastname": "Seet",
                "displayName": "Joleen"
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

This resource retrieve specific account.

### HTTP Request

`GET [BASE_URL]/accounts/`**uuid**

URI Parameter | Type | Description
--------- | ------- | -----------
uuid | string | The generated UUID of the selected account.

### HTTP Get Parameters

`No HTTP get parameters required.`

### Request Headers
Key | Value | Description
--------- | ------- | -----------
`Content-Type` | **application/json** | Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
`Authorization` | **Bearer $token** | Lorem ipsum dolor sit amet, consectetur adipiscing elit.


### HTTP Post Parameters

`No HTTP post parameters required.`









## Update Account

> 200

```json
{
    "data": {
        "id": 1,
        "accountName": "sample-account1",
        "organisationName": "Sample Account 1",
        "paymentMethod": "Free",
        "type": "Free",
        "isActive": false,
        "isPaid": false,
        "isGeneric": false,
        "expiryDate": null,
        "dateExpired": null,
        "uuid": "04a11db6-2f52-41fe-840d-b1f8662e674b",
        "isArchived": false,
        "isTrashed": false,
        "dateCreated": "2018-08-07T05:57:06Z",
        "lastModified": "2018-08-07T05:57:06Z",
        "accountAdmins": [
            {
                "uuid": "a6d4634d-9ba4-4a72-a69b-8ddd26f362aa",
                "identity": "mbsoliven",
                "email": "ninomichaelangelosoliven@gmail.com",
                "firstname": "Michael Angelo",
                "lastname": "Soliven",
                "displayName": "Michael Angelo Soliven"
            },
            {
                "uuid": "8646c8d4-f0e0-4f2a-abb0-6d782167901f",
                "identity": "jseet",
                "email": "jolene@intedashboard.com",
                "firstname": "Joleen",
                "lastname": "Seet",
                "displayName": "Joleen"
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

This resource update selected account.

### HTTP Request

`PUT [BASE_URL]/accounts/`**uuid**

URI Parameter | Type | Description
--------- | ------- | -----------
uuid | string | The generated UUID of the selected account.

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
paymentMethod <br /> `required`| **enum[string]** <br /> `Demo, Trial, Paid, Free` <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
type <br /> `required`| **enum[string]** <br /> `Institution, Student-paid, Free` <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
isActive| **boolean** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
isPaid| **boolean** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
isGeneric| **boolean** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
expiryDate | **date** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.






## Archive/Unarchive Account

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
        "accountName": "sample-account1",
        "organisationName": "Sample Account 1",
        "paymentMethod": "Free",
        "type": "Free",
        "isActive": false,
        "isPaid": false,
        "isGeneric": false,
        "expiryDate": null,
        "dateExpired": null,
        "uuid": "04a11db6-2f52-41fe-840d-b1f8662e674b",
        "isArchived": false,
        "isTrashed": false,
        "dateCreated": "2018-08-07T05:57:06Z",
        "lastModified": "2018-08-07T05:57:06Z",
        "accountAdmins": [
            {
                "uuid": "a6d4634d-9ba4-4a72-a69b-8ddd26f362aa",
                "identity": "mbsoliven",
                "email": "ninomichaelangelosoliven@gmail.com",
                "firstname": "Michael Angelo",
                "lastname": "Soliven",
                "displayName": "Michael Angelo Soliven"
            },
            {
                "uuid": "8646c8d4-f0e0-4f2a-abb0-6d782167901f",
                "identity": "jseet",
                "email": "jolene@intedashboard.com",
                "firstname": "Joleen",
                "lastname": "Seet",
                "displayName": "Joleen"
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

This resource archive/unarchive selected account.

### HTTP Request

`PATCH [BASE_URL]/accounts/`**uuid**

URI Parameter | Type | Description
--------- | ------- | -----------
uuid | string | The generated UUID of the selected account.

### HTTP Get Parameters

`No HTTP get parameters required.`

### Request Headers
Key | Value | Description
--------- | ------- | -----------
`Content-Type` | **application/json** | Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
`Authorization` | **Bearer $token** | Lorem ipsum dolor sit amet, consectetur adipiscing elit.


### HTTP Post Parameters

`No HTTP post parameters required.`









## Trash Account

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

This resource trash selected account.

### HTTP Request

`DELETE [BASE_URL]/accounts/`**uuid**

URI Parameter | Type | Description
--------- | ------- | -----------
uuid | string | The generated UUID of the selected account.

### HTTP Get Parameters

`No HTTP get parameters required.`

### Request Headers
Key | Value | Description
--------- | ------- | -----------
`Content-Type` | **application/json** | Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
`Authorization` | **Bearer $token** | Lorem ipsum dolor sit amet, consectetur adipiscing elit.


### HTTP Post Parameters

`No HTTP post parameters required.`






## Untrash Account

> 200

```json
{
    "data": {
        "id": 1,
        "accountName": "sample-account1",
        "organisationName": "Sample Account 1",
        "paymentMethod": "Free",
        "type": "Free",
        "isActive": false,
        "isPaid": false,
        "isGeneric": false,
        "expiryDate": null,
        "dateExpired": null,
        "uuid": "04a11db6-2f52-41fe-840d-b1f8662e674b",
        "isArchived": false,
        "isTrashed": false,
        "dateCreated": "2018-08-07T05:57:06Z",
        "lastModified": "2018-08-07T05:57:06Z",
        "accountAdmins": [
            {
                "uuid": "a6d4634d-9ba4-4a72-a69b-8ddd26f362aa",
                "identity": "mbsoliven",
                "email": "ninomichaelangelosoliven@gmail.com",
                "firstname": "Michael Angelo",
                "lastname": "Soliven",
                "displayName": "Michael Angelo Soliven"
            },
            {
                "uuid": "8646c8d4-f0e0-4f2a-abb0-6d782167901f",
                "identity": "jseet",
                "email": "jolene@intedashboard.com",
                "firstname": "Joleen",
                "lastname": "Seet",
                "displayName": "Joleen"
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

This resource untrash trashed account.

### HTTP Request

`GET [BASE_URL]/accounts/`**uuid**`/restore`

URI Parameter | Type | Description
--------- | ------- | -----------
uuid | string | The generated UUID of the selected account.

### HTTP Get Parameters

`No HTTP get parameters required.`

### Request Headers
Key | Value | Description
--------- | ------- | -----------
`Content-Type` | **application/json** | Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
`Authorization` | **Bearer $token** | Lorem ipsum dolor sit amet, consectetur adipiscing elit.


### HTTP Post Parameters

`No HTTP post parameters required.`