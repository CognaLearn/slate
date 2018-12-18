# Profile

<aside class="success">
Resources related to <code>profile management</code>.
</aside>



## Retrieve Profile

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
        ],
        "identity": [
            "The identity has already been taken."
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