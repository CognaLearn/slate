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


This resource verify sign-in of specific account.

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

This resource sign-in the token of selected account role.

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






## Sign-in With Two-Factor Authentication
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

This resource sign-in the selected account using Two-Factor Authentication .

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


