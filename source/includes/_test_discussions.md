# Test Discussions

<aside class="notice">
Resources related to <code>test discussion management</code>.
</aside>

## Display Answer

> 200

```json
{
    "message": "success",
    "status_code": 200
}
```

<!--
```json--wb
{
	"users":{
		"students": [
			$userUuid
		],
		"teachers":[
			$userUuid
		]
	},
	"message":{
	    "type": "question.update_question_gallery_status",
		"data": {
			"activityQuestion": [
                "uuid": $activityQuestion->uuid,
                "isDisplayed": $activityQuestion->isDisplayed,
                "eGalleryStatus": $activityQuestion->eGalleryStatus,
                "votingMethod": $activityQuestion->votingMethod,
                "rankingValue": $activityQuestion->rankingValue,
                "displayAnswer": $activityQuestion->allowDisplayAnswer,
                "displayAnswerStatistics": $activityQuestion->allowDisplayAnswerStatistics,
                "answers": [
                    {
                        "uuid": $answer->uuid,
                        "dateCompleted": $answer->dateCompleted,
                        "duration": $duration,
                        "answer": $answer->lastAnswerKey,
                        "comments": $answer->comments,
                        "attachments": $answer->attachments,
                        "manualScore": $answer->manualScore,
                        "isGoodAnswer": (boolean) $answer->isGoodAnswer,
                        "isSelected": $answer->isSelected,
                        "applicationGrade": $answer->applicationGrade,
                        "comments": $answer->displayAnswerComments(),
                        "votes": $answer->displayVotes(),
                        "ranks": $answer->displayRanks(),
                        "student": [
                            "userPlacementTestUuid": $answer->userPlacementTest->uuid,
                            "fullname": $answer->userPlacementTest->placement->user->fullname,
                        ]
                    },
                ],
            ],
            "testUuid": $test->uuid,
		}
	}
}
```
-->


> 422

```json
{
    "message": "422 Unprocessable Entity",
    "errors": {
        "activityQuestionUuid": [
            "The selected activity question uuid is invalid."
        ]
    },
    "status_code": 422
}
```

This resource updates answer visibility in team discussion.

### HTTP Request

`POST [BASE_URL]/tests/{test-uuid}/discussions/display-answer`

### HTTP Get Parameters

`No HTTP get parameters required.`

### Request Headers

[Standard Request Headers](#principles)

### HTTP Post Parameters
Parameter | Description
--------- | -----------
activityQuestionUuid <br /> `required`| **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.


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
            "a4f259bd-01e1-4014-b544-82a795708f0f",
         ],
         "teachers":[
            "b5044539-d7a3-4cc5-989b-c81c5224054d"
         ]
      },
      "message":{
         "type":"question.update_question_gallery_status",
         "data":{
            "activityQuestion":{
               "uuid":"e7213b41-f8ae-4f8c-b55e-08d9711df1c6",
               "isDisplayed":0,
               "eGalleryStatus":null,
               "votingMethod":null,
               "rankingValue":null,
               "displayAnswer":0,
               "displayAnswerStatistics":0,
               "answers":[
                  {
                     "uuid":"55121c6b-2a1c-4b09-be8c-50bb143d319a",
                     "dateCompleted":"2019-09-05 04:47:51",
                     "duration":5,
                     "answer":"A",
                     "comments":[

                     ],
                     "attachments":null,
                     "manualScore":"5.00",
                     "isGoodAnswer":false,
                     "isSelected":null,
                     "applicationGrade":null,
                     "votes":[

                     ],
                     "ranks":[

                     ],
                     "student":{
                        "userPlacementTestUuid":"4897c91c-11a7-4806-ab56-0afe29d906c2",
                        "fullname":"C3-1-1-1s1"
                     }
                  }
               ]
            },
            "testUuid":"3a3f8cd0-57db-4f5b-b045-390a37c15c35"
         }
      }
   }
]
```








## Display Answer Statistics

> 200

```json
{
    "message": "success",
    "status_code": 200
}
```

> 422

```json
{
    "message": "422 Unprocessable Entity",
    "errors": {
        "activityQuestionUuid": [
            "The selected activity question uuid is invalid."
        ]
    },
    "status_code": 422
}
```

This resource updates answer statistics visibility in team discussion.

### HTTP Request

`POST [BASE_URL]/tests/{test-uuid}/discussions/display-answer-statistics`

### HTTP Get Parameters

`No HTTP get parameters required.`

### Request Headers

[Standard Request Headers](#principles)


### HTTP Post Parameters
Parameter | Description
--------- | -----------
activityQuestionUuid <br /> `required`| **string** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.


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
         "type":"question.update_question_gallery_status",
         "data":{
            "activityQuestion":{
               "uuid":"e7213b41-f8ae-4f8c-b55e-08d9711df1c6",
               "isDisplayed":0,
               "eGalleryStatus":null,
               "votingMethod":null,
               "rankingValue":null,
               "displayAnswer":0,
               "displayAnswerStatistics":1,
               "answers":[
                  {
                     "uuid":"55121c6b-2a1c-4b09-be8c-50bb143d319a",
                     "dateCompleted":"2019-09-05 04:47:51",
                     "duration":5,
                     "answer":"A",
                     "comments":[

                     ],
                     "attachments":null,
                     "manualScore":"5.00",
                     "isGoodAnswer":false,
                     "isSelected":null,
                     "applicationGrade":null,
                     "votes":[

                     ],
                     "ranks":[

                     ],
                     "student":{
                        "userPlacementTestUuid":"4897c91c-11a7-4806-ab56-0afe29d906c2",
                        "fullname":"C3-1-1-1s1"
                     }
                  }
               ]
            },
            "testUuid":"3a3f8cd0-57db-4f5b-b045-390a37c15c35"
         }
      }
   }
]
```









## Sync Settings

> 200

```json
{
    "message": "success",
    "status_code": 200
}
```

> 422

```json
{
    "message": "422 Unprocessable Entity",
    "errors": {
        "activityQuestionUuid": [
            "The selected activity question uuid is invalid."
        ]
    },
    "status_code": 422
}
```

This resource syncs all the questions' visibility of answer and answer statistics.

### HTTP Request

`POST [BASE_URL]/tests/{test-uuid}/discussions/sync`

### HTTP Get Parameters

`No HTTP get parameters required.`

### Request Headers

[Standard Request Headers](#principles)

### HTTP Post Parameters
Parameter | Description
--------- | -----------
allowDisplayAnswer | **boolean** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
allowDisplayAnswerStatistics | **boolean** <br /> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.



### Winterbreak Setups

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
         "type":"question.sync",
         "data":{
            "testUuid":"3a3f8cd0-57db-4f5b-b045-390a37c15c35",
            "displayAnswer":0,
            "displayAnswerStatistics":1
         }
      }
   }
]
```