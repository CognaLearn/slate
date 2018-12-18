# Users

<aside class="success">
Resources related to <code>user management</code>.
</aside>






## List of Users

> 200

```json
{
    "data": [
        {
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
            "identity": "1-student1",
            "email": "student-1@sample.com",
            "firstname": "First",
            "lastname": "Student",
            "displayName": "First Student",
            "accountType": null,
            "isActive": false,
            "isSuspended": false,
            "isDeletable": true,
            "roleId": 4,
            "role": "Student",
            "dateSuspended": null,
            "dateLastLogin": null,
            "dateTempPasswordRequested": null,
            "uuid": "62430d3b-61c0-4697-9fd6-848d91a7a01a",
            "isArchived": false,
            "isTrashed": false,
            "dateCreated": "2018-10-02T07:04:44Z",
            "createBy": "Michael Angelo11 Soliven11",
            "lastModified": "2018-10-02T07:04:44Z",
            "lastUpdatedBy": null,
            "dateActivated": null,
            "authorisations": [],
            "courses": [
                {
                    "accountType": null,
                    "uuid": "1ec37b16-a6c6-48b9-96bb-d12d97d6cab2",
                    "description": "<p>Sample Description</p>",
                    "descriptionIsHTML": true,
                    "consumerKeyLTI": "key123452",
                    "sharedSecretLTI": "secret123452",
                    "code": "SC-2",
                    "startDate": "2018-07-23T07:00:00Z",
                    "endDate": "2018-07-26T07:00:00Z",
                    "isPublished": true,
                    "objectives": null,
                    "configURLLTI": "v3-dev.intedashboard.com/lti/config/key123452",
                    "launchURLLTI": "v3-dev.intedashboard.com/lti/launch/key123452",
                    "isArchived": false,
                    "isTrashed": false,
                    "dateCreated": "2018-09-05T07:33:54Z",
                    "lastModified": "2018-09-05T07:33:54Z"
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

This resource allows to list all users.




### HTTP Request

`GET [BASE_URL]/users`

### HTTP Get Parameters

[Standard HTTP Get Parameters](#principles)

`i.e. [BASE_URL]/users?page=1&per_page=3`

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











## Create User

> 201

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
        "identity": "1-student1",
        "email": "student-1@sample.com",
        "firstname": "First",
        "lastname": "Student",
        "displayName": "First Student",
        "accountType": null,
        "isActive": false,
        "isSuspended": false,
        "isDeletable": true,
        "roleId": 4,
        "role": "Student",
        "dateSuspended": null,
        "dateLastLogin": null,
        "dateTempPasswordRequested": null,
        "uuid": "62430d3b-61c0-4697-9fd6-848d91a7a01a",
        "isArchived": false,
        "isTrashed": false,
        "dateCreated": "2018-10-02T07:04:44Z",
        "createBy": "Michael Angelo11 Soliven11",
        "lastModified": "2018-10-02T07:04:44Z",
        "lastUpdatedBy": null,
        "dateActivated": null,
        "authorisations": [],
        "courses": []
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
      "The email field is required.",
      "The email is invalid."
    ],
    "firstname": [
      "The firstname field is required."
    ],
    "roleId": [
      "The role id field is required.",
      "The selected role id is invalid."
    ],
    "accountUuid": [
      "The account uuid field is required.",
      "The selected account uuid is invalid."
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

This resource create new user.

### HTTP Request

`POST [BASE_URL]/users`

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
email <br /> `required`| **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
firstname <br /> `required`| **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
roleId <br /> `required`| **int** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
accountUuid <br /> `required if roleId != 1`| **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
password | **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
password_confirmation <br /> `required if isset(password)`| **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.                

<aside class="notice">
If <code>password</code> is not provided, activation link will be sent to the email.
</aside>


## Retrieve User

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
        "identity": "1-ninomichaelangelosoliven+2@gmail.com",
        "email": "ninomichaelangelosoliven+2@gmail.com",
        "firstname": "Michael Angelo11",
        "lastname": "Soliven11",
        "displayName": "Michael Angelo Soliven",
        "accountType": null,
        "isActive": true,
        "isSuspended": false,
        "isDeletable": true,
        "roleId": 2,
        "role": "Account Admin",
        "dateSuspended": null,
        "dateLastLogin": "2018-12-10T02:40:29Z",
        "dateTempPasswordRequested": null,
        "uuid": "deb49db3-99a3-4f7a-bd98-86a6ef46111b",
        "isArchived": false,
        "isTrashed": false,
        "dateCreated": "2018-09-05T05:09:46Z",
        "createBy": "Mark Png",
        "lastModified": "2018-12-18T02:00:07Z",
        "lastUpdatedBy": "Mark Png",
        "dateActivated": null,
        "authorisations": [
            "App\\Http\\Controllers\\UserController@index",
            "App\\Http\\Controllers\\UserController@store",
            "App\\Http\\Controllers\\UserController@show",
            "App\\Http\\Controllers\\UserController@update",
            "App\\Http\\Controllers\\UserController@archive",
            "App\\Http\\Controllers\\UserController@destroy",
            "App\\Http\\Controllers\\UserController@restore",
            "App\\Http\\Controllers\\CourseController@index",
            "App\\Http\\Controllers\\CourseController@store",
            "App\\Http\\Controllers\\CourseController@show",
            "App\\Http\\Controllers\\CourseController@update",
            "App\\Http\\Controllers\\CourseController@archive",
            "App\\Http\\Controllers\\CourseController@destroy",
            "App\\Http\\Controllers\\CourseController@restore",
            "App\\Http\\Controllers\\AccountController@index",
            "App\\Http\\Controllers\\AccountController@store",
            "App\\Http\\Controllers\\AccountController@show",
            "App\\Http\\Controllers\\AccountController@update",
            "App\\Http\\Controllers\\AccountUserController@index",
            "App\\Http\\Controllers\\AccountCourseUserController@index",
            "App\\Http\\Controllers\\AccountCourseUserController@store",
            "App\\Http\\Controllers\\AccountCourseUserController@remove",
            "App\\Http\\Controllers\\AccountCourseUserController@update",
            "App\\Http\\Controllers\\CourseUserController@index",
            "App\\Http\\Controllers\\CourseUserController@teachersNotIn",
            "App\\Http\\Controllers\\ModuleController@index",
            "App\\Http\\Controllers\\ModuleController@store",
            "App\\Http\\Controllers\\ModuleController@show",
            "App\\Http\\Controllers\\ModuleController@update",
            "App\\Http\\Controllers\\ModuleController@archive",
            "App\\Http\\Controllers\\ModuleController@destroy",
            "App\\Http\\Controllers\\ModuleController@restore",
            "App\\Http\\Controllers\\StudentController@index",
            "App\\Http\\Controllers\\StudentController@storeManual",
            "App\\Http\\Controllers\\StudentController@storePasted",
            "App\\Http\\Controllers\\StudentController@storeUploaded",
            "App\\Http\\Controllers\\StudentController@storeGeneric",
            "App\\Http\\Controllers\\StudentController@remove",
            "App\\Http\\Controllers\\StudentController@sendInvites",
            "App\\Http\\Controllers\\StudentController@assignRandom",
            "App\\Http\\Controllers\\ CourseSectionController@bulkUpdateTeam",
            "App\\Http\\Controllers\\QuestionController@index",
            "App\\Http\\Controllers\\QuestionController@store",
            "App\\Http\\Controllers\\QuestionController@show",
            "App\\Http\\Controllers\\QuestionController@update",
            "App\\Http\\Controllers\\QuestionController@archive",
            "App\\Http\\Controllers\\QuestionController@destroy",
            "App\\Http\\Controllers\\QuestionController@restore",
            "App\\Http\\Controllers\\ActivityController@index",
            "App\\Http\\Controllers\\ActivityController@store",
            "App\\Http\\Controllers\\ActivityController@show",
            "App\\Http\\Controllers\\ActivityController@update",
            "App\\Http\\Controllers\\ActivityController@archive",
            "App\\Http\\Controllers\\ActivityController@destroy",
            "App\\Http\\Controllers\\ActivityController@restore",
            "App\\Http\\Controllers\\UserController@activityLog",
            "App\\Http\\Controllers\\PaymentPlanController@store",
            "App\\Http\\Controllers\\PaymentPlanController@update",
            "App\\Http\\Controllers\\PaymentPlanController@destroy",
            "App\\Http\\Controllers\\PaymentPlanController@restore"
        ],
        "courses": [
            {
                "accountType": "Admin",
                "uuid": "9df8a17b-ba0e-4f52-9b6b-9c19b77f0c4f",
                "description": "<p>Test Audit</p>",
                "descriptionIsHTML": true,
                "consumerKeyLTI": "SuE6qps4UJlVZKHweBIM",
                "sharedSecretLTI": "QzgulxAycDdIBwF9Z1sG",
                "code": "TA-13",
                "startDate": "2018-07-23T07:00:00Z",
                "endDate": "2018-07-26T07:00:00Z",
                "isPublished": true,
                "objectives": null,
                "configURLLTI": "v3-dev.intedashboard.com/lti/config/SuE6qps4UJlVZKHweBIM",
                "launchURLLTI": "v3-dev.intedashboard.com/lti/launch/SuE6qps4UJlVZKHweBIM",
                "isArchived": false,
                "isTrashed": false,
                "dateCreated": "2018-10-25T09:24:50Z",
                "lastModified": "2018-10-25T09:24:50Z"
            },
            {
                "accountType": "Owner",
                "uuid": "2738854d-a4f3-4fa4-8df1-3a19f3bb363f",
                "description": "<p>Test Audit</p>",
                "descriptionIsHTML": true,
                "consumerKeyLTI": "ZnTW8bRlE9GxpOCo73IP",
                "sharedSecretLTI": "ebyhqoxVu30cdKSJ5XvG",
                "code": "TA-14",
                "startDate": "2018-07-23T07:00:00Z",
                "endDate": "2018-07-26T07:00:00Z",
                "isPublished": true,
                "objectives": {
                    "values": [
                        "Test1",
                        "Test2"
                    ]
                },
                "configURLLTI": "v3-dev.intedashboard.com/lti/config/ZnTW8bRlE9GxpOCo73IP",
                "launchURLLTI": "v3-dev.intedashboard.com/lti/launch/ZnTW8bRlE9GxpOCo73IP",
                "isArchived": false,
                "isTrashed": false,
                "dateCreated": "2018-12-07T04:40:04Z",
                "lastModified": "2018-12-07T04:40:04Z"
            },
            {
                "accountType": "Owner",
                "uuid": "fcc79bed-1198-491c-bf8e-3c13070d5178",
                "description": "<p>Test Audit</p>",
                "descriptionIsHTML": true,
                "consumerKeyLTI": "zEgl0Whjv6F3uO7LrA2G",
                "sharedSecretLTI": "tR3mBgsnGQ9zaHUp2ZYi",
                "code": "TA-15",
                "startDate": "2018-07-23T07:00:00Z",
                "endDate": "2018-07-26T07:00:00Z",
                "isPublished": true,
                "objectives": {
                    "values": [
                        "Test1",
                        "Test2"
                    ]
                },
                "configURLLTI": "v3-dev.intedashboard.com/lti/config/zEgl0Whjv6F3uO7LrA2G",
                "launchURLLTI": "v3-dev.intedashboard.com/lti/launch/zEgl0Whjv6F3uO7LrA2G",
                "isArchived": false,
                "isTrashed": false,
                "dateCreated": "2018-12-07T04:42:53Z",
                "lastModified": "2018-12-07T04:42:53Z"
            },
            {
                "accountType": "Owner",
                "uuid": "000981fd-c0c2-4509-ada8-17630215d14f",
                "description": "<p>Test Audit</p>",
                "descriptionIsHTML": true,
                "consumerKeyLTI": "HdaxOQrKmZWR4XDzpYyT",
                "sharedSecretLTI": "GiXed0wAM8uybo2ZETn3",
                "code": "TA-16",
                "startDate": "2018-07-23T07:00:00Z",
                "endDate": "2018-07-26T07:00:00Z",
                "isPublished": true,
                "objectives": [
                    "O1",
                    "O2",
                    "O3"
                ],
                "configURLLTI": "v3-dev.intedashboard.com/lti/config/HdaxOQrKmZWR4XDzpYyT",
                "launchURLLTI": "v3-dev.intedashboard.com/lti/launch/HdaxOQrKmZWR4XDzpYyT",
                "isArchived": false,
                "isTrashed": false,
                "dateCreated": "2018-12-10T03:15:11Z",
                "lastModified": "2018-12-10T03:15:11Z"
            },
            {
                "accountType": "Owner",
                "uuid": "71c18162-8b17-490c-8d74-545bd0ee65e5",
                "description": "<p>Test Create 1</p>",
                "descriptionIsHTML": true,
                "consumerKeyLTI": "a5ikQrcRmPy31j9f8NzF",
                "sharedSecretLTI": "eglrvN9xdGUmwRJS5A7B",
                "code": "TA-17",
                "startDate": "2018-07-23T07:00:00Z",
                "endDate": "2018-07-26T07:00:00Z",
                "isPublished": true,
                "objectives": [
                    "O1"
                ],
                "configURLLTI": "v3-dev.intedashboard.com/lti/config/a5ikQrcRmPy31j9f8NzF",
                "launchURLLTI": "v3-dev.intedashboard.com/lti/launch/a5ikQrcRmPy31j9f8NzF",
                "isArchived": false,
                "isTrashed": false,
                "dateCreated": "2018-12-10T03:25:05Z",
                "lastModified": "2018-12-10T03:25:05Z"
            },
            {
                "accountType": "Owner",
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

> 404

```json
{
  "error": {
    "message": "Not found.",
    "status_code": 404
  }
}
```

This resource retrieve specific user.

### HTTP Request

`GET [BASE_URL]/users/`**uuid**

URI Parameter | Type | Description
--------- | ------- | -----------
uuid | string | The generated UUID of the selected user.

### HTTP Get Parameters

`No HTTP get parameters required.`

### Request Headers
Key | Value | Description
--------- | ------- | -----------
`Content-Type` | **application/json** | Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
`Authorization` | **Bearer $token** | Lorem ipsum dolor sit amet, consectetur adipiscing elit.


### HTTP Post Parameters

`No HTTP post parameters required.`









## Update User

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
        "identity": "1-ninomichaelangelosoliven+2@gmail.com",
        "email": "ninomichaelangelosoliven+2@gmail.com",
        "firstname": "Michael Angelo11",
        "lastname": "Soliven11",
        "displayName": "Michael Angelo Soliven",
        "accountType": null,
        "isActive": true,
        "isSuspended": false,
        "isDeletable": true,
        "roleId": 2,
        "role": "Account Admin",
        "dateSuspended": null,
        "dateLastLogin": "2018-12-10T02:40:29Z",
        "dateTempPasswordRequested": null,
        "uuid": "deb49db3-99a3-4f7a-bd98-86a6ef46111b",
        "isArchived": false,
        "isTrashed": false,
        "dateCreated": "2018-09-05T05:09:46Z",
        "createBy": "Mark Png",
        "lastModified": "2018-12-18T02:00:07Z",
        "lastUpdatedBy": "Mark Png",
        "dateActivated": null,
        "authorisations": [
            "App\\Http\\Controllers\\UserController@index",
            "App\\Http\\Controllers\\UserController@store",
            "App\\Http\\Controllers\\UserController@show",
            "App\\Http\\Controllers\\UserController@update",
            "App\\Http\\Controllers\\UserController@archive",
            "App\\Http\\Controllers\\UserController@destroy",
            "App\\Http\\Controllers\\UserController@restore",
            "App\\Http\\Controllers\\CourseController@index",
            "App\\Http\\Controllers\\CourseController@store",
            "App\\Http\\Controllers\\CourseController@show",
            "App\\Http\\Controllers\\CourseController@update",
            "App\\Http\\Controllers\\CourseController@archive",
            "App\\Http\\Controllers\\CourseController@destroy",
            "App\\Http\\Controllers\\CourseController@restore",
            "App\\Http\\Controllers\\AccountController@index",
            "App\\Http\\Controllers\\AccountController@store",
            "App\\Http\\Controllers\\AccountController@show",
            "App\\Http\\Controllers\\AccountController@update",
            "App\\Http\\Controllers\\AccountUserController@index",
            "App\\Http\\Controllers\\AccountCourseUserController@index",
            "App\\Http\\Controllers\\AccountCourseUserController@store",
            "App\\Http\\Controllers\\AccountCourseUserController@remove",
            "App\\Http\\Controllers\\AccountCourseUserController@update",
            "App\\Http\\Controllers\\CourseUserController@index",
            "App\\Http\\Controllers\\CourseUserController@teachersNotIn",
            "App\\Http\\Controllers\\ModuleController@index",
            "App\\Http\\Controllers\\ModuleController@store",
            "App\\Http\\Controllers\\ModuleController@show",
            "App\\Http\\Controllers\\ModuleController@update",
            "App\\Http\\Controllers\\ModuleController@archive",
            "App\\Http\\Controllers\\ModuleController@destroy",
            "App\\Http\\Controllers\\ModuleController@restore",
            "App\\Http\\Controllers\\StudentController@index",
            "App\\Http\\Controllers\\StudentController@storeManual",
            "App\\Http\\Controllers\\StudentController@storePasted",
            "App\\Http\\Controllers\\StudentController@storeUploaded",
            "App\\Http\\Controllers\\StudentController@storeGeneric",
            "App\\Http\\Controllers\\StudentController@remove",
            "App\\Http\\Controllers\\StudentController@sendInvites",
            "App\\Http\\Controllers\\StudentController@assignRandom",
            "App\\Http\\Controllers\\ CourseSectionController@bulkUpdateTeam",
            "App\\Http\\Controllers\\QuestionController@index",
            "App\\Http\\Controllers\\QuestionController@store",
            "App\\Http\\Controllers\\QuestionController@show",
            "App\\Http\\Controllers\\QuestionController@update",
            "App\\Http\\Controllers\\QuestionController@archive",
            "App\\Http\\Controllers\\QuestionController@destroy",
            "App\\Http\\Controllers\\QuestionController@restore",
            "App\\Http\\Controllers\\ActivityController@index",
            "App\\Http\\Controllers\\ActivityController@store",
            "App\\Http\\Controllers\\ActivityController@show",
            "App\\Http\\Controllers\\ActivityController@update",
            "App\\Http\\Controllers\\ActivityController@archive",
            "App\\Http\\Controllers\\ActivityController@destroy",
            "App\\Http\\Controllers\\ActivityController@restore",
            "App\\Http\\Controllers\\UserController@activityLog",
            "App\\Http\\Controllers\\PaymentPlanController@store",
            "App\\Http\\Controllers\\PaymentPlanController@update",
            "App\\Http\\Controllers\\PaymentPlanController@destroy",
            "App\\Http\\Controllers\\PaymentPlanController@restore"
        ],
        "courses": [
            {
                "accountType": "Admin",
                "uuid": "9df8a17b-ba0e-4f52-9b6b-9c19b77f0c4f",
                "description": "<p>Test Audit</p>",
                "descriptionIsHTML": true,
                "consumerKeyLTI": "SuE6qps4UJlVZKHweBIM",
                "sharedSecretLTI": "QzgulxAycDdIBwF9Z1sG",
                "code": "TA-13",
                "startDate": "2018-07-23T07:00:00Z",
                "endDate": "2018-07-26T07:00:00Z",
                "isPublished": true,
                "objectives": null,
                "configURLLTI": "v3-dev.intedashboard.com/lti/config/SuE6qps4UJlVZKHweBIM",
                "launchURLLTI": "v3-dev.intedashboard.com/lti/launch/SuE6qps4UJlVZKHweBIM",
                "isArchived": false,
                "isTrashed": false,
                "dateCreated": "2018-10-25T09:24:50Z",
                "lastModified": "2018-10-25T09:24:50Z"
            },
            {
                "accountType": "Owner",
                "uuid": "2738854d-a4f3-4fa4-8df1-3a19f3bb363f",
                "description": "<p>Test Audit</p>",
                "descriptionIsHTML": true,
                "consumerKeyLTI": "ZnTW8bRlE9GxpOCo73IP",
                "sharedSecretLTI": "ebyhqoxVu30cdKSJ5XvG",
                "code": "TA-14",
                "startDate": "2018-07-23T07:00:00Z",
                "endDate": "2018-07-26T07:00:00Z",
                "isPublished": true,
                "objectives": {
                    "values": [
                        "Test1",
                        "Test2"
                    ]
                },
                "configURLLTI": "v3-dev.intedashboard.com/lti/config/ZnTW8bRlE9GxpOCo73IP",
                "launchURLLTI": "v3-dev.intedashboard.com/lti/launch/ZnTW8bRlE9GxpOCo73IP",
                "isArchived": false,
                "isTrashed": false,
                "dateCreated": "2018-12-07T04:40:04Z",
                "lastModified": "2018-12-07T04:40:04Z"
            },
            {
                "accountType": "Owner",
                "uuid": "fcc79bed-1198-491c-bf8e-3c13070d5178",
                "description": "<p>Test Audit</p>",
                "descriptionIsHTML": true,
                "consumerKeyLTI": "zEgl0Whjv6F3uO7LrA2G",
                "sharedSecretLTI": "tR3mBgsnGQ9zaHUp2ZYi",
                "code": "TA-15",
                "startDate": "2018-07-23T07:00:00Z",
                "endDate": "2018-07-26T07:00:00Z",
                "isPublished": true,
                "objectives": {
                    "values": [
                        "Test1",
                        "Test2"
                    ]
                },
                "configURLLTI": "v3-dev.intedashboard.com/lti/config/zEgl0Whjv6F3uO7LrA2G",
                "launchURLLTI": "v3-dev.intedashboard.com/lti/launch/zEgl0Whjv6F3uO7LrA2G",
                "isArchived": false,
                "isTrashed": false,
                "dateCreated": "2018-12-07T04:42:53Z",
                "lastModified": "2018-12-07T04:42:53Z"
            },
            {
                "accountType": "Owner",
                "uuid": "000981fd-c0c2-4509-ada8-17630215d14f",
                "description": "<p>Test Audit</p>",
                "descriptionIsHTML": true,
                "consumerKeyLTI": "HdaxOQrKmZWR4XDzpYyT",
                "sharedSecretLTI": "GiXed0wAM8uybo2ZETn3",
                "code": "TA-16",
                "startDate": "2018-07-23T07:00:00Z",
                "endDate": "2018-07-26T07:00:00Z",
                "isPublished": true,
                "objectives": [
                    "O1",
                    "O2",
                    "O3"
                ],
                "configURLLTI": "v3-dev.intedashboard.com/lti/config/HdaxOQrKmZWR4XDzpYyT",
                "launchURLLTI": "v3-dev.intedashboard.com/lti/launch/HdaxOQrKmZWR4XDzpYyT",
                "isArchived": false,
                "isTrashed": false,
                "dateCreated": "2018-12-10T03:15:11Z",
                "lastModified": "2018-12-10T03:15:11Z"
            },
            {
                "accountType": "Owner",
                "uuid": "71c18162-8b17-490c-8d74-545bd0ee65e5",
                "description": "<p>Test Create 1</p>",
                "descriptionIsHTML": true,
                "consumerKeyLTI": "a5ikQrcRmPy31j9f8NzF",
                "sharedSecretLTI": "eglrvN9xdGUmwRJS5A7B",
                "code": "TA-17",
                "startDate": "2018-07-23T07:00:00Z",
                "endDate": "2018-07-26T07:00:00Z",
                "isPublished": true,
                "objectives": [
                    "O1"
                ],
                "configURLLTI": "v3-dev.intedashboard.com/lti/config/a5ikQrcRmPy31j9f8NzF",
                "launchURLLTI": "v3-dev.intedashboard.com/lti/launch/a5ikQrcRmPy31j9f8NzF",
                "isArchived": false,
                "isTrashed": false,
                "dateCreated": "2018-12-10T03:25:05Z",
                "lastModified": "2018-12-10T03:25:05Z"
            },
            {
                "accountType": "Owner",
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
    "email": [
      "The email is invalid."
    ],
    "roleId": [
      "The selected role id is invalid."
    ],
    "accountUuid": [
      "The selected account uuid is invalid."
    ],
    "password": [
      "The password must be at least 8 characters.",
      "The password confirmation does not match.",
      "Password must contain uppercase character(s).",
      "Password must contain lowercase character(s).",
      "Password must contain special character(s).",
      "Password must contain numeric character(s)."
    ],
    "password_confirmation": [
      "The password confirmation field is required."
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

This resource update selected user.

### HTTP Request

`PUT [BASE_URL]/users/`**uuid**

URI Parameter | Type | Description
--------- | ------- | -----------
uuid | string | The generated UUID of the selected user.

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
identity | **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
email | **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
firstname | **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
roleId | **int** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
accountUuid <br /> `required`| **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
password | **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
password_confirmation <br /> `required if isset(password)`| **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
isActive | **boolean** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.






## Archive/Unarchive User

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
        "identity": "1-ninomichaelangelosoliven+2@gmail.com",
        "email": "ninomichaelangelosoliven+2@gmail.com",
        "firstname": "Michael Angelo11",
        "lastname": "Soliven11",
        "displayName": "Michael Angelo Soliven",
        "accountType": null,
        "isActive": true,
        "isSuspended": false,
        "isDeletable": true,
        "roleId": 2,
        "role": "Account Admin",
        "dateSuspended": null,
        "dateLastLogin": "2018-12-10T02:40:29Z",
        "dateTempPasswordRequested": null,
        "uuid": "deb49db3-99a3-4f7a-bd98-86a6ef46111b",
        "isArchived": false,
        "isTrashed": false,
        "dateCreated": "2018-09-05T05:09:46Z",
        "createBy": "Mark Png",
        "lastModified": "2018-12-18T02:00:07Z",
        "lastUpdatedBy": "Mark Png",
        "dateActivated": null,
        "authorisations": [
            "App\\Http\\Controllers\\UserController@index",
            "App\\Http\\Controllers\\UserController@store",
            "App\\Http\\Controllers\\UserController@show",
            "App\\Http\\Controllers\\UserController@update",
            "App\\Http\\Controllers\\UserController@archive",
            "App\\Http\\Controllers\\UserController@destroy",
            "App\\Http\\Controllers\\UserController@restore",
            "App\\Http\\Controllers\\CourseController@index",
            "App\\Http\\Controllers\\CourseController@store",
            "App\\Http\\Controllers\\CourseController@show",
            "App\\Http\\Controllers\\CourseController@update",
            "App\\Http\\Controllers\\CourseController@archive",
            "App\\Http\\Controllers\\CourseController@destroy",
            "App\\Http\\Controllers\\CourseController@restore",
            "App\\Http\\Controllers\\AccountController@index",
            "App\\Http\\Controllers\\AccountController@store",
            "App\\Http\\Controllers\\AccountController@show",
            "App\\Http\\Controllers\\AccountController@update",
            "App\\Http\\Controllers\\AccountUserController@index",
            "App\\Http\\Controllers\\AccountCourseUserController@index",
            "App\\Http\\Controllers\\AccountCourseUserController@store",
            "App\\Http\\Controllers\\AccountCourseUserController@remove",
            "App\\Http\\Controllers\\AccountCourseUserController@update",
            "App\\Http\\Controllers\\CourseUserController@index",
            "App\\Http\\Controllers\\CourseUserController@teachersNotIn",
            "App\\Http\\Controllers\\ModuleController@index",
            "App\\Http\\Controllers\\ModuleController@store",
            "App\\Http\\Controllers\\ModuleController@show",
            "App\\Http\\Controllers\\ModuleController@update",
            "App\\Http\\Controllers\\ModuleController@archive",
            "App\\Http\\Controllers\\ModuleController@destroy",
            "App\\Http\\Controllers\\ModuleController@restore",
            "App\\Http\\Controllers\\StudentController@index",
            "App\\Http\\Controllers\\StudentController@storeManual",
            "App\\Http\\Controllers\\StudentController@storePasted",
            "App\\Http\\Controllers\\StudentController@storeUploaded",
            "App\\Http\\Controllers\\StudentController@storeGeneric",
            "App\\Http\\Controllers\\StudentController@remove",
            "App\\Http\\Controllers\\StudentController@sendInvites",
            "App\\Http\\Controllers\\StudentController@assignRandom",
            "App\\Http\\Controllers\\ CourseSectionController@bulkUpdateTeam",
            "App\\Http\\Controllers\\QuestionController@index",
            "App\\Http\\Controllers\\QuestionController@store",
            "App\\Http\\Controllers\\QuestionController@show",
            "App\\Http\\Controllers\\QuestionController@update",
            "App\\Http\\Controllers\\QuestionController@archive",
            "App\\Http\\Controllers\\QuestionController@destroy",
            "App\\Http\\Controllers\\QuestionController@restore",
            "App\\Http\\Controllers\\ActivityController@index",
            "App\\Http\\Controllers\\ActivityController@store",
            "App\\Http\\Controllers\\ActivityController@show",
            "App\\Http\\Controllers\\ActivityController@update",
            "App\\Http\\Controllers\\ActivityController@archive",
            "App\\Http\\Controllers\\ActivityController@destroy",
            "App\\Http\\Controllers\\ActivityController@restore",
            "App\\Http\\Controllers\\UserController@activityLog",
            "App\\Http\\Controllers\\PaymentPlanController@store",
            "App\\Http\\Controllers\\PaymentPlanController@update",
            "App\\Http\\Controllers\\PaymentPlanController@destroy",
            "App\\Http\\Controllers\\PaymentPlanController@restore"
        ],
        "courses": [
            {
                "accountType": "Admin",
                "uuid": "9df8a17b-ba0e-4f52-9b6b-9c19b77f0c4f",
                "description": "<p>Test Audit</p>",
                "descriptionIsHTML": true,
                "consumerKeyLTI": "SuE6qps4UJlVZKHweBIM",
                "sharedSecretLTI": "QzgulxAycDdIBwF9Z1sG",
                "code": "TA-13",
                "startDate": "2018-07-23T07:00:00Z",
                "endDate": "2018-07-26T07:00:00Z",
                "isPublished": true,
                "objectives": null,
                "configURLLTI": "v3-dev.intedashboard.com/lti/config/SuE6qps4UJlVZKHweBIM",
                "launchURLLTI": "v3-dev.intedashboard.com/lti/launch/SuE6qps4UJlVZKHweBIM",
                "isArchived": false,
                "isTrashed": false,
                "dateCreated": "2018-10-25T09:24:50Z",
                "lastModified": "2018-10-25T09:24:50Z"
            },
            {
                "accountType": "Owner",
                "uuid": "2738854d-a4f3-4fa4-8df1-3a19f3bb363f",
                "description": "<p>Test Audit</p>",
                "descriptionIsHTML": true,
                "consumerKeyLTI": "ZnTW8bRlE9GxpOCo73IP",
                "sharedSecretLTI": "ebyhqoxVu30cdKSJ5XvG",
                "code": "TA-14",
                "startDate": "2018-07-23T07:00:00Z",
                "endDate": "2018-07-26T07:00:00Z",
                "isPublished": true,
                "objectives": {
                    "values": [
                        "Test1",
                        "Test2"
                    ]
                },
                "configURLLTI": "v3-dev.intedashboard.com/lti/config/ZnTW8bRlE9GxpOCo73IP",
                "launchURLLTI": "v3-dev.intedashboard.com/lti/launch/ZnTW8bRlE9GxpOCo73IP",
                "isArchived": false,
                "isTrashed": false,
                "dateCreated": "2018-12-07T04:40:04Z",
                "lastModified": "2018-12-07T04:40:04Z"
            },
            {
                "accountType": "Owner",
                "uuid": "fcc79bed-1198-491c-bf8e-3c13070d5178",
                "description": "<p>Test Audit</p>",
                "descriptionIsHTML": true,
                "consumerKeyLTI": "zEgl0Whjv6F3uO7LrA2G",
                "sharedSecretLTI": "tR3mBgsnGQ9zaHUp2ZYi",
                "code": "TA-15",
                "startDate": "2018-07-23T07:00:00Z",
                "endDate": "2018-07-26T07:00:00Z",
                "isPublished": true,
                "objectives": {
                    "values": [
                        "Test1",
                        "Test2"
                    ]
                },
                "configURLLTI": "v3-dev.intedashboard.com/lti/config/zEgl0Whjv6F3uO7LrA2G",
                "launchURLLTI": "v3-dev.intedashboard.com/lti/launch/zEgl0Whjv6F3uO7LrA2G",
                "isArchived": false,
                "isTrashed": false,
                "dateCreated": "2018-12-07T04:42:53Z",
                "lastModified": "2018-12-07T04:42:53Z"
            },
            {
                "accountType": "Owner",
                "uuid": "000981fd-c0c2-4509-ada8-17630215d14f",
                "description": "<p>Test Audit</p>",
                "descriptionIsHTML": true,
                "consumerKeyLTI": "HdaxOQrKmZWR4XDzpYyT",
                "sharedSecretLTI": "GiXed0wAM8uybo2ZETn3",
                "code": "TA-16",
                "startDate": "2018-07-23T07:00:00Z",
                "endDate": "2018-07-26T07:00:00Z",
                "isPublished": true,
                "objectives": [
                    "O1",
                    "O2",
                    "O3"
                ],
                "configURLLTI": "v3-dev.intedashboard.com/lti/config/HdaxOQrKmZWR4XDzpYyT",
                "launchURLLTI": "v3-dev.intedashboard.com/lti/launch/HdaxOQrKmZWR4XDzpYyT",
                "isArchived": false,
                "isTrashed": false,
                "dateCreated": "2018-12-10T03:15:11Z",
                "lastModified": "2018-12-10T03:15:11Z"
            },
            {
                "accountType": "Owner",
                "uuid": "71c18162-8b17-490c-8d74-545bd0ee65e5",
                "description": "<p>Test Create 1</p>",
                "descriptionIsHTML": true,
                "consumerKeyLTI": "a5ikQrcRmPy31j9f8NzF",
                "sharedSecretLTI": "eglrvN9xdGUmwRJS5A7B",
                "code": "TA-17",
                "startDate": "2018-07-23T07:00:00Z",
                "endDate": "2018-07-26T07:00:00Z",
                "isPublished": true,
                "objectives": [
                    "O1"
                ],
                "configURLLTI": "v3-dev.intedashboard.com/lti/config/a5ikQrcRmPy31j9f8NzF",
                "launchURLLTI": "v3-dev.intedashboard.com/lti/launch/a5ikQrcRmPy31j9f8NzF",
                "isArchived": false,
                "isTrashed": false,
                "dateCreated": "2018-12-10T03:25:05Z",
                "lastModified": "2018-12-10T03:25:05Z"
            },
            {
                "accountType": "Owner",
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

> 404

```json
{
  "error": {
    "message": "Not found.",
    "status_code": 404
  }
}
```

This resource archive/unarchive selected user.

### HTTP Request

`PATCH [BASE_URL]/users/`**uuid**

URI Parameter | Type | Description
--------- | ------- | -----------
uuid | string | The generated UUID of the selected user.

### HTTP Get Parameters

`No HTTP get parameters required.`

### Request Headers
Key | Value | Description
--------- | ------- | -----------
`Content-Type` | **application/json** | Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
`Authorization` | **Bearer $token** | Lorem ipsum dolor sit amet, consectetur adipiscing elit.


### HTTP Post Parameters

`No HTTP post parameters required.`









## Trash User

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

This resource trash selected user.

### HTTP Request

`DELETE [BASE_URL]/users/`**uuid**

URI Parameter | Type | Description
--------- | ------- | -----------
uuid | string | The generated UUID of the selected user.

### HTTP Get Parameters

`No HTTP get parameters required.`

### Request Headers
Key | Value | Description
--------- | ------- | -----------
`Content-Type` | **application/json** | Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
`Authorization` | **Bearer $token** | Lorem ipsum dolor sit amet, consectetur adipiscing elit.


### HTTP Post Parameters

`No HTTP post parameters required.`






## Untrash User

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
        "identity": "1-ninomichaelangelosoliven+2@gmail.com",
        "email": "ninomichaelangelosoliven+2@gmail.com",
        "firstname": "Michael Angelo11",
        "lastname": "Soliven11",
        "displayName": "Michael Angelo Soliven",
        "accountType": null,
        "isActive": true,
        "isSuspended": false,
        "isDeletable": true,
        "roleId": 2,
        "role": "Account Admin",
        "dateSuspended": null,
        "dateLastLogin": "2018-12-10T02:40:29Z",
        "dateTempPasswordRequested": null,
        "uuid": "deb49db3-99a3-4f7a-bd98-86a6ef46111b",
        "isArchived": false,
        "isTrashed": false,
        "dateCreated": "2018-09-05T05:09:46Z",
        "createBy": "Mark Png",
        "lastModified": "2018-12-18T02:00:07Z",
        "lastUpdatedBy": "Mark Png",
        "dateActivated": null,
        "authorisations": [
            "App\\Http\\Controllers\\UserController@index",
            "App\\Http\\Controllers\\UserController@store",
            "App\\Http\\Controllers\\UserController@show",
            "App\\Http\\Controllers\\UserController@update",
            "App\\Http\\Controllers\\UserController@archive",
            "App\\Http\\Controllers\\UserController@destroy",
            "App\\Http\\Controllers\\UserController@restore",
            "App\\Http\\Controllers\\CourseController@index",
            "App\\Http\\Controllers\\CourseController@store",
            "App\\Http\\Controllers\\CourseController@show",
            "App\\Http\\Controllers\\CourseController@update",
            "App\\Http\\Controllers\\CourseController@archive",
            "App\\Http\\Controllers\\CourseController@destroy",
            "App\\Http\\Controllers\\CourseController@restore",
            "App\\Http\\Controllers\\AccountController@index",
            "App\\Http\\Controllers\\AccountController@store",
            "App\\Http\\Controllers\\AccountController@show",
            "App\\Http\\Controllers\\AccountController@update",
            "App\\Http\\Controllers\\AccountUserController@index",
            "App\\Http\\Controllers\\AccountCourseUserController@index",
            "App\\Http\\Controllers\\AccountCourseUserController@store",
            "App\\Http\\Controllers\\AccountCourseUserController@remove",
            "App\\Http\\Controllers\\AccountCourseUserController@update",
            "App\\Http\\Controllers\\CourseUserController@index",
            "App\\Http\\Controllers\\CourseUserController@teachersNotIn",
            "App\\Http\\Controllers\\ModuleController@index",
            "App\\Http\\Controllers\\ModuleController@store",
            "App\\Http\\Controllers\\ModuleController@show",
            "App\\Http\\Controllers\\ModuleController@update",
            "App\\Http\\Controllers\\ModuleController@archive",
            "App\\Http\\Controllers\\ModuleController@destroy",
            "App\\Http\\Controllers\\ModuleController@restore",
            "App\\Http\\Controllers\\StudentController@index",
            "App\\Http\\Controllers\\StudentController@storeManual",
            "App\\Http\\Controllers\\StudentController@storePasted",
            "App\\Http\\Controllers\\StudentController@storeUploaded",
            "App\\Http\\Controllers\\StudentController@storeGeneric",
            "App\\Http\\Controllers\\StudentController@remove",
            "App\\Http\\Controllers\\StudentController@sendInvites",
            "App\\Http\\Controllers\\StudentController@assignRandom",
            "App\\Http\\Controllers\\ CourseSectionController@bulkUpdateTeam",
            "App\\Http\\Controllers\\QuestionController@index",
            "App\\Http\\Controllers\\QuestionController@store",
            "App\\Http\\Controllers\\QuestionController@show",
            "App\\Http\\Controllers\\QuestionController@update",
            "App\\Http\\Controllers\\QuestionController@archive",
            "App\\Http\\Controllers\\QuestionController@destroy",
            "App\\Http\\Controllers\\QuestionController@restore",
            "App\\Http\\Controllers\\ActivityController@index",
            "App\\Http\\Controllers\\ActivityController@store",
            "App\\Http\\Controllers\\ActivityController@show",
            "App\\Http\\Controllers\\ActivityController@update",
            "App\\Http\\Controllers\\ActivityController@archive",
            "App\\Http\\Controllers\\ActivityController@destroy",
            "App\\Http\\Controllers\\ActivityController@restore",
            "App\\Http\\Controllers\\UserController@activityLog",
            "App\\Http\\Controllers\\PaymentPlanController@store",
            "App\\Http\\Controllers\\PaymentPlanController@update",
            "App\\Http\\Controllers\\PaymentPlanController@destroy",
            "App\\Http\\Controllers\\PaymentPlanController@restore"
        ],
        "courses": [
            {
                "accountType": "Admin",
                "uuid": "9df8a17b-ba0e-4f52-9b6b-9c19b77f0c4f",
                "description": "<p>Test Audit</p>",
                "descriptionIsHTML": true,
                "consumerKeyLTI": "SuE6qps4UJlVZKHweBIM",
                "sharedSecretLTI": "QzgulxAycDdIBwF9Z1sG",
                "code": "TA-13",
                "startDate": "2018-07-23T07:00:00Z",
                "endDate": "2018-07-26T07:00:00Z",
                "isPublished": true,
                "objectives": null,
                "configURLLTI": "v3-dev.intedashboard.com/lti/config/SuE6qps4UJlVZKHweBIM",
                "launchURLLTI": "v3-dev.intedashboard.com/lti/launch/SuE6qps4UJlVZKHweBIM",
                "isArchived": false,
                "isTrashed": false,
                "dateCreated": "2018-10-25T09:24:50Z",
                "lastModified": "2018-10-25T09:24:50Z"
            },
            {
                "accountType": "Owner",
                "uuid": "2738854d-a4f3-4fa4-8df1-3a19f3bb363f",
                "description": "<p>Test Audit</p>",
                "descriptionIsHTML": true,
                "consumerKeyLTI": "ZnTW8bRlE9GxpOCo73IP",
                "sharedSecretLTI": "ebyhqoxVu30cdKSJ5XvG",
                "code": "TA-14",
                "startDate": "2018-07-23T07:00:00Z",
                "endDate": "2018-07-26T07:00:00Z",
                "isPublished": true,
                "objectives": {
                    "values": [
                        "Test1",
                        "Test2"
                    ]
                },
                "configURLLTI": "v3-dev.intedashboard.com/lti/config/ZnTW8bRlE9GxpOCo73IP",
                "launchURLLTI": "v3-dev.intedashboard.com/lti/launch/ZnTW8bRlE9GxpOCo73IP",
                "isArchived": false,
                "isTrashed": false,
                "dateCreated": "2018-12-07T04:40:04Z",
                "lastModified": "2018-12-07T04:40:04Z"
            },
            {
                "accountType": "Owner",
                "uuid": "fcc79bed-1198-491c-bf8e-3c13070d5178",
                "description": "<p>Test Audit</p>",
                "descriptionIsHTML": true,
                "consumerKeyLTI": "zEgl0Whjv6F3uO7LrA2G",
                "sharedSecretLTI": "tR3mBgsnGQ9zaHUp2ZYi",
                "code": "TA-15",
                "startDate": "2018-07-23T07:00:00Z",
                "endDate": "2018-07-26T07:00:00Z",
                "isPublished": true,
                "objectives": {
                    "values": [
                        "Test1",
                        "Test2"
                    ]
                },
                "configURLLTI": "v3-dev.intedashboard.com/lti/config/zEgl0Whjv6F3uO7LrA2G",
                "launchURLLTI": "v3-dev.intedashboard.com/lti/launch/zEgl0Whjv6F3uO7LrA2G",
                "isArchived": false,
                "isTrashed": false,
                "dateCreated": "2018-12-07T04:42:53Z",
                "lastModified": "2018-12-07T04:42:53Z"
            },
            {
                "accountType": "Owner",
                "uuid": "000981fd-c0c2-4509-ada8-17630215d14f",
                "description": "<p>Test Audit</p>",
                "descriptionIsHTML": true,
                "consumerKeyLTI": "HdaxOQrKmZWR4XDzpYyT",
                "sharedSecretLTI": "GiXed0wAM8uybo2ZETn3",
                "code": "TA-16",
                "startDate": "2018-07-23T07:00:00Z",
                "endDate": "2018-07-26T07:00:00Z",
                "isPublished": true,
                "objectives": [
                    "O1",
                    "O2",
                    "O3"
                ],
                "configURLLTI": "v3-dev.intedashboard.com/lti/config/HdaxOQrKmZWR4XDzpYyT",
                "launchURLLTI": "v3-dev.intedashboard.com/lti/launch/HdaxOQrKmZWR4XDzpYyT",
                "isArchived": false,
                "isTrashed": false,
                "dateCreated": "2018-12-10T03:15:11Z",
                "lastModified": "2018-12-10T03:15:11Z"
            },
            {
                "accountType": "Owner",
                "uuid": "71c18162-8b17-490c-8d74-545bd0ee65e5",
                "description": "<p>Test Create 1</p>",
                "descriptionIsHTML": true,
                "consumerKeyLTI": "a5ikQrcRmPy31j9f8NzF",
                "sharedSecretLTI": "eglrvN9xdGUmwRJS5A7B",
                "code": "TA-17",
                "startDate": "2018-07-23T07:00:00Z",
                "endDate": "2018-07-26T07:00:00Z",
                "isPublished": true,
                "objectives": [
                    "O1"
                ],
                "configURLLTI": "v3-dev.intedashboard.com/lti/config/a5ikQrcRmPy31j9f8NzF",
                "launchURLLTI": "v3-dev.intedashboard.com/lti/launch/a5ikQrcRmPy31j9f8NzF",
                "isArchived": false,
                "isTrashed": false,
                "dateCreated": "2018-12-10T03:25:05Z",
                "lastModified": "2018-12-10T03:25:05Z"
            },
            {
                "accountType": "Owner",
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

> 404

```json
{
  "error": {
    "message": "Not found.",
    "status_code": 404
  }
}
```

This resource untrash trashed user.

### HTTP Request

`GET [BASE_URL]/users/`**uuid**`/restore`

URI Parameter | Type | Description
--------- | ------- | -----------
uuid | string | The generated UUID of the selected user.

### HTTP Get Parameters

`No HTTP get parameters required.`

### Request Headers
Key | Value | Description
--------- | ------- | -----------
`Content-Type` | **application/json** | Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
`Authorization` | **Bearer $token** | Lorem ipsum dolor sit amet, consectetur adipiscing elit.


### HTTP Post Parameters

`No HTTP post parameters required.`