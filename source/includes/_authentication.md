# Authentication

<aside class="success">
Resources related to <code>authentication</code>.
</aside>

> Sample code:

```shell
# To authorize request, you can just pass the correct header with each request
curl "https://api3-dev.intedashboard.com/api/v1"
  -H "Content-Type: application/json"
  -H "Authorization: Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiIsImp0aSI6Imptd1ZTYnpDTzNxM1Rjb1ExenpOd1ZNcnRSZUtWa2dYUG1CS3M5ekNSaGxBZm5LaTFwQlJScjlYQzNtTDlRWTJPbVl2d2R6VWphYWhUTERWIn0.eyJzdWIiOiJJbnRlRGFzaGJvYXJkIiwiaXNzIjoiQ29nbmFMZWFybiIsImF1ZCI6ImFkbWlucyIsImp0aSI6Imptd1ZTYnpDTzNxM1Rjb1ExenpOd1ZNcnRSZUtWa2dYUG1CS3M5ekNSaGxBZm5LaTFwQlJScjlYQzNtTDlRWTJPbVl2d2R6VWphYWhUTERWIiwiaWF0IjoxNTMyNTI4OTkwLCJuYmYiOjE1MzI1Mjg5OTAsImV4cCI6MTUzMjYxNTM5MH0.XzD6IgazS4givUdYVWV0Srvi7D9m8D2XE_ehxui6OuQ"
```

> Make sure to replace `$token` with your personal token.

**InteDashboard™** expects for the `token` to be included in most (if not all) API requests to the server in a header that looks like the following:

`Authorization: Bearer $token`

<aside class="notice">
Replace <code>$token</code> with your personal token.
</aside>

## Process

To fully utilise the authentication, listed below are the flows to be followed:

