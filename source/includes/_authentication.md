# Authentication

<aside class="notice">
Resources related to <code>authentication</code>.
</aside>


## Sign-in Verify
> 401

```json
{
   "status_code":200,
   "message":"OK",
   "result":[
      [
         {
            "role":"Account Admin",
            "loginToken":"jcq48zwORPslEtypnHkG45OJWhyCnVoNMrjAFou6StQH631hFuG4IaJQjRpmd0tWFrPRxjOe5UBHgaJp",
            "is2FAEnabled":false,
            "organisation":{
               "uuid":"08299f88-6223-49aa-84e7-1958d703de6e",
               "accountName":null,
               "organisationName":"Cy's University",
               "isActive":0,
               "isSuspended":0,
               "settings":{
                  "enableLti":false,
                  "mfaForStudents":false,
                  "mfaForTeachers":false,
                  "allowGenericUsers":false,
                  "defaultTratSettings":[
                     5,
                     3,
                     1,
                     0
                  ],
                  "maxFailedSignInAttempts":3
               },
               "isPaid":0
            }
         },
         {
            "role":"Student",
            "loginToken":"YhE6n9w9qdHOZzhJ7GAFiCO67usNJkb4nq8Eq8FEaVhk7iKYn8bImNaLgQCQY7iKqSjCFK10SqMauORO",
            "is2FAEnabled":false,
            "organisation":{
               "uuid":"08299f88-6223-49aa-84e7-1958d703de6e",
               "accountName":null,
               "organisationName":"Cy's University",
               "isActive":0,
               "isSuspended":0,
               "settings":{
                  "enableLti":false,
                  "mfaForStudents":false,
                  "mfaForTeachers":false,
                  "allowGenericUsers":false,
                  "defaultTratSettings":[
                     5,
                     3,
                     1,
                     0
                  ],
                  "maxFailedSignInAttempts":3
               },
               "isPaid":0
            }
         },
         {
            "role":"Teacher",
            "loginToken":"NYFdK8tXyRrDnZ8XtXBc7x9wqMcOKsmDs5XkNxgGPu8VmriwkG75XEdHuIWPvNKeivtlw82i3yG1XAs2",
            "is2FAEnabled":false,
            "organisation":{
               "uuid":"c5a47ef7-eba8-4d7c-805c-3b6cc6abb53c",
               "accountName":null,
               "organisationName":"Brian's University",
               "isActive":0,
               "isSuspended":0,
               "settings":null,
               "isPaid":0
            }
         },
         {
            "role":"Superuser",
            "loginToken":"T5bUK8KBOmUW301XUMSnPuqGypvdLRBSRiPOcYyZkZhxqWx3NMDp2g4hgCzTunJvQFR0UwaTn6EI5lSz",
            "is2FAEnabled":true,
            "organisation":{
               "organisationName":"Superusers"
            }
         },
      ],
      [
         {
            "role":"Account Admin",
            "organisation":{
               "uuid":"f5018d73-5b20-4cca-87a7-aba9d5fd0f6a",
               "accountName":null,
               "organisationName":"Cy",
               "isActive":0,
               "isSuspended":0,
               "settings":null,
               "isPaid":0
            },
            "message":"Identity or Password is invalid."
         },
      ]
   ]
}
```

> 401

```json
{
	"status_code": 401,
	"message": "Password is invalid."
}
```

> 401

```json
{
	"status_code": 401,
	"message": "No user(s) found."
}
```


This resource unpublishes specific activity.

### HTTP Request

`POST [BASE_URL]/auth/sign-in-verify`

### HTTP Get Parameters

`No HTTP get parameters required.`

### Request Headers

[Standard Request Headers](#principles)

### HTTP Post Parameters
Parameter | Description
--------- | -----------
identity <br /> `required`| **string** <br /> Email/identity of the user.
password <br /> `required`| **string** <br /> Password of the user.


**Post Parameters**

Sample post values -->

```
$data[
	{
		"identity": "cy@intedashboard.com",
		"password": "********"
	}
]
```