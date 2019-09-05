# Activities

<aside class="notice">
Resources related to <code>activities management</code>.
</aside>





## Unpublish

> 200

```json
{
    "message": "success",
    "status_code": 200
}
```

> 404

```json
{
    "message": "Not Found",
    "status_code": 404
}
```

This resource unpublishes specific activity.

### HTTP Request

`POST [BASE_URL]/activities/{activity-uuid}/unpublish`

### HTTP Get Parameters

`No HTTP get parameters required.`

### Request Headers

[Standard Request Headers](#principles)

### HTTP Post Parameters

`No HTTP post parameters required.`


### Winterbreak Setups

**Request Headers**    

[Standard Winterbreak Headers](#winterbreak)


**Post Parameters**

Sample post values -->

```
$data[
   {
      "users":{
         "students":[
            "42b5273c-876b-44ac-9cbf-c736482c5ed1"
         ],
         "teachers":[
            "e0f0ad43-adea-4aa3-b9ef-506adb3a0ce2"
         ]
      },
      "message":{
         "type":"activity.unpublish",
         "data":{
            "testUuids":[
               "e97761c5-c441-4ce0-94ea-c7529f2f1196"
            ]
         }
      }
   }
]
```