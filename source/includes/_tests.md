# Tests

<aside class="notice">
Resources related to <code>tests management</code>.
</aside>





## Visible

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

This resource updates test visibility.

### HTTP Request

`POST [BASE_URL]/tests/{test-uuid}/visible`

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
            "a4f259bd-01e1-4014-b544-82a795708f0f"
         ],
         "teachers":[
            "b5044539-d7a3-4cc5-989b-c81c5224054d"
         ]
      },
      "message":{
         "type":"test.update_visibility",
         "data":{
            "test":{
               "uuid":"3a3f8cd0-57db-4f5b-b045-390a37c15c35",
               "isPublished":false,
               "isVisible":true,
               "allowStudentsToViewAnswer":true,
               "allowStudentsToViewScore":false,
               "allowStudentsToPreviewQuestions":false,
               "status":"ongoing",
               "clarificationStatus":null,
               "timePaused":null,
               "settings":{
                  "type":"asynchronous",
                  "startTime":"2019-09-01T16:00:00Z",
                  "endTime":"2020-03-03T15:00:00Z",
                  "diffInSeconds":null,
                  "durationDays":null,
                  "durationHours":null,
                  "durationMinutes":20
               }
            }
         }
      }
   }
]
```










## Answer Visibility

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

This resource updates answer visibility of specific test.

### HTTP Request

`POST [BASE_URL]/tests/{test-uuid}/answer-visibility`

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
            "a4f259bd-01e1-4014-b544-82a795708f0f"
         ],
         "teachers":[
            "b5044539-d7a3-4cc5-989b-c81c5224054d"
         ]
      },
      "message":{
         "type":"test.update_visibility",
         "data":{
            "test":{
               "uuid":"3a3f8cd0-57db-4f5b-b045-390a37c15c35",
               "isPublished":false,
               "isVisible":true,
               "allowStudentsToViewAnswer":true,
               "allowStudentsToViewScore":false,
               "allowStudentsToPreviewQuestions":false,
               "status":"ongoing",
               "clarificationStatus":null,
               "timePaused":null,
               "settings":{
                  "type":"asynchronous",
                  "startTime":"2019-09-01T16:00:00Z",
                  "endTime":"2020-03-03T15:00:00Z",
                  "diffInSeconds":null,
                  "durationDays":null,
                  "durationHours":null,
                  "durationMinutes":20
               }
            }
         }
      }
   }
]
```










## Score Visibility

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

This resource updates score visibility of specific test.

### HTTP Request

`POST [BASE_URL]/tests/{test-uuid}/score-visibility`

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
            "a4f259bd-01e1-4014-b544-82a795708f0f"
         ],
         "teachers":[
            "b5044539-d7a3-4cc5-989b-c81c5224054d"
         ]
      },
      "message":{
         "type":"test.update_visibility",
         "data":{
            "test":{
               "uuid":"3a3f8cd0-57db-4f5b-b045-390a37c15c35",
               "isPublished":false,
               "isVisible":true,
               "allowStudentsToViewAnswer":true,
               "allowStudentsToViewScore":false,
               "allowStudentsToPreviewQuestions":false,
               "status":"ongoing",
               "clarificationStatus":null,
               "timePaused":null,
               "settings":{
                  "type":"asynchronous",
                  "startTime":"2019-09-01T16:00:00Z",
                  "endTime":"2020-03-03T15:00:00Z",
                  "diffInSeconds":null,
                  "durationDays":null,
                  "durationHours":null,
                  "durationMinutes":20
               }
            }
         }
      }
   }
]
```







## Question Preview

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

This resource updates question preview of specific test.

### HTTP Request

`POST [BASE_URL]/tests/{test-uuid}/question-preview`

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
            "a4f259bd-01e1-4014-b544-82a795708f0f"
         ],
         "teachers":[
            "b5044539-d7a3-4cc5-989b-c81c5224054d"
         ]
      },
      "message":{
         "type":"test.update_visibility",
         "data":{
            "test":{
               "uuid":"3a3f8cd0-57db-4f5b-b045-390a37c15c35",
               "isPublished":false,
               "isVisible":true,
               "allowStudentsToViewAnswer":true,
               "allowStudentsToViewScore":false,
               "allowStudentsToPreviewQuestions":false,
               "status":"ongoing",
               "clarificationStatus":null,
               "timePaused":null,
               "settings":{
                  "type":"asynchronous",
                  "startTime":"2019-09-01T16:00:00Z",
                  "endTime":"2020-03-03T15:00:00Z",
                  "diffInSeconds":null,
                  "durationDays":null,
                  "durationHours":null,
                  "durationMinutes":20
               }
            }
         }
      }
   }
]
```





## Question Preview

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

This resource updates question preview of specific test.

### HTTP Request

`POST [BASE_URL]/tests/{test-uuid}/question-preview`

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
            "a4f259bd-01e1-4014-b544-82a795708f0f"
         ],
         "teachers":[
            "b5044539-d7a3-4cc5-989b-c81c5224054d"
         ]
      },
      "message":{
         "type":"test.update_visibility",
         "data":{
            "test":{
               "uuid":"3a3f8cd0-57db-4f5b-b045-390a37c15c35",
               "isPublished":false,
               "isVisible":true,
               "allowStudentsToViewAnswer":true,
               "allowStudentsToViewScore":false,
               "allowStudentsToPreviewQuestions":false,
               "status":"ongoing",
               "clarificationStatus":null,
               "timePaused":null,
               "settings":{
                  "type":"asynchronous",
                  "startTime":"2019-09-01T16:00:00Z",
                  "endTime":"2020-03-03T15:00:00Z",
                  "diffInSeconds":null,
                  "durationDays":null,
                  "durationHours":null,
                  "durationMinutes":20
               }
            }
         }
      }
   }
]
```






## Publish

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

This resource publishes specific test.

### HTTP Request

`POST [BASE_URL]/tests/{test-uuid}/publish`

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
            "a4f259bd-01e1-4014-b544-82a795708f0f"
         ],
         "teachers":[
            "b5044539-d7a3-4cc5-989b-c81c5224054d"
         ]
      },
      "message":{
         "type":"test.update_visibility",
         "data":{
            "test":{
               "uuid":"3a3f8cd0-57db-4f5b-b045-390a37c15c35",
               "isPublished":false,
               "isVisible":true,
               "allowStudentsToViewAnswer":true,
               "allowStudentsToViewScore":false,
               "allowStudentsToPreviewQuestions":false,
               "status":"ongoing",
               "clarificationStatus":null,
               "timePaused":null,
               "settings":{
                  "type":"asynchronous",
                  "startTime":"2019-09-01T16:00:00Z",
                  "endTime":"2020-03-03T15:00:00Z",
                  "diffInSeconds":null,
                  "durationDays":null,
                  "durationHours":null,
                  "durationMinutes":20
               }
            }
         }
      }
   }
]
```







## Start

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

This resource starts specific test.

### HTTP Request

`POST [BASE_URL]/tests/{test-uuid}/start`

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
            "a4f259bd-01e1-4014-b544-82a795708f0f"
         ],
         "teachers":[
            "b5044539-d7a3-4cc5-989b-c81c5224054d"
         ]
      },
      "message":{
         "type":"test.update_status",
         "data":{
            "test":{
               "uuid":"3a3f8cd0-57db-4f5b-b045-390a37c15c35",
               "isPublished":false,
               "isVisible":true,
               "allowStudentsToViewAnswer":true,
               "allowStudentsToViewScore":false,
               "allowStudentsToPreviewQuestions":false,
               "status":"ongoing",
               "clarificationStatus":null,
               "timePaused":null,
               "settings":{
                  "type":"asynchronous",
                  "startTime":"2019-09-01T16:00:00Z",
                  "endTime":"2020-03-03T15:00:00Z",
                  "diffInSeconds":null,
                  "durationDays":null,
                  "durationHours":null,
                  "durationMinutes":20
               }
            }
         }
      }
   }
]
```




## End

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

This resource ends specific test.

### HTTP Request

`POST [BASE_URL]/tests/{test-uuid}/end`

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
            "a4f259bd-01e1-4014-b544-82a795708f0f"
         ],
         "teachers":[
            "b5044539-d7a3-4cc5-989b-c81c5224054d"
         ]
      },
      "message":{
         "type":"test.update_status",
         "data":{
            "test":{
               "uuid":"3a3f8cd0-57db-4f5b-b045-390a37c15c35",
               "isPublished":false,
               "isVisible":true,
               "allowStudentsToViewAnswer":true,
               "allowStudentsToViewScore":false,
               "allowStudentsToPreviewQuestions":false,
               "status":"ongoing",
               "clarificationStatus":null,
               "timePaused":null,
               "settings":{
                  "type":"asynchronous",
                  "startTime":"2019-09-01T16:00:00Z",
                  "endTime":"2020-03-03T15:00:00Z",
                  "diffInSeconds":null,
                  "durationDays":null,
                  "durationHours":null,
                  "durationMinutes":20
               }
            }
         }
      }
   }
]
```







## Extend

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

This resource extends specific test.

### HTTP Request

`POST [BASE_URL]/tests/{test-uuid}/extend`

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
            "a4f259bd-01e1-4014-b544-82a795708f0f"
         ],
         "teachers":[
            "b5044539-d7a3-4cc5-989b-c81c5224054d"
         ]
      },
      "message":{
         "type":"test.update_status",
         "data":{
            "test":{
               "uuid":"3a3f8cd0-57db-4f5b-b045-390a37c15c35",
               "isPublished":false,
               "isVisible":true,
               "allowStudentsToViewAnswer":true,
               "allowStudentsToViewScore":false,
               "allowStudentsToPreviewQuestions":false,
               "status":"ongoing",
               "clarificationStatus":null,
               "timePaused":null,
               "settings":{
                  "type":"asynchronous",
                  "startTime":"2019-09-01T16:00:00Z",
                  "endTime":"2020-03-03T15:00:00Z",
                  "diffInSeconds":null,
                  "durationDays":null,
                  "durationHours":null,
                  "durationMinutes":20
               }
            }
         }
      }
   }
]
```







## Pause

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

This resource pauses specific test.

### HTTP Request

`POST [BASE_URL]/tests/{test-uuid}/pause`

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
            "a4f259bd-01e1-4014-b544-82a795708f0f"
         ],
         "teachers":[
            "b5044539-d7a3-4cc5-989b-c81c5224054d"
         ]
      },
      "message":{
         "type":"test.update_status",
         "data":{
            "test":{
               "uuid":"3a3f8cd0-57db-4f5b-b045-390a37c15c35",
               "isPublished":false,
               "isVisible":true,
               "allowStudentsToViewAnswer":true,
               "allowStudentsToViewScore":false,
               "allowStudentsToPreviewQuestions":false,
               "status":"ongoing",
               "clarificationStatus":null,
               "timePaused":null,
               "settings":{
                  "type":"asynchronous",
                  "startTime":"2019-09-01T16:00:00Z",
                  "endTime":"2020-03-03T15:00:00Z",
                  "diffInSeconds":null,
                  "durationDays":null,
                  "durationHours":null,
                  "durationMinutes":20
               }
            }
         }
      }
   }
]
```






## Resume

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

This resource resumes specific test.

### HTTP Request

`POST [BASE_URL]/tests/{test-uuid}/resume`

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
            "a4f259bd-01e1-4014-b544-82a795708f0f"
         ],
         "teachers":[
            "b5044539-d7a3-4cc5-989b-c81c5224054d"
         ]
      },
      "message":{
         "type":"test.update_status",
         "data":{
            "test":{
               "uuid":"3a3f8cd0-57db-4f5b-b045-390a37c15c35",
               "isPublished":false,
               "isVisible":true,
               "allowStudentsToViewAnswer":true,
               "allowStudentsToViewScore":false,
               "allowStudentsToPreviewQuestions":false,
               "status":"ongoing",
               "clarificationStatus":null,
               "timePaused":null,
               "settings":{
                  "type":"asynchronous",
                  "startTime":"2019-09-01T16:00:00Z",
                  "endTime":"2020-03-03T15:00:00Z",
                  "diffInSeconds":null,
                  "durationDays":null,
                  "durationHours":null,
                  "durationMinutes":20
               }
            }
         }
      }
   }
]
```







## Update Period

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

This resource updates period of specific test.

### HTTP Request

`POST [BASE_URL]/tests/{test-uuid}/update-period`

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
            "a4f259bd-01e1-4014-b544-82a795708f0f"
         ],
         "teachers":[
            "b5044539-d7a3-4cc5-989b-c81c5224054d"
         ]
      },
      "message":{
         "type":"test.update_period",
         "data":{
            "test":{
               "uuid":"3a3f8cd0-57db-4f5b-b045-390a37c15c35",
               "isPublished":false,
               "isVisible":true,
               "allowStudentsToViewAnswer":true,
               "allowStudentsToViewScore":false,
               "allowStudentsToPreviewQuestions":false,
               "status":"ongoing",
               "clarificationStatus":null,
               "timePaused":null,
               "settings":{
                  "type":"asynchronous",
                  "startTime":"2019-09-01T16:00:00Z",
                  "endTime":"2020-03-03T15:00:00Z",
                  "diffInSeconds":null,
                  "durationDays":null,
                  "durationHours":null,
                  "durationMinutes":20
               }
            }
         }
      }
   }
]
```







## Grade

> 200

```

File will be downloaded

```

> 404

```json
{
    "message": "Not Found",
    "status_code": 404
}
```

This resource exports grades of specific test.

### HTTP Request

`GET [BASE_URL]/tests/{test-uuid}/grades`

### HTTP Get Parameters

`No HTTP get parameters required.`

### Request Headers

[Standard Request Headers](#principles)

### HTTP Post Parameters

`No HTTP post parameters required.`