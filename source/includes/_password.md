# Password

<aside class="success">
Resources related to <code>password reset</code>.
</aside>




## Send Reset Token

> 200

```json
{
    "sent": true
}
```

> 422

```json
{
    "message": "422 Unprocessable Entity",
    "errors": {
        "organisation": [
            "The organisation field is required."
        ],
        "email": [
            "The email field is required."
        ]
    },
    "status_code": 422
}
```

This resource allows to send token for password reset/recovery.




### HTTP Request

`POST [BASE_URL]/password/send-token`

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
email <br /> `required`| **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
                

An email with a link to a password reset form is sent. The User resets his/her password using [Verify Account](#verify-account).

<aside class="warning">
If a user’s password is not changed after a certain period of time set by the admin (e.g., 80 days) an email reminder will be sent to the user daily until the allowable validity of password reset (e.g., 90 days), along with a link to reset the user's password. Day after the allowable validity of password reset, the system will no longer acknowledge the old password.
</aside>







## Reset Password

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

> 404

```json
{
    "message": "Reset token not found.",
    "status_code": 404
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
      "Password must contain numeric character(s).",
      "Previous password must never be used again."
    ],
    "password_confirmation": [
      "The password confirmation field is required."
    ]
  },
  "status_code": 422
}
```

This resource reset password.

### HTTP Request

`POST [BASE_URL]/password/reset`

### HTTP Get Parameters

`No HTTP get parameters required.`

### Request Headers
Key | Value | Description
--------- | ------- | -----------
`Content-Type` | **application/json** | Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.


### HTTP Post Parameters
Parameter | Description
--------- | -----------
means <br /> `required`| **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
token <br /> `required`| **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
password <br /> `required`| **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
password_confirmation <br /> `required`| **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.