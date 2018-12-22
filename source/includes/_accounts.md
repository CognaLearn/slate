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
            "avatar": null,
            "accountName": "soliven",
            "organisationName": "Soliven Updated",
            "paymentMethod": "Student",
            "type": "Free",
            "isActive": false,
            "isSuspended": false,
            "isPaid": false,
            "startDate": null,
            "expiryDate": null,
            "dateExpired": null,
            "dateActivated": null,
            "uuid": "62edba2c-2b15-4053-8e7b-2d935ab914bd",
            "isArchived": false,
            "isTrashed": false,
            "dateCreated": "2018-09-05T05:01:04Z",
            "createBy": "Mark Png",
            "lastModified": "2018-11-22T06:16:49Z",
            "paymentPlans": [
                {
                    "uuid": "391d2506-a6fa-49f8-ac8d-284010459e43",
                    "name": "One Year",
                    "price": "12.23",
                    "currency": "USD",
                    "startDate": "2018-07-23T00:00:00Z",
                    "endDate": "2018-07-24T00:00:00Z"
                }
            ],
            "adminTeacherAccounts": [
                {
                    "uuid": "deb49db3-99a3-4f7a-bd98-86a6ef46111b",
                    "identity": "1-ninomichaelangelosoliven+2@gmail.com",
                    "email": "ninomichaelangelosoliven+2@gmail.com",
                    "firstname": "Michael Angelo11",
                    "lastname": "Soliven11",
                    "displayName": "Michael Angelo Soliven",
                    "accountType": null,
                    "isActive": true,
                    "isSuspended": false,
                    "dateLastLogin": "2018-12-10T02:40:29Z"
                },
                {
                    "uuid": "7c59fb65-59fd-40cc-b8fe-17a8594515bg",
                    "identity": "1-mcpng",
                    "email": "mark.c.png@gmail.com",
                    "firstname": "Mark",
                    "lastname": "Png",
                    "displayName": "",
                    "accountType": null,
                    "isActive": true,
                    "isSuspended": false,
                    "dateLastLogin": "2018-11-08T05:11:44Z"
                }
            ],
            "adminTeacherAccount": {
                "uuid": "deb49db3-99a3-4f7a-bd98-86a6ef46111b",
                "identity": "1-ninomichaelangelosoliven+2@gmail.com",
                "email": "ninomichaelangelosoliven+2@gmail.com",
                "firstname": "Michael Angelo11",
                "lastname": "Soliven11",
                "displayName": "Michael Angelo Soliven",
                "accountType": null,
                "isActive": true,
                "isSuspended": false,
                "dateLastLogin": "2018-12-10T02:40:29Z"
            },
            "teachers": [
                {
                    "uuid": "48bfd12b-ff6a-485a-9d2b-edfc8ac5c7b4",
                    "identity": "1-test4@example.com",
                    "email": "test4@example.com",
                    "firstname": "Updated thru",
                    "lastname": "Course User",
                    "displayName": "Jane Why Doe",
                    "isActive": false,
                    "isSuspended": false,
                    "dateLastLogin": null
                },
                {
                    "uuid": "69cf06a2-e946-40fd-8eed-28abfaa1e6e0",
                    "identity": "1-ninomichaelangelosoliven+3@gmail.com",
                    "email": "ninomichaelangelosoliven+3@gmail.com",
                    "firstname": "Teacher Michael Angelo",
                    "lastname": "Soliven",
                    "displayName": "Teacher Michael Angelo Soliven",
                    "isActive": true,
                    "isSuspended": false,
                    "dateLastLogin": "2018-12-20T04:14:21Z"
                },
                {
                    "uuid": "7c59fb65-59fd-40cc-b8fe-17a8594515bh",
                    "identity": "1-mcpng-st",
                    "email": "mark.c.png@gmail.com",
                    "firstname": "Mark",
                    "lastname": "Png",
                    "displayName": "",
                    "isActive": true,
                    "isSuspended": false,
                    "dateLastLogin": "2018-10-25T09:29:34Z"
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
        "avatar": null,
        "accountName": "soliven",
        "organisationName": "Soliven Updated",
        "paymentMethod": "Student",
        "type": "Free",
        "isActive": false,
        "isSuspended": false,
        "isPaid": false,
        "startDate": null,
        "expiryDate": null,
        "dateExpired": null,
        "dateActivated": null,
        "uuid": "62edba2c-2b15-4053-8e7b-2d935ab914bd",
        "isArchived": false,
        "isTrashed": false,
        "dateCreated": "2018-09-05T05:01:04Z",
        "createBy": "Mark Png",
        "lastModified": "2018-11-22T06:16:49Z",
        "paymentPlans": [
            {
                "uuid": "391d2506-a6fa-49f8-ac8d-284010459e43",
                "name": "One Year",
                "price": "12.23",
                "currency": "USD",
                "startDate": "2018-07-23T00:00:00Z",
                "endDate": "2018-07-24T00:00:00Z"
            }
        ],
        "adminTeacherAccounts": [
            {
                "uuid": "deb49db3-99a3-4f7a-bd98-86a6ef46111b",
                "identity": "1-ninomichaelangelosoliven+2@gmail.com",
                "email": "ninomichaelangelosoliven+2@gmail.com",
                "firstname": "Michael Angelo11",
                "lastname": "Soliven11",
                "displayName": "Michael Angelo Soliven",
                "accountType": null,
                "isActive": true,
                "isSuspended": false,
                "dateLastLogin": "2018-12-10T02:40:29Z"
            },
            {
                "uuid": "7c59fb65-59fd-40cc-b8fe-17a8594515bg",
                "identity": "1-mcpng",
                "email": "mark.c.png@gmail.com",
                "firstname": "Mark",
                "lastname": "Png",
                "displayName": "",
                "accountType": null,
                "isActive": true,
                "isSuspended": false,
                "dateLastLogin": "2018-11-08T05:11:44Z"
            }
        ],
        "adminTeacherAccount": {
            "uuid": "deb49db3-99a3-4f7a-bd98-86a6ef46111b",
            "identity": "1-ninomichaelangelosoliven+2@gmail.com",
            "email": "ninomichaelangelosoliven+2@gmail.com",
            "firstname": "Michael Angelo11",
            "lastname": "Soliven11",
            "displayName": "Michael Angelo Soliven",
            "accountType": null,
            "isActive": true,
            "isSuspended": false,
            "dateLastLogin": "2018-12-10T02:40:29Z"
        },
        "teachers": [
            {
                "uuid": "48bfd12b-ff6a-485a-9d2b-edfc8ac5c7b4",
                "identity": "1-test4@example.com",
                "email": "test4@example.com",
                "firstname": "Updated thru",
                "lastname": "Course User",
                "displayName": "Jane Why Doe",
                "isActive": false,
                "isSuspended": false,
                "dateLastLogin": null
            },
            {
                "uuid": "69cf06a2-e946-40fd-8eed-28abfaa1e6e0",
                "identity": "1-ninomichaelangelosoliven+3@gmail.com",
                "email": "ninomichaelangelosoliven+3@gmail.com",
                "firstname": "Teacher Michael Angelo",
                "lastname": "Soliven",
                "displayName": "Teacher Michael Angelo Soliven",
                "isActive": true,
                "isSuspended": false,
                "dateLastLogin": "2018-12-20T04:14:21Z"
            },
            {
                "uuid": "7c59fb65-59fd-40cc-b8fe-17a8594515bh",
                "identity": "1-mcpng-st",
                "email": "mark.c.png@gmail.com",
                "firstname": "Mark",
                "lastname": "Png",
                "displayName": "",
                "isActive": true,
                "isSuspended": false,
                "dateLastLogin": "2018-10-25T09:29:34Z"
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
        "accountName": [
            "The account name field is required.",
            "The account name has already been taken.",
            "The account name should only contain alphanumeric characters (a-z, 0-9).",
            "The account name should not contain uppercase.",
            "The account name should not contain special characters.",
            "Reserved words should never be used."
        ],
        "organisationName": [
            "The organisation name field is required.",
            "The organisation name has already been taken."
        ],
        "type": [
            "The selected type is invalid."
        ],
        "paymentMethod": [
            "The selected payment method is invalid."
        ],
        "startDate": [
            "The start date field is required."
        ],
        "expiryDate": [
            "The expiry date field is required."
        ],
        "paymentPlans": [
            "The payment plans field is required."
        ],
        "email": [
            "The email field is required."
        ],
        "identity": [
            "The identity field is required."
        ],
        "firstname": [
            "The firstname field is required."
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
avatar <br /> | **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
accountName <br /> `required`| **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
organisationName <br /> `required`| **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
paymentMethod <br /> `required`| **enum[string]** <br /> `Institute, Student, Free` <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
type <br /> `required`| **enum[string]** <br /> `Demo, Trial, Paid, Free` <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
accountType <br /> | **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
startDate <br /> `required if paymentMethod == institute`| **date** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
expiryDate <br /> `required if paymentMethod == institute`| **date** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
paymentPlans <br /> `required if paymentMethod == student`| **json[string]** <br /> `[name, price, currency, startDate, endDate]` <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
firstname <br /> `required`| **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
lastname | **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
identity <br /> `required`| **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
email <br /> `required`| **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
                

<aside class="info">
When an Account is created by a Superuser, the Admin Teacher receives an invitation email with a link for them to set their password and access their Account.
</aside>



## Retrieve Account

> 200

```json
{
    "data": {
        "avatar": null,
        "accountName": "soliven",
        "organisationName": "Soliven Updated",
        "paymentMethod": "Student",
        "type": "Free",
        "isActive": false,
        "isSuspended": false,
        "isPaid": false,
        "startDate": null,
        "expiryDate": null,
        "dateExpired": null,
        "dateActivated": null,
        "uuid": "62edba2c-2b15-4053-8e7b-2d935ab914bd",
        "isArchived": false,
        "isTrashed": false,
        "dateCreated": "2018-09-05T05:01:04Z",
        "createBy": "Mark Png",
        "lastModified": "2018-11-22T06:16:49Z",
        "paymentPlans": [
            {
                "uuid": "391d2506-a6fa-49f8-ac8d-284010459e43",
                "name": "One Year",
                "price": "12.23",
                "currency": "USD",
                "startDate": "2018-07-23T00:00:00Z",
                "endDate": "2018-07-24T00:00:00Z"
            }
        ],
        "adminTeacherAccounts": [
            {
                "uuid": "deb49db3-99a3-4f7a-bd98-86a6ef46111b",
                "identity": "1-ninomichaelangelosoliven+2@gmail.com",
                "email": "ninomichaelangelosoliven+2@gmail.com",
                "firstname": "Michael Angelo11",
                "lastname": "Soliven11",
                "displayName": "Michael Angelo Soliven",
                "accountType": null,
                "isActive": true,
                "isSuspended": false,
                "dateLastLogin": "2018-12-10T02:40:29Z"
            },
            {
                "uuid": "7c59fb65-59fd-40cc-b8fe-17a8594515bg",
                "identity": "1-mcpng",
                "email": "mark.c.png@gmail.com",
                "firstname": "Mark",
                "lastname": "Png",
                "displayName": "",
                "accountType": null,
                "isActive": true,
                "isSuspended": false,
                "dateLastLogin": "2018-11-08T05:11:44Z"
            }
        ],
        "adminTeacherAccount": {
            "uuid": "deb49db3-99a3-4f7a-bd98-86a6ef46111b",
            "identity": "1-ninomichaelangelosoliven+2@gmail.com",
            "email": "ninomichaelangelosoliven+2@gmail.com",
            "firstname": "Michael Angelo11",
            "lastname": "Soliven11",
            "displayName": "Michael Angelo Soliven",
            "accountType": null,
            "isActive": true,
            "isSuspended": false,
            "dateLastLogin": "2018-12-10T02:40:29Z"
        },
        "teachers": [
            {
                "uuid": "48bfd12b-ff6a-485a-9d2b-edfc8ac5c7b4",
                "identity": "1-test4@example.com",
                "email": "test4@example.com",
                "firstname": "Updated thru",
                "lastname": "Course User",
                "displayName": "Jane Why Doe",
                "isActive": false,
                "isSuspended": false,
                "dateLastLogin": null
            },
            {
                "uuid": "69cf06a2-e946-40fd-8eed-28abfaa1e6e0",
                "identity": "1-ninomichaelangelosoliven+3@gmail.com",
                "email": "ninomichaelangelosoliven+3@gmail.com",
                "firstname": "Teacher Michael Angelo",
                "lastname": "Soliven",
                "displayName": "Teacher Michael Angelo Soliven",
                "isActive": true,
                "isSuspended": false,
                "dateLastLogin": "2018-12-20T04:14:21Z"
            },
            {
                "uuid": "7c59fb65-59fd-40cc-b8fe-17a8594515bh",
                "identity": "1-mcpng-st",
                "email": "mark.c.png@gmail.com",
                "firstname": "Mark",
                "lastname": "Png",
                "displayName": "",
                "isActive": true,
                "isSuspended": false,
                "dateLastLogin": "2018-10-25T09:29:34Z"
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
        "avatar": null,
        "accountName": "soliven",
        "organisationName": "Soliven Updated",
        "paymentMethod": "Student",
        "type": "Free",
        "isActive": false,
        "isSuspended": false,
        "isPaid": false,
        "startDate": null,
        "expiryDate": null,
        "dateExpired": null,
        "dateActivated": null,
        "uuid": "62edba2c-2b15-4053-8e7b-2d935ab914bd",
        "isArchived": false,
        "isTrashed": false,
        "dateCreated": "2018-09-05T05:01:04Z",
        "createBy": "Mark Png",
        "lastModified": "2018-11-22T06:16:49Z",
        "paymentPlans": [
            {
                "uuid": "391d2506-a6fa-49f8-ac8d-284010459e43",
                "name": "One Year",
                "price": "12.23",
                "currency": "USD",
                "startDate": "2018-07-23T00:00:00Z",
                "endDate": "2018-07-24T00:00:00Z"
            }
        ],
        "adminTeacherAccounts": [
            {
                "uuid": "deb49db3-99a3-4f7a-bd98-86a6ef46111b",
                "identity": "1-ninomichaelangelosoliven+2@gmail.com",
                "email": "ninomichaelangelosoliven+2@gmail.com",
                "firstname": "Michael Angelo11",
                "lastname": "Soliven11",
                "displayName": "Michael Angelo Soliven",
                "accountType": null,
                "isActive": true,
                "isSuspended": false,
                "dateLastLogin": "2018-12-10T02:40:29Z"
            },
            {
                "uuid": "7c59fb65-59fd-40cc-b8fe-17a8594515bg",
                "identity": "1-mcpng",
                "email": "mark.c.png@gmail.com",
                "firstname": "Mark",
                "lastname": "Png",
                "displayName": "",
                "accountType": null,
                "isActive": true,
                "isSuspended": false,
                "dateLastLogin": "2018-11-08T05:11:44Z"
            }
        ],
        "adminTeacherAccount": {
            "uuid": "deb49db3-99a3-4f7a-bd98-86a6ef46111b",
            "identity": "1-ninomichaelangelosoliven+2@gmail.com",
            "email": "ninomichaelangelosoliven+2@gmail.com",
            "firstname": "Michael Angelo11",
            "lastname": "Soliven11",
            "displayName": "Michael Angelo Soliven",
            "accountType": null,
            "isActive": true,
            "isSuspended": false,
            "dateLastLogin": "2018-12-10T02:40:29Z"
        },
        "teachers": [
            {
                "uuid": "48bfd12b-ff6a-485a-9d2b-edfc8ac5c7b4",
                "identity": "1-test4@example.com",
                "email": "test4@example.com",
                "firstname": "Updated thru",
                "lastname": "Course User",
                "displayName": "Jane Why Doe",
                "isActive": false,
                "isSuspended": false,
                "dateLastLogin": null
            },
            {
                "uuid": "69cf06a2-e946-40fd-8eed-28abfaa1e6e0",
                "identity": "1-ninomichaelangelosoliven+3@gmail.com",
                "email": "ninomichaelangelosoliven+3@gmail.com",
                "firstname": "Teacher Michael Angelo",
                "lastname": "Soliven",
                "displayName": "Teacher Michael Angelo Soliven",
                "isActive": true,
                "isSuspended": false,
                "dateLastLogin": "2018-12-20T04:14:21Z"
            },
            {
                "uuid": "7c59fb65-59fd-40cc-b8fe-17a8594515bh",
                "identity": "1-mcpng-st",
                "email": "mark.c.png@gmail.com",
                "firstname": "Mark",
                "lastname": "Png",
                "displayName": "",
                "isActive": true,
                "isSuspended": false,
                "dateLastLogin": "2018-10-25T09:29:34Z"
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
        "accountName": [
            "The account name has already been taken.",
            "The account name should only contain alphanumeric characters (a-z, 0-9).",
            "The account name should not contain uppercase.",
            "The account name should not contain special characters.",
            "Reserved words should never be used."
        ],
        "organisationName": [
            "The organisation name has already been taken."
        ],
        "type": [
            "The selected type is invalid."
        ],
        "paymentMethod": [
            "The selected payment method is invalid."
        ],
        "startDate": [
            "The start date field is required."
        ],
        "expiryDate": [
            "The expiry date field is required."
        ],
        "paymentPlans": [
            "The payment plans field is required."
        ],
        "isActive": [
          "The is active field must be true or false."
        ],
        "isSuspended": [
          "The is suspended field must be true or false."
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
avatar <br /> | **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
accountName <br /> `required`| **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
organisationName <br /> `required`| **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
paymentMethod <br /> `required`| **enum[string]** <br /> `Institute, Student, Free` <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
type <br /> `required`| **enum[string]** <br /> `Demo, Trial, Paid, Free` <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
accountType <br /> | **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
startDate <br /> `required if paymentMethod == institute`| **date** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
expiryDate <br /> `required if paymentMethod == institute`| **date** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
paymentPlans <br /> `required if paymentMethod == student`| **json[string]** <br /> `[name, price, currency, startDate, endDate]` <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
firstname <br /> `required`| **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
lastname | **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
identity <br /> `required`| **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
email <br /> `required`| **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
isSuspended <br /> | **boolean** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
isActive <br /> | **boolean** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.






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
        "avatar": null,
        "accountName": "soliven",
        "organisationName": "Soliven Updated",
        "paymentMethod": "Student",
        "type": "Free",
        "isActive": false,
        "isSuspended": false,
        "isPaid": false,
        "startDate": null,
        "expiryDate": null,
        "dateExpired": null,
        "dateActivated": null,
        "uuid": "62edba2c-2b15-4053-8e7b-2d935ab914bd",
        "isArchived": false,
        "isTrashed": false,
        "dateCreated": "2018-09-05T05:01:04Z",
        "createBy": "Mark Png",
        "lastModified": "2018-11-22T06:16:49Z",
        "paymentPlans": [
            {
                "uuid": "391d2506-a6fa-49f8-ac8d-284010459e43",
                "name": "One Year",
                "price": "12.23",
                "currency": "USD",
                "startDate": "2018-07-23T00:00:00Z",
                "endDate": "2018-07-24T00:00:00Z"
            }
        ],
        "adminTeacherAccounts": [
            {
                "uuid": "deb49db3-99a3-4f7a-bd98-86a6ef46111b",
                "identity": "1-ninomichaelangelosoliven+2@gmail.com",
                "email": "ninomichaelangelosoliven+2@gmail.com",
                "firstname": "Michael Angelo11",
                "lastname": "Soliven11",
                "displayName": "Michael Angelo Soliven",
                "accountType": null,
                "isActive": true,
                "isSuspended": false,
                "dateLastLogin": "2018-12-10T02:40:29Z"
            },
            {
                "uuid": "7c59fb65-59fd-40cc-b8fe-17a8594515bg",
                "identity": "1-mcpng",
                "email": "mark.c.png@gmail.com",
                "firstname": "Mark",
                "lastname": "Png",
                "displayName": "",
                "accountType": null,
                "isActive": true,
                "isSuspended": false,
                "dateLastLogin": "2018-11-08T05:11:44Z"
            }
        ],
        "adminTeacherAccount": {
            "uuid": "deb49db3-99a3-4f7a-bd98-86a6ef46111b",
            "identity": "1-ninomichaelangelosoliven+2@gmail.com",
            "email": "ninomichaelangelosoliven+2@gmail.com",
            "firstname": "Michael Angelo11",
            "lastname": "Soliven11",
            "displayName": "Michael Angelo Soliven",
            "accountType": null,
            "isActive": true,
            "isSuspended": false,
            "dateLastLogin": "2018-12-10T02:40:29Z"
        },
        "teachers": [
            {
                "uuid": "48bfd12b-ff6a-485a-9d2b-edfc8ac5c7b4",
                "identity": "1-test4@example.com",
                "email": "test4@example.com",
                "firstname": "Updated thru",
                "lastname": "Course User",
                "displayName": "Jane Why Doe",
                "isActive": false,
                "isSuspended": false,
                "dateLastLogin": null
            },
            {
                "uuid": "69cf06a2-e946-40fd-8eed-28abfaa1e6e0",
                "identity": "1-ninomichaelangelosoliven+3@gmail.com",
                "email": "ninomichaelangelosoliven+3@gmail.com",
                "firstname": "Teacher Michael Angelo",
                "lastname": "Soliven",
                "displayName": "Teacher Michael Angelo Soliven",
                "isActive": true,
                "isSuspended": false,
                "dateLastLogin": "2018-12-20T04:14:21Z"
            },
            {
                "uuid": "7c59fb65-59fd-40cc-b8fe-17a8594515bh",
                "identity": "1-mcpng-st",
                "email": "mark.c.png@gmail.com",
                "firstname": "Mark",
                "lastname": "Png",
                "displayName": "",
                "isActive": true,
                "isSuspended": false,
                "dateLastLogin": "2018-10-25T09:29:34Z"
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
        "avatar": null,
        "accountName": "soliven",
        "organisationName": "Soliven Updated",
        "paymentMethod": "Student",
        "type": "Free",
        "isActive": false,
        "isSuspended": false,
        "isPaid": false,
        "startDate": null,
        "expiryDate": null,
        "dateExpired": null,
        "dateActivated": null,
        "uuid": "62edba2c-2b15-4053-8e7b-2d935ab914bd",
        "isArchived": false,
        "isTrashed": false,
        "dateCreated": "2018-09-05T05:01:04Z",
        "createBy": "Mark Png",
        "lastModified": "2018-11-22T06:16:49Z",
        "paymentPlans": [
            {
                "uuid": "391d2506-a6fa-49f8-ac8d-284010459e43",
                "name": "One Year",
                "price": "12.23",
                "currency": "USD",
                "startDate": "2018-07-23T00:00:00Z",
                "endDate": "2018-07-24T00:00:00Z"
            }
        ],
        "adminTeacherAccounts": [
            {
                "uuid": "deb49db3-99a3-4f7a-bd98-86a6ef46111b",
                "identity": "1-ninomichaelangelosoliven+2@gmail.com",
                "email": "ninomichaelangelosoliven+2@gmail.com",
                "firstname": "Michael Angelo11",
                "lastname": "Soliven11",
                "displayName": "Michael Angelo Soliven",
                "accountType": null,
                "isActive": true,
                "isSuspended": false,
                "dateLastLogin": "2018-12-10T02:40:29Z"
            },
            {
                "uuid": "7c59fb65-59fd-40cc-b8fe-17a8594515bg",
                "identity": "1-mcpng",
                "email": "mark.c.png@gmail.com",
                "firstname": "Mark",
                "lastname": "Png",
                "displayName": "",
                "accountType": null,
                "isActive": true,
                "isSuspended": false,
                "dateLastLogin": "2018-11-08T05:11:44Z"
            }
        ],
        "adminTeacherAccount": {
            "uuid": "deb49db3-99a3-4f7a-bd98-86a6ef46111b",
            "identity": "1-ninomichaelangelosoliven+2@gmail.com",
            "email": "ninomichaelangelosoliven+2@gmail.com",
            "firstname": "Michael Angelo11",
            "lastname": "Soliven11",
            "displayName": "Michael Angelo Soliven",
            "accountType": null,
            "isActive": true,
            "isSuspended": false,
            "dateLastLogin": "2018-12-10T02:40:29Z"
        },
        "teachers": [
            {
                "uuid": "48bfd12b-ff6a-485a-9d2b-edfc8ac5c7b4",
                "identity": "1-test4@example.com",
                "email": "test4@example.com",
                "firstname": "Updated thru",
                "lastname": "Course User",
                "displayName": "Jane Why Doe",
                "isActive": false,
                "isSuspended": false,
                "dateLastLogin": null
            },
            {
                "uuid": "69cf06a2-e946-40fd-8eed-28abfaa1e6e0",
                "identity": "1-ninomichaelangelosoliven+3@gmail.com",
                "email": "ninomichaelangelosoliven+3@gmail.com",
                "firstname": "Teacher Michael Angelo",
                "lastname": "Soliven",
                "displayName": "Teacher Michael Angelo Soliven",
                "isActive": true,
                "isSuspended": false,
                "dateLastLogin": "2018-12-20T04:14:21Z"
            },
            {
                "uuid": "7c59fb65-59fd-40cc-b8fe-17a8594515bh",
                "identity": "1-mcpng-st",
                "email": "mark.c.png@gmail.com",
                "firstname": "Mark",
                "lastname": "Png",
                "displayName": "",
                "isActive": true,
                "isSuspended": false,
                "dateLastLogin": "2018-10-25T09:29:34Z"
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