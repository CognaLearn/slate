# Courses

<aside class="notice">
Resources related to <code>course management</code>.
</aside>

## List of Courses

> 200

```json
{
    "data": [
        {
            "user": {
                "accountType": "Full Access"
            },
            "course": {
                "name": "Bachelor of Science in Computer Science (BSCS)",
                "code": "BSCS",
                "startDate": "2019-08-26T16:00:00Z",
                "endDate": "2020-02-27T15:59:59Z",
                "uuid": "a4ce9d2c-8cb0-4b82-85e2-4f845ab38b36"
            }
        },
    ],
    "meta": {
        "pagination": {
            "total": 1,
            "count": 1,
            "per_page": 10,
            "current_page": 1,
            "total_pages": 1,
            "links": {
                "next": "https://api3-dev.intedashboard.com/api/v1/courses?page=2"
            }
        }
    }
}
```

This resource gets all courses.

### HTTP Request

`GET [BASE_URL]/courses`

### HTTP Get Parameters

[Standard HTTP Get Parameters](#principles)

`i.e. [BASE_URL]/courses?page=1&per_page=3`

### Request Headers

[Standard Request Headers](#principles)

### HTTP Post Parameters

`No HTTP post parameters required.`