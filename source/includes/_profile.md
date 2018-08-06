# Profile

<aside class="success">
Resources related to <code>profile management</code>.
</aside>



## Retrieve Profile

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

> 403

```json
{
  "error": {
    "message": "Permission denied.",
    "status_code": 403
  }
}
```


This resource retrieve user profile.




### HTTP Request

`GET [BASE_URL]/profile`

### HTTP Get Parameters

`No HTTP get parameters required.`

### Request Headers
Key | Value | Description
--------- | ------- | -----------
`Content-Type` | **application/json** | Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
`Authorization` | **Bearer $token** | Lorem ipsum dolor sit amet, consectetur adipiscing elit.


### HTTP Post Parameters

`No HTTP post parameters required.`



## Update Profile

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
        "email": [
            "The email has already been taken."
        ]
    },
    "status_code": 422
}
```

This resource update profile record.

### HTTP Request

`PUT [BASE_URL]/profile`

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
email | **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
identity | **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
firstname | **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
lastname | **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
displayName | **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.




## Update Password

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
        "password": [
            "Current password is invalid."
        ]
    },
    "status_code": 422
}
```

This resource update profile password.

### HTTP Request

`PATCH [BASE_URL]/profile/password`

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
current_password <br /> `required`| **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
password <br /> `required` | **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
password_confirmation <br /> `required`| **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.

<aside class="warning">
Requires re-login after updating password.
</aside>



## Sign-out

> 200

```json
{
    "invalidated": true
}
```

This resource sign outs current user.

### HTTP Request

`GET [BASE_URL]/profile/sign-out`

### HTTP Get Parameters

`No HTTP get parameters required.`

### Request Headers
Key | Value | Description
--------- | ------- | -----------
`Content-Type` | **application/json** | Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
`Authorization` | **Bearer $token** | Lorem ipsum dolor sit amet, consectetur adipiscing elit.


### HTTP Post Parameters

`No HTTP post parameters required.`