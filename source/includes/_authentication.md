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
        "account": "Sample Account",
        "identity": "mbsoliven",
        "email": "ninomichaelangelosoliven@gmail.com",
        "firstname": "Michael Angelo",
        "lastname": "Soliven",
        "displayName": "Michael Angelo Soliven",
        "role": "teacher",
        "uuid": "6747a397-285f-4848-b0e0-b217b5fa2a2c",
        "isArchived": false,
        "isTrashed": false,
        "dateCreated": "2018-07-26T02:51:52Z",
        "createBy": "Brian O’Dwyer",
        "lastModified": "2018-07-26T03:01:25Z",
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
            "Verification are allowed for first time users only."
        ],
        "status_code": 403
    }
}
```

> 404

```json
{
    "error": {
        "message": [
            "Reset token not found.",
            "Email not found."
        ],
        "status_code": 404
    }
}
```

> 422

```json
{
    "message": [
        "422 Unprocessable Entity",
        "Password must contain uppercase character(s).",
        "Password must contain lowercase character(s).",
        "Password must contain special character(s).",
        "Password must contain numeric character(s)."
    ],
    "errors": {
        "identity": [
            "The access field is required."
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
email <br /> `required`| **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
password <br /> `required`| **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
password_confirmation <br /> `required`| **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
            
            
            
            
            
            
	
## Sign In

> 200

```json
{
    "status_code": 200,
    "message": "OK",
    "user": {
        "account": null,
        "identity": "bodwyer",
        "email": "brian@cognalearn.com",
        "firstname": "Brian",
        "lastname": "O’Dwyer",
        "displayName": "",
        "role": "super admin",
        "uuid": "b5669180-a81e-490e-ae4e-f464e5afdb5b",
        "isArchived": false,
        "isTrashed": false,
        "dateCreated": null,
        "createBy": null,
        "lastModified": "2018-07-26T02:45:28Z",
        "lastUpdatedBy": null,
        "authorisations": []
    },
    "token": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiIsImp0aSI6Ikd5T0M1NG1vbThEaVZkTDJqQzQxZ3pzeUV5NllJanFXTjhsVWE3YzRldUJTdUQ5bFZYd29EUzNSVnVRZ3JPWGl6VXhqeW50TVdpSmExUEdQIn0.eyJzdWIiOiJJbnRlRGFzaGJvYXJkIiwiaXNzIjoiQ29nbmFMZWFybiIsImF1ZCI6InN1cGVyIGFkbWluIiwianRpIjoiR3lPQzU0bW9tOERpVmRMMmpDNDFnenN5RXk2WUlqcVdOOGxVYTdjNGV1QlN1RDlsVlh3b0RTM1JWdVFnck9YaXpVeGp5bnRNV2lKYTFQR1AiLCJpYXQiOjE1MzI1NzMxMzAsIm5iZiI6MTUzMjU3MzEzMCwiZXhwIjoxNTMyNjU5NTMwfQ.8Q-UZYp7iwrfQO5HNBF68u8dxkdbJJwT9gDWhzzeV7M",
    "password_expired": false
}
```

> 403

```json
{
    "error": {
        "message": [
            "Identity or Password is invalid.",
            "Identity or Password is invalid. 3 login attempt(s) left",
            "Account has been temporarily locked because of too many failed attempts.",
            "Account has been locked. Please contact your Account Administrator.",
            "Account has been locked. Please try again after 6hr and 32min or contact your Account Administrator."
            "Permission denied."
        ],
        "status_code": 403
    }
}
```

> 404

```json
{
    "error": {
        "message": [
            "User does not exist."
        ],
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
            "The identity field is required."
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
identity <br /> `required`| **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
password <br /> `required`| **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.