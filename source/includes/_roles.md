# Roles

<aside class="success">
Resources related to <code>roles management</code>.
</aside>






## List

> 200

```json
{
    "data": [
        {
            "name": "Superuser",
            "access": "admins",
            "accessLevel": "All",
            "uuid": "dd7a1718-2c54-40a4-a086-994a2394b562",
            "isArchived": false,
            "isTrashed": false,
            "dateCreated": null,
            "lastModified": null,
            "authorisations": []
        },
        {
            "name": "Account Admin",
            "access": "admins",
            "accessLevel": "Organisation",
            "uuid": "7b3a8610-e9b2-4c01-b801-4f2cf17ef806",
            "isArchived": false,
            "isTrashed": false,
            "dateCreated": null,
            "lastModified": "2018-08-02T05:24:31Z",
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
        },
        {
            "name": "Teacher",
            "access": "teachers",
            "accessLevel": "Ownership",
            "uuid": "b30b29f7-fd5d-4ca4-8ec4-eacde54a80ae",
            "isArchived": false,
            "isTrashed": false,
            "dateCreated": null,
            "lastModified": null,
            "authorisations": []
        },
        {
            "name": "Student",
            "access": "students",
            "accessLevel": "Ownership",
            "uuid": "5c6f721a-3625-4067-a19e-ad6382571b52",
            "isArchived": false,
            "isTrashed": false,
            "dateCreated": null,
            "lastModified": null,
            "authorisations": []
        }
    ],
    "meta": {
        "pagination": {
            "total": 4,
            "count": 4,
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

This resource allows to list all roles.




### HTTP Request

`GET [BASE_URL]/roles`

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











## Retrieve

> 200

```json
{
    "data": {
        "name": "Account Admin",
        "access": "admins",
        "accessLevel": "Organisation",
        "uuid": "7b3a8610-e9b2-4c01-b801-4f2cf17ef806",
        "isArchived": false,
        "isTrashed": false,
        "dateCreated": null,
        "lastModified": "2018-08-02T05:24:31Z",
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

This resource retrieve specific role.

### HTTP Request

`GET [BASE_URL]/roles/`**uuid**

### HTTP Get Parameters

Parameter | Type | Description
--------- | ------- | -----------
uuid | string | The generated UUID of the selected role.

### Request Headers
Key | Value | Description
--------- | ------- | -----------
`Content-Type` | **application/json** | Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
`Authorization` | **Bearer $token** | Lorem ipsum dolor sit amet, consectetur adipiscing elit.


### HTTP Post Parameters

`No HTTP post parameters required.`









## Update

> 200

```json
{
    "data": {
        "name": "Account Admin",
        "access": "admins",
        "accessLevel": "Organisation",
        "uuid": "7b3a8610-e9b2-4c01-b801-4f2cf17ef806",
        "isArchived": false,
        "isTrashed": false,
        "dateCreated": null,
        "lastModified": "2018-08-02T05:24:31Z",
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

> 422

```json
{
  "message": "422 Unprocessable Entity",
  "errors": {
    "name": [
      "The name has already been taken."
    ]
  },
  "status_code": 422
}
```

This resource update selected roole.

### HTTP Request

`PUT [BASE_URL]/accounts/`**uuid**

### HTTP Get Parameters

Parameter | Type | Description
--------- | ------- | -----------
uuid | string | The generated UUID of the selected account.

### Request Headers
Key | Value | Description
--------- | ------- | -----------
`Content-Type` | **application/json** | Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
`Authorization` | **Bearer $token** | Lorem ipsum dolor sit amet, consectetur adipiscing elit.


### HTTP Post Parameters
Parameter | Description
--------- | -----------
access | **enum[string]** <br /> `admins, teachers, students` <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
accessLevel | **enum[string]** <br /> `All, Organisation, Ownership` <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
name| **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
routers| **array[string]** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.

<aside class="notice">
Sample value for <b>routers</b> parameter:

<br /> <br />
<code>
"routers": [ <br />
&nbsp; "App\\Http\\Controllers\\RouterController@index", <br />
&nbsp; "App\\Http\\Controllers\\UserController@index", <br />
&nbsp; "App\\Http\\Controllers\\UserController@store", <br />
&nbsp; "App\\Http\\Controllers\\UserController@show", <br />
&nbsp; "App\\Http\\Controllers\\UserController@update", <br />
&nbsp; "App\\Http\\Controllers\\UserController@archive", <br />
&nbsp; "App\\Http\\Controllers\\UserController@destroy", <br />
&nbsp; "App\\Http\\Controllers\\UserController@restore" <br />
]
</code>

</aside>

<aside class="warning">
To list all the routers, use this enpoint: 
<br />
<code> GET [BASE_URL]/routers </code>
</aside>