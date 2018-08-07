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
        "email": [
            "The selected email is invalid."
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
        "account": "Sample Account 3",
        "identity": "accountadmin1",
        "email": "accountadmin1@gmail.com",
        "firstname": "Account Admin 1",
        "lastname": null,
        "displayName": "Account Admin 1",
        "isActive": false,
        "isDeletable": true,
        "roleId": 2,
        "role": "Account Admin",
        "uuid": "12b45cf6-6e9f-4d9b-937a-78adf593f7a7",
        "isArchived": false,
        "isTrashed": false,
        "dateCreated": "2018-08-01T09:32:41Z",
        "createBy": "Brian O’Dwyer",
        "lastModified": "2018-08-06T06:41:50Z",
        "lastUpdatedBy": null,
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
    "identity": [
      "The account field is required."
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
email <br /> `required`| **enum[string]** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
password <br /> `required`| **enum[string]** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
password_confirmation <br /> `required`| **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.