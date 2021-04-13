# Authentication

<aside class="notice">
Resources related to <code>authentication</code>.


Bearer authentication (also called token authentication) is an HTTP authentication scheme that involves security tokens called bearer tokens. The client must send this token in the Authorization header when making requests to protected resources:

<br/><br/>
<code>Authorization: Bearer \<token\></code>.

<br/><br/>
API Authentication requires minimum of two steps (plus an extra step if 2FA is enabled) to generate bearer token.


<ol>
<li><code>/v2/sign-in-verify</code></li>
<li><code>/v2/sign-in</code></li>
<li>(If 2FA is enabled) <code>/v2/sign-in-with-2fa</code></li>
</ol>

</aside>


## Sign-in Verify
> 200

```json
{
   "status_code":200,
   "isLocked":0,
   "result":[
      [
         {
            "role":"Student",
            "loginToken":"2gn2BEDYHIqMOBVFBbX0nm3bvjXWGFBEF0X3YFCoAeYXTKP4XRG5t1qyD4LDtplxsqfiAZwIDbRMDm0d",
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
         }
      ],
      [
         
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

Generates a unique login token for sign-in. If the account has multiple roles attached, multiple login tokens will be generated per role.

### HTTP Request

`POST [BASE_URL]/auth/sign-in-verify`

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

> 200

```json
{
   "status_code":200,
   "isLocked":0,
   "result":[
      [
         {
            "role":"Student",
            "loginToken":"2gn2BEDYHIqMOBVFBbX0nm3bvjXWGFBEF0X3YFCoAeYXTKP4XRG5t1qyD4LDtplxsqfiAZwIDbRMDm0d",
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
         }
      ],
      [
         
      ]
   ]
}
```

> 401

```json
{
	"status_code": 401,
	"message": "Provided login token is invalid."
}
```

If 2FA is enabled, the user will receive an email with a pin that is valid for 15 minutes.

<br/>
If 2FA is disabled, returns the bearer token immediately.

### HTTP Request

`POST [BASE_URL]/auth/sign-in`

### Request Headers

[Standard Request Headers](#principles)

### HTTP Post Parameters
Parameter | Description
--------- | -----------
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

Returns the bearer token. 2FA PIN is required from Step 2 and Login Token from Step 1.

### HTTP Request

`POST [BASE_URL]/auth/sign-in-with-2fa`

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
   "success": true,
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

### Request Headers

[Standard Request Headers](#principles)

### HTTP Post Parameters
Parameter | Description
--------- | -----------
means <br /> `required`| **string** <br /> tokenn or verify.
token <br /> `required`| **string** <br /> Token sent to the email.