* **[Verify Account](#verify-account)** - Once account has been created, a verification token will be sent to the email of the user. The said `token` must be used as one of the **HTTP Post Parameters** to successfully verify the account.
* **[Sign In](#sign-in)** - After verifying the account, user is now allowed to sign in the said account.


## Verify Account

> 200

```json
{
    "data": {
        "account": {
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
            "lastModified": "2018-11-22T06:16:49Z"
        },
        "accountUuid": "62edba2c-2b15-4053-8e7b-2d935ab914bd",
        "avatar": null,
        "lmsID": null,
        "identity": "1-ninomichaelangelosoliven+3@gmail.com",
        "email": "ninomichaelangelosoliven+3@gmail.com",
        "firstname": "Teacher Michael Angelo",
        "lastname": "Soliven",
        "displayName": "Teacher Michael Angelo Soliven",
        "accountType": null,
        "isActive": true,
        "isSuspended": false,
        "isDeletable": true,
        "roleId": 3,
        "role": "Teacher",
        "dateSuspended": null,
        "dateLastLogin": "2018-12-18T06:32:44Z",
        "dateTempPasswordRequested": null,
        "uuid": "69cf06a2-e946-40fd-8eed-28abfaa1e6e0",
        "isArchived": false,
        "isTrashed": false,
        "dateCreated": "2018-09-07T07:14:38Z",
        "createBy": "Michael Angelo11 Soliven11",
        "lastModified": "2018-12-18T06:32:44Z",
        "lastUpdatedBy": null,
        "dateActivated": null,
        "authorisations": [
            "App\\Http\\Controllers\\UserController@index",
            "App\\Http\\Controllers\\UserController@store",
            "App\\Http\\Controllers\\UserController@show",
            "App\\Http\\Controllers\\UserController@update",
            "App\\Http\\Controllers\\UserController@archive",
            "App\\Http\\Controllers\\UserController@destroy",
            "App\\Http\\Controllers\\UserController@restore"
        ],
        "courses": [
            {
                "accountType": "Full Access",
                "uuid": "3fc6328a-327f-44e1-9723-ef1ee7c4efa9",
                "description": "<p>Test Create 1</p>",
                "descriptionIsHTML": true,
                "consumerKeyLTI": "DpuOw8hMgvkrl1EiFxqH",
                "sharedSecretLTI": "jv6OUAZYQkhfIHK4lpNF",
                "code": "TA-18",
                "startDate": "2018-07-23T07:00:00Z",
                "endDate": "2018-07-26T07:00:00Z",
                "isPublished": true,
                "objectives": [
                    "O1"
                ],
                "configURLLTI": "v3-dev.intedashboard.com/lti/config/DpuOw8hMgvkrl1EiFxqH",
                "launchURLLTI": "v3-dev.intedashboard.com/lti/launch/DpuOw8hMgvkrl1EiFxqH",
                "isArchived": false,
                "isTrashed": false,
                "dateCreated": "2018-12-10T04:07:12Z",
                "lastModified": "2018-12-10T04:07:12Z"
            }
        ]
    }
}
```

> 401

```json
{
    "error": {
        "message": [
            "Verification are allowed for first time users only."
        ],
        "status_code": 401
    }
}
```

> 422

```json
{
  "message": "422 Unprocessable Entity",
  "errors": {
    "means": [
      "The means field is required.",
      "The selected means is invalid."
    ],
    "token": [
      "The token field is required.",
      "The selected token is invalid."
    ],
    "password": [
      "The password field is required.",
      "The password must be at least 8 characters.",
      "The password confirmation does not match.",
      "Password must contain uppercase character(s).",
      "Password must contain lowercase character(s).",
      "Password must contain special character(s).",
      "Password must contain numeric character(s)."
    ],
    "password_confirmation": [
      "The password confirmation field is required."
    ]
  },
  "status_code": 422
}
```

This resource verifies the user account.

### HTTP Request

`POST [BASE_URL]/password/verify`

### HTTP Get Parameters

`No HTTP get parameters required.`

### Request Headers
Key | Value | Description
--------- | ------- | -----------
`Content-Type` | **application/json** | Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.


### HTTP Post Parameters
Parameter | Description
--------- | -----------
means <br /> `required`| **string** <br /> token
token <br /> `required`| **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
password <br /> `required`| **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
password_confirmation <br /> `required`| **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.

            
            
            
            
            
	
## Sign In

> 200

```json
{
    "status_code": 200,
    "message": "OK",
    "user": {
        "account": {
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
            "lastModified": "2018-11-22T06:16:49Z"
        },
        "accountUuid": "62edba2c-2b15-4053-8e7b-2d935ab914bd",
        "avatar": null,
        "lmsID": null,
        "identity": "1-ninomichaelangelosoliven+3@gmail.com",
        "email": "ninomichaelangelosoliven+3@gmail.com",
        "firstname": "Teacher Michael Angelo",
        "lastname": "Soliven",
        "displayName": "Teacher Michael Angelo Soliven",
        "accountType": null,
        "isActive": true,
        "isSuspended": false,
        "isDeletable": true,
        "roleId": 3,
        "role": "Teacher",
        "dateSuspended": null,
        "dateLastLogin": "2018-12-18T06:32:44Z",
        "dateTempPasswordRequested": null,
        "uuid": "69cf06a2-e946-40fd-8eed-28abfaa1e6e0",
        "isArchived": false,
        "isTrashed": false,
        "dateCreated": "2018-09-07T07:14:38Z",
        "createBy": "Michael Angelo11 Soliven11",
        "lastModified": "2018-12-18T06:32:44Z",
        "lastUpdatedBy": null,
        "dateActivated": null,
        "authorisations": [
            "App\\Http\\Controllers\\UserController@index",
            "App\\Http\\Controllers\\UserController@store",
            "App\\Http\\Controllers\\UserController@show",
            "App\\Http\\Controllers\\UserController@update",
            "App\\Http\\Controllers\\UserController@archive",
            "App\\Http\\Controllers\\UserController@destroy",
            "App\\Http\\Controllers\\UserController@restore"
        ],
        "courses": [
            {
                "accountType": "Full Access",
                "uuid": "3fc6328a-327f-44e1-9723-ef1ee7c4efa9",
                "description": "<p>Test Create 1</p>",
                "descriptionIsHTML": true,
                "consumerKeyLTI": "DpuOw8hMgvkrl1EiFxqH",
                "sharedSecretLTI": "jv6OUAZYQkhfIHK4lpNF",
                "code": "TA-18",
                "startDate": "2018-07-23T07:00:00Z",
                "endDate": "2018-07-26T07:00:00Z",
                "isPublished": true,
                "objectives": [
                    "O1"
                ],
                "configURLLTI": "v3-dev.intedashboard.com/lti/config/DpuOw8hMgvkrl1EiFxqH",
                "launchURLLTI": "v3-dev.intedashboard.com/lti/launch/DpuOw8hMgvkrl1EiFxqH",
                "isArchived": false,
                "isTrashed": false,
                "dateCreated": "2018-12-10T04:07:12Z",
                "lastModified": "2018-12-10T04:07:12Z"
            }
        ]
    },
    "token": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiIsImp0aSI6IkRMWEk1TVcwbzMyaVBlQ04wb1hhU2dIb3ZXSGM3UWhvRlZ5QTBmbkFKRThHTmdSS1lSd1VKSnV3SjJ1eGxYRkhPN2djeHl0YTVhc0tTT2lPIn0.eyJzdWIiOiJJbnRlRGFzaGJvYXJkIiwiaXNzIjoiQ29nbmFMZWFybiIsImF1ZCI6IjMiLCJqdGkiOiJETFhJNU1XMG8zMmlQZUNOMG9YYVNnSG92V0hjN1Fob0ZWeUEwZm5BSkU4R05nUktZUndVSkp1d0oydXhsWEZITzdnY3h5dGE1YXNLU09pTyIsImlhdCI6MTU0NTExNDc3MSwibmJmIjoxNTQ1MTE0NzcxLCJleHAiOjE1NDUyMDExNzF9.4Eg6_9-XxCn2KCL4eFZxce-zJ6T_-KpbIvssLo-bWbc",
    "password_expired": false
}
```


> 401

```json
{
    "error": {
        "message": [
            "User not found. Please try again.",
            "Identity or Password is invalid."
        ],
        "status_code": 401
    }
}
```


> 403

```json
{
    "error": {
        "message": [
            "Account is suspended.",
            "User has multiple account. Please select role.",
            "User is not active.",
            "User is suspended."
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
        "organisation": [
            "The organisation field is required.",
            "Organisation not found."
        ],
        "identity": [
            "The identity field is required."
        ],
        "password": [
            "The password field is required."
        ]
    },
    "status_code": 422
}
```

This resource authenticates user account.

### HTTP Request

`POST [BASE_URL]/auth/sign-in`

### HTTP Get Parameters

`No HTTP get parameters required.`

### Request Headers
Key | Value | Description
--------- | ------- | -----------
`Content-Type` | **application/json** | Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.


### HTTP Post Parameters
Parameter | Description
--------- | -----------
organisation <br /> `required`| **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
identity <br /> `required`| **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
password <br /> `required`| **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.