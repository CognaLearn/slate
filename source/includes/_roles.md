# Roles

<aside class="success">
Resources related to <code>roles management</code>.
</aside>






## List of Roles

> 200

```json
{
    "data": [
        {
            "name": "Superuser",
            "access": "admins",
            "accessLevel": "All",
            "uuid": "1c497772-4af3-4cef-8eb8-e795dff12d7b",
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
            "uuid": "7b9f4fdf-50a4-4826-8d1e-1b881408aa2b",
            "isArchived": false,
            "isTrashed": false,
            "dateCreated": null,
            "lastModified": "2018-09-05T07:32:00Z",
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
            ]
        },
        {
            "name": "Teacher",
            "access": "teachers",
            "accessLevel": "Ownership",
            "uuid": "172b1ada-1110-4456-8195-f4855a50189b",
            "isArchived": false,
            "isTrashed": false,
            "dateCreated": null,
            "lastModified": "2018-09-05T07:32:10Z",
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
                "App\\Http\\Controllers\\StudentController@transfer",
                "App\\Http\\Controllers\\CourseSectionController@store",
                "App\\Http\\Controllers\\CourseSectionController@show",
                "App\\Http\\Controllers\\CourseSectionController@update",
                "App\\Http\\Controllers\\CourseSectionController@destroy",
                "App\\Http\\Controllers\\CourseSectionTeamController@store",
                "App\\Http\\Controllers\\CourseSectionTeamController@show",
                "App\\Http\\Controllers\\CourseSectionTeamController@update",
                "App\\Http\\Controllers\\CourseSectionTeamController@destroy",
                "App\\Http\\Controllers\\CourseUserController@students",
                "App\\Http\\Controllers\\StudentController@bulkTransfer",
                "App\\Http\\Controllers\\CourseSectionController@bulkUpdate",
                "App\\Http\\Controllers\\CourseSectionController@bulkUpdateTeam",
                "App\\Http\\Controllers\\CourseSectionController@bulkDestroy",
                "App\\Http\\Controllers\\CourseSectionController@bulkDestroyTeam",
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
            ]
        },
        {
            "name": "Student",
            "access": "students",
            "accessLevel": "Ownership",
            "uuid": "be063640-8203-4de5-940a-a908d206c037",
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











## Retrieve Role

> 200

```json
{
    "data": {
        "name": "Account Admin",
        "access": "admins",
        "accessLevel": "Organisation",
        "uuid": "7b9f4fdf-50a4-4826-8d1e-1b881408aa2b",
        "isArchived": false,
        "isTrashed": false,
        "dateCreated": null,
        "lastModified": "2018-09-05T07:32:00Z",
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









## Update Role

> 200

```json
{
    "data": {
        "name": "Account Admin",
        "access": "admins",
        "accessLevel": "Organisation",
        "uuid": "7b9f4fdf-50a4-4826-8d1e-1b881408aa2b",
        "isArchived": false,
        "isTrashed": false,
        "dateCreated": null,
        "lastModified": "2018-09-05T07:32:00Z",
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
    "routers.26": [
        "The selected routers.26 is invalid."
    ],
    "name": [
      "The name field is required.",
      "The name has already been taken."
    ],
    "access": [
      "The access field is required.",
      "The selected access is invalid."
    ],
    "accessLevel": [
      "The accessLevel field is required.",
      "The selected accessLevel is invalid."
    ]
  },
  "status_code": 422
}
```

This resource update selected roole.

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