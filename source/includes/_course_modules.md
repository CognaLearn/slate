# Course Modules

<aside class="notice">
Resources related to <code>course modules management</code>.
</aside>

## List of Course Modules

> 200

```json
{
    "data": [
        {
            "uuid": "71f2350b-3c99-4f29-bf7c-8650773f8748",
            "name": "Database Management",
            "startDate": "2019-08-26T16:00:00Z",
            "endDate": "2020-02-27T15:59:59Z",
            "isArchived": false,
            "activities": [
                {
                    "uuid": "804d71d3-434b-46d3-99e2-7a3d11435e75",
                    "name": "IRAT Activity",
                    "type": "irat",
                    "isPublished": true,
                    "tests": [
                        {
                            "ownerUuid": "d4f4b6f3-0c2a-4a26-b611-4c2dacc2a841",
                            "name": "IRAT Activity",
                            "activityType": "irat",
                            "uuid": "069a9370-aade-4727-b930-d1e43d413d5f",
                            "section": "1",
                            "type": "irat",
                            "isPublished": true,
                            "status": "ongoing",
                            "students": {
                                "length": 30
                            },
                            "settings": {
                                "type": "asynchronous"
                            }
                        }
                    ],
                    "settings": {
                        "irat": {
                            "type": "asynchronous"
                        }
                    }
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

> 404

```json
{
    "message": "Not Found",
    "status_code": 404
}
```

This resource gets all modules of specific course.

### HTTP Request

`GET [BASE_URL]/courses/{course-uuid}/modules`

### HTTP Get Parameters

[Standard HTTP Get Parameters](#principles)

`i.e. [BASE_URL]/courses/{course-uuid}/modules?page=1&per_page=3`

### Request Headers

[Standard Request Headers](#principles)

### HTTP Post Parameters

`No HTTP post parameters required.`