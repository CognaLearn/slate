# Authentication

<aside class="notice">
Resources related to <code>authentication</code>.
</aside>


## Sign-in Verify
> 200

```json
{
   "status_code":200,
   "message":"OK",
   "result":[
      [
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


This resource verifies sign-in of specific account.

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



## Sign-in
> 200

```json
{
   "is2FAEnabled": true,
   "loginToken": "T5bUK8KBOmUW301XUMSnPuqGypvdLRBSRiPOcYyZkZhxqWx3NMDp2g4hgCzTunJvQFR0UwaTn6EI5lSz"
}
```

> 401

```json
{
	"status_code": 401,
	"message": "Provided login token is invalid."
}
```

This resource signs in the token of selected account role.

### HTTP Request

`POST [BASE_URL]/auth/sign-in`

### HTTP Get Parameters

`No HTTP get parameters required.`

### Request Headers

[Standard Request Headers](#principles)

### HTTP Post Parameters
Parameter | Description
--------- | -----------
is2FAEnabled <br /> `required`| **boolean** <br /> To identify if the organisation requires 2FA.
loginToken <br /> `required`| **string** <br /> Token of the selected account role.






## Sign-in With 2FA
> 200

```json
{
   "loginToken": "T5bUK8KBOmUW301XUMSnPuqGypvdLRBSRiPOcYyZkZhxqWx3NMDp2g4hgCzTunJvQFR0UwaTn6EI5lSz",
   "pin": "000000",
}
```

> 401

```json
{
	"status_code": 401,
	"message": "Provided pin is invalid."
}
```

This resource signs in the selected account using Two-Factor Authentication .

### HTTP Request

`POST [BASE_URL]/auth/sign-in-with-2fa`

### HTTP Get Parameters

`No HTTP get parameters required.`

### Request Headers

[Standard Request Headers](#principles)

### HTTP Post Parameters
Parameter | Description
--------- | -----------
loginToken <br /> `required`| **string** <br /> Token of the selected account role.
pin <br /> `required`| **string** <br /> Pin sent to the email of the user.




## Resend 2FA
> 200

```json
{
   "loginToken": "T5bUK8KBOmUW301XUMSnPuqGypvdLRBSRiPOcYyZkZhxqWx3NMDp2g4hgCzTunJvQFR0UwaTn6EI5lSz",
   "pin": "000000",
}
```

> 422

```json
{
	"message": "422 Unprocessable Entity",
    "errors": {
        "loginToken": [
            "The login token is required."
        ]
    },
    "status_code": 422
}
```

This resource resends the pin for Two-Factor Authentication.

### HTTP Request

`POST [BASE_URL]/auth/resend-2fa`

### HTTP Get Parameters

`No HTTP get parameters required.`

### Request Headers

[Standard Request Headers](#principles)

### HTTP Post Parameters
Parameter | Description
--------- | -----------
loginToken <br /> `required`| **string** <br /> Token of the selected account role.



## Send Token
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
            "The email is required."
        ]
    },
    "status_code": 422
}
```

This resource sends token to the user.

### HTTP Request

`POST [BASE_URL]/password/send-token`

### HTTP Get Parameters

`No HTTP get parameters required.`

### Request Headers

[Standard Request Headers](#principles)

### HTTP Post Parameters
Parameter | Description
--------- | -----------
email <br /> `required`| **string** <br /> Email of the user.




## Reset
> 200

```json
{
   "data":{
      "status_code":200,
      "message":"OK",
      "user":{
         "role":"Student",
         "roleId":4,
         "isDeletable":1,
         "avatar":null,
         "firstname":"Nino",
         "lastname":"Soliven",
         "uuid":"2149a364-c610-4695-a1e6-5aa76be50206",
         "displayName":"Nino Soliven",
         "identity":"nino+1@intedashboard.com",
         "email":"nino+1@intedashboard.com",
         "canAddTeacher":0,
         "canUseExpressSignIn":0,
         "isMultipleUser":false,
         "dateLtiSignin":null,
         "status":"Active",
         "origin":"Email",
         "paidDate":null,
         "account":{
            "uuid":"08299f88-6223-49aa-84e7-1958d703de6e",
            "paymentMethod":"Institution",
            "type":"Free Trial",
            "organisationName":"Cy's University",
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
            "version":"full",
            "paymentPlans":[
               
            ]
         }
      },
      "token":"eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJodHRwOlwvXC8xMjcuMC4wLjE6ODAwMFwvdjJcL3Bhc3N3b3JkXC9yZXNldCIsImlhdCI6MTYxNzg4NDg0OSwibmJmIjoxNjE3ODg0ODQ5LCJqdGkiOiJMNVFPZ1ZNVnJOREtSSTRpIiwic3ViIjoxNjA0MCwicHJ2IjoiODdlMGFmMWVmOWZkMTU4MTJmZGVjOTcxNTNhMTRlMGIwNDc1NDZhYSJ9.Ze-V5OQ_-w8M-TQ6iwbSWrdSOs81ErUTiCOAEbZ_IeU",
      "required_change_password":0,
      "currentTime":1617884849,
      "api_url":"http://127.0.0.1:8000/v2",
      "isGeneric":false
   }
}
```

> 422

```json
{
	"message": "422 Unprocessable Entity",
    "errors": {
        "password": [
            "You cannot reuse old passwords."
        ]
    },
    "status_code": 422
}
```

> 404

```json
{
    "message": "Reset token not found.",
    "status_code": 404
}
```

This resource resets password of the account.

### HTTP Request

`POST [BASE_URL]/password/reset`

### HTTP Get Parameters

`No HTTP get parameters required.`

### Request Headers

[Standard Request Headers](#principles)

### HTTP Post Parameters
Parameter | Description
--------- | -----------
means <br /> `required`| **string** <br /> tokenn or verify.
token <br /> `required`| **string** <br /> Token sent to the email.





