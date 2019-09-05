# Dashboard

<aside class="notice">
Resources related to <code>dashboard</code>.
</aside>


## Overview

> 200 (Prework)

```json
{
    "data": {
        "activityUuid": "891f0207-cd14-4e39-bf8d-10bccfbef34e",
        "name": "Prework",
        "description": null,
        "descriptionIsHTML": null,
        "others": {
            "preworkType": "simple"
        },
        "hasStartedBefore": true,
        "isActivitySettingsCompleted": true,
        "pointSettingsVersion": null,
        "uuid": "31da0f8b-c258-4b27-8fed-c37d7cbad32e",
        "type": "prework",
        "totalMarks": 0,
        "status": "ongoing",
        "timeStarted": "2019-09-02T03:00:40Z",
        "timeEnded": null,
        "timePaused": null,
        "isVisible": true,
        "isPublished": true,
        "allowStudentsToViewAnswer": false,
        "allowStudentsToViewScore": false,
        "allowStudentsToPreviewQuestions": false,
        "settings": {
            "type": "asynchronous",
            "startDate": "2019-08-14T16:00:00Z",
            "endDate": "2020-02-15T15:59:59Z",
            "durationDays": null,
            "durationHours": null,
            "durationMinutes": null,
            "confidenceBasedTesting": null,
            "allowTeamClarifications": null,
            "password": null
        },
        "course": {
            "uuid": "9499c8e4-91dc-479a-885d-dc631f8f92e7",
            "name": "C2",
            "code": null
        },
        "plannedDuration": "0 Sec",
        "actualDuration": "0 Sec",
        "eGalleryProgression": {
            "currentQuestionUuid": null
        },
        "startTime": "2019-08-14T16:00:00Z",
        "endTime": "2020-02-15T15:59:59Z",
        "materials": [
            {
                "material": {
                    "filename": "(evaluation)View my Scores_2019_08_31.xlsx",
                    "handle": "AGPrvL8TRKuGE8SUWFf2",
                    "mimetype": "application/vnd.openxmlformats-officedocument.spreadsheetml.sheet",
                    "originalPath": "(evaluation)View my Scores_2019_08_31.xlsx",
                    "size": 13122,
                    "source": "local_file_system",
                    "url": "https://cdn.filestackcontent.com/AGPrvL8TRKuGE8SUWFf2",
                    "uploadId": "0c7d9e1e1e72957c2c9c169073facdf2",
                    "originalFile": {
                        "name": "(evaluation)View my Scores_2019_08_31.xlsx",
                        "type": "application/vnd.openxmlformats-officedocument.spreadsheetml.sheet",
                        "size": 13122
                    },
                    "status": "Stored"
                },
                "opened": [
                    "C2P1-1-1s1"
                ],
                "downloaded": [
                    "C2P1-1-1s1"
                ]
            }
        ],
        "students": [
            {
                "displayName": "C2P1-1-1s1"
            }
        ]
    }
}
```

> 200 (IRAT)

```json
{
    "data": {
        "activityUuid": "11b2eeb1-75dc-4746-a332-5f09f3d44ca8",
        "name": "IRAT",
        "description": null,
        "descriptionIsHTML": null,
        "others": [],
        "hasStartedBefore": true,
        "isActivitySettingsCompleted": true,
        "pointSettingsVersion": "JSe1y",
        "uuid": "00ead9a8-8b51-4382-9b96-891a0d1de85c",
        "type": "irat",
        "totalMarks": 9,
        "status": "ongoing",
        "timeStarted": "2019-08-16T08:43:00Z",
        "timeEnded": null,
        "timePaused": null,
        "isVisible": true,
        "isPublished": true,
        "allowStudentsToViewAnswer": false,
        "allowStudentsToViewScore": false,
        "allowStudentsToPreviewQuestions": false,
        "settings": {
            "type": "asynchronous",
            "startDate": "2019-08-14T16:00:00Z",
            "endDate": "2020-02-16T15:00:00Z",
            "durationDays": null,
            "durationHours": null,
            "durationMinutes": 20,
            "confidenceBasedTesting": false,
            "allowTeamClarifications": null,
            "password": ""
        },
        "course": {
            "uuid": "9499c8e4-91dc-479a-885d-dc631f8f92e7",
            "name": "C2",
            "code": null
        },
        "plannedDuration": "20 Min, 0 Sec",
        "actualDuration": "0 Sec",
        "eGalleryProgression": {
            "currentQuestionUuid": null
        },
        "startTime": "2019-08-14T16:00:00Z",
        "endTime": "2020-02-16T15:00:00Z",
        "otherTestUuids": [
            {
                "type": "irat",
                "section": "2",
                "uuid": "84383c05-a3a4-49c7-a956-174d3e8bdf87"
            }
        ],
        "attendance": {
            "present": 1,
            "students": [
                {
                    "uuid": "79a8cab0-fee0-425c-bf5d-d172b58dbcca",
                    "displayName": "C2P1-1-1s1",
                    "isPresent": true
                }
            ]
        },
        "activityStatus": {
            "present": 1,
            "started": 1,
            "entered": 1,
            "ongoing": 0,
            "finished": 1,
            "submitted": 1,
            "questionsAnswered": 1
        },
        "questions": [
            [
                {
                    "uuid": "2928cbb7-e17d-42dd-abbf-99c34a61d362",
                    "group": 1,
                    "order": 1,
                    "question": "Who is the President of the Philippines?",
                    "questionIsHTML": true,
                    "type": "mcqs",
                    "settings": {
                        "irat": {
                            "point": 1
                        }
                    },
                    "tags": [],
                    "attachments": [],
                    "options": [
                        {
                            "key": "A",
                            "tags": [],
                            "content": "Rodrigo Duterte",
                            "remarks": "",
                            "isCorrect": true,
                            "contentIsHTML": true
                        },
                        {
                            "key": "B",
                            "tags": [],
                            "content": "Bong Go",
                            "remarks": "",
                            "isCorrect": false,
                            "contentIsHTML": true
                        },
                        {
                            "key": "C",
                            "tags": [],
                            "content": "Gloria Arroyo",
                            "remarks": "",
                            "isCorrect": false,
                            "contentIsHTML": true
                        }
                    ],
                    "minimum": 1,
                    "maximum": null,
                    "difficultyLevel": 1,
                    "topics": [],
                    "displayAnswer": false,
                    "displayAnswerStatistics": false,
                    "optionKeys": [
                        {
                            "key": "A",
                            "isCorrect": true,
                            "countAnswersPerOptionData": 4,
                            "countPresentStudents": 4,
                            "percent": 100,
                            "answersPerOption": [
                                {
                                    "student": {
                                        "userPlacementTestUuid": "892cd54c-9dd4-4002-a572-95dc5dec5533",
                                        "fullname": "C2P1-1-1s1"
                                    },
                                    "dateCompleted": {
                                        "date": "2019-08-16 08:44:44.000000",
                                        "timezone_type": 3,
                                        "timezone": "UTC"
                                    },
                                    "duration": 7
                                }
                            ]
                        },
                        {
                            "key": "B",
                            "isCorrect": false,
                            "countAnswersPerOptionData": 0,
                            "countPresentStudents": 4,
                            "percent": 0,
                            "answersPerOption": []
                        },
                        {
                            "key": "C",
                            "isCorrect": false,
                            "countAnswersPerOptionData": 0,
                            "countPresentStudents": 4,
                            "percent": 0,
                            "answersPerOption": []
                        },
                    ],
                    "answers": [],
                    "statistics": {
                        "averageTime": "0 Sec"
                    },
                    "presentStudentsWithNoAnswer": [],
                    "score": 1,
                    "eGallery": null
                }
            ],
        ],
        "totalAverageCompletion": "0 Sec",
        "totalAverageCompletionPerQuestion": 0
    }
}
```

> 200 (TRAT)

```json
{
    "data": {
        "activityUuid": "19b057bf-e6f3-4dc9-890d-f9331900131b",
        "name": "TRAT",
        "description": null,
        "descriptionIsHTML": null,
        "others": [],
        "hasStartedBefore": true,
        "isActivitySettingsCompleted": true,
        "pointSettingsVersion": "2c6Tm",
        "uuid": "9665e76f-5cb6-4eb8-bf4f-9118f2d7fc10",
        "type": "trat",
        "totalMarks": 46,
        "status": "ongoing",
        "timeStarted": "2019-08-17T00:46:47Z",
        "timeEnded": null,
        "timePaused": null,
        "isVisible": true,
        "isPublished": true,
        "allowStudentsToViewAnswer": true,
        "allowStudentsToViewScore": false,
        "allowStudentsToPreviewQuestions": false,
        "settings": {
            "type": "asynchronous",
            "startDate": "2019-08-14T16:00:00Z",
            "endDate": "2020-02-17T15:00:00Z",
            "durationDays": null,
            "durationHours": null,
            "durationMinutes": 20,
            "confidenceBasedTesting": null,
            "allowTeamClarifications": true,
            "password": ""
        },
        "course": {
            "uuid": "9499c8e4-91dc-479a-885d-dc631f8f92e7",
            "name": "C2",
            "code": null
        },
        "plannedDuration": "20 Min, 0 Sec",
        "actualDuration": "0 Sec",
        "eGalleryProgression": {
            "currentQuestionUuid": null
        },
        "startTime": "2019-08-14T16:00:00Z",
        "endTime": "2020-02-17T15:00:00Z",
        "otherTestUuids": [
            {
                "type": "trat",
                "section": "2",
                "uuid": "387b7c45-a23a-4a6c-8939-544360b921f6"
            }
        ],
        "attendance": {
            "present": 1,
            "teams": [
                {
                    "uuid": "84538319-1e46-4034-97ce-68447ea1fedc",
                    "name": "Team 1",
                    "isPresent": true
                }
            ]
        },
        "activityStatus": {
            "present": 1,
            "started": 1,
            "entered": 1,
            "ongoing": 0,
            "finished": 1,
            "submitted": 1,
            "questionsAnswered": 1
        },
        "questions": [
            [
                {
                    "uuid": "7dd2e708-c4f3-4a5b-9a49-8a39c6f242b8",
                    "group": 1,
                    "order": 1,
                    "question": "Who is the President of the Philippines?",
                    "questionIsHTML": true,
                    "type": "mcqs",
                    "settings": {
                        "trat": {
                            "points": [
                                5,
                                3,
                                1,
                                0
                            ]
                        }
                    },
                    "tags": [],
                    "attachments": [],
                    "options": [
                        {
                            "key": "A",
                            "tags": [],
                            "content": "Rodrigo Duterte",
                            "remarks": "",
                            "isCorrect": true,
                            "contentIsHTML": true
                        },
                        {
                            "key": "B",
                            "tags": [],
                            "content": "Bong Go",
                            "remarks": "",
                            "isCorrect": false,
                            "contentIsHTML": true
                        },
                        {
                            "key": "C",
                            "tags": [],
                            "content": "Gloria Arroyo",
                            "remarks": "",
                            "isCorrect": false,
                            "contentIsHTML": true
                        }
                    ],
                    "minimum": 1,
                    "maximum": null,
                    "difficultyLevel": 1,
                    "topics": [],
                    "displayAnswer": true,
                    "displayAnswerStatistics": true,
                    "optionKeys": [
                        {
                            "key": "A",
                            "isCorrect": true,
                            "countAnswersPerOptionData": 1,
                            "countPresentTeams": 1,
                            "percent": 100,
                            "answersPerOption": [
                                {
                                    "team": {
                                        "uuid": "84538319-1e46-4034-97ce-68447ea1fedc",
                                        "name": "Team 1",
                                        "members": [
                                            {
                                                "studentUuid": "79a8cab0-fee0-425c-bf5d-d172b58dbcca",
                                                "team": "Team 1",
                                                "identity": "C2P1-1-1s1",
                                                "email": null,
                                                "firstname": "C2P1-1-1s1",
                                                "lastname": null,
                                                "displayName": "C2P1-1-1s1",
                                                "avatar": null
                                            }
                                        ]
                                    },
                                    "reporter": "C2P1-1-1s1",
                                    "dateCompleted": {
                                        "date": "2019-08-17 00:48:30.000000",
                                        "timezone_type": 3,
                                        "timezone": "UTC"
                                    },
                                    "duration": 11
                                }
                            ]
                        },
                        {
                            "key": "B",
                            "isCorrect": false,
                            "countAnswersPerOptionData": 0,
                            "countPresentTeams": 1,
                            "percent": 0,
                            "answersPerOption": []
                        },
                        {
                            "key": "C",
                            "isCorrect": false,
                            "countAnswersPerOptionData": 0,
                            "countPresentTeams": 1,
                            "percent": 0,
                            "answersPerOption": []
                        }
                    ],
                    "answers": [],
                    "statistics": {
                        "averageTime": "11 Sec",
                        "percentCorrect": 100
                    },
                    "presentTeamsWithNoAnswer": [],
                    "score": 5,
                    "eGallery": null
                }
            ]
        ],
        "totalAverageCompletionPerQuestion": "0 Sec",
        "totalAverageCompletion": "9 Sec"
    }
}
```

> 200 (Application - Individual)

```json
{
    "data": {
        "activityUuid": "4357906f-8dbe-43bc-8aff-cc0b12d70bdf",
        "name": "Application Individual - Graded",
        "description": null,
        "descriptionIsHTML": null,
        "others": {
            "applicationType": "individual",
            "isApplicationGraded": true
        },
        "hasStartedBefore": true,
        "isActivitySettingsCompleted": true,
        "pointSettingsVersion": "U4TRV",
        "uuid": "fbc66981-d432-4321-8aa3-9b82707adf1b",
        "type": "application",
        "totalMarks": 1,
        "status": "ended",
        "timeStarted": "2019-09-02T04:28:28Z",
        "timeEnded": "2019-09-02T04:29:15Z",
        "timePaused": null,
        "isVisible": true,
        "isPublished": true,
        "allowStudentsToViewAnswer": true,
        "allowStudentsToViewScore": true,
        "allowStudentsToPreviewQuestions": false,
        "settings": {
            "type": "synchronous",
            "startDate": "2019-08-14T16:00:00Z",
            "endDate": "2020-02-15T15:59:59Z",
            "durationDays": null,
            "durationHours": null,
            "durationMinutes": 20,
            "confidenceBasedTesting": null,
            "allowTeamClarifications": null,
            "password": null
        },
        "course": {
            "uuid": "9499c8e4-91dc-479a-885d-dc631f8f92e7",
            "name": "C2",
            "code": null
        },
        "plannedDuration": "20 Min, 0 Sec",
        "actualDuration": "47 Sec",
        "eGalleryProgression": {
            "currentQuestionUuid": "f9cd7204-b8da-4091-9cd9-38fcdb30fb4e"
        },
        "startTime": "2019-09-02T04:28:28Z",
        "endTime": "2019-09-02T04:48:28Z",
        "attendance": {
            "present": 1,
            "students": [
                {
                    "uuid": "79a8cab0-fee0-425c-bf5d-d172b58dbcca",
                    "displayName": "C2P1-1-1s1",
                    "isPresent": true
                }
            ]
        },
        "activityStatus": {
            "present": 1,
            "started": 1,
            "entered": 1,
            "ongoing": 0,
            "finished": 1,
            "submitted": 1,
            "questionsAnswered": 3
        },
        "questions": [
            [
                {
                    "uuid": "2928cbb7-e17d-42dd-abbf-99c34a61d362",
                    "group": 1,
                    "order": 1,
                    "question": "Who is the President of the Philippines?",
                    "questionIsHTML": true,
                    "type": "mcqs",
                    "settings": {
                        "irat": {
                            "point": 1
                        }
                    },
                    "tags": [],
                    "attachments": [],
                    "options": [
                        {
                            "key": "A",
                            "tags": [],
                            "content": "Rodrigo Duterte",
                            "remarks": "",
                            "isCorrect": true,
                            "contentIsHTML": true
                        },
                        {
                            "key": "B",
                            "tags": [],
                            "content": "Bong Go",
                            "remarks": "",
                            "isCorrect": false,
                            "contentIsHTML": true
                        },
                        {
                            "key": "C",
                            "tags": [],
                            "content": "Gloria Arroyo",
                            "remarks": "",
                            "isCorrect": false,
                            "contentIsHTML": true
                        },
                    ],
                    "minimum": 1,
                    "maximum": null,
                    "difficultyLevel": 1,
                    "topics": [],
                    "displayAnswer": false,
                    "displayAnswerStatistics": false,
                    "optionKeys": [
                        {
                            "key": "A",
                            "isCorrect": true,
                            "countAnswersPerOptionData": 4,
                            "countPresentStudents": 4,
                            "percent": 100,
                            "answersPerOption": [
                                {
                                    "student": {
                                        "userPlacementTestUuid": "892cd54c-9dd4-4002-a572-95dc5dec5533",
                                        "fullname": "C2P1-1-1s1"
                                    },
                                    "dateCompleted": {
                                        "date": "2019-08-16 08:44:44.000000",
                                        "timezone_type": 3,
                                        "timezone": "UTC"
                                    },
                                    "duration": 7
                                }
                            ]
                        },
                        {
                            "key": "B",
                            "isCorrect": false,
                            "countAnswersPerOptionData": 0,
                            "countPresentStudents": 4,
                            "percent": 0,
                            "answersPerOption": []
                        },
                        {
                            "key": "C",
                            "isCorrect": false,
                            "countAnswersPerOptionData": 0,
                            "countPresentStudents": 4,
                            "percent": 0,
                            "answersPerOption": []
                        },
                    ],
                    "answers": [],
                    "statistics": {
                        "averageTime": "0 Sec"
                    },
                    "presentStudentsWithNoAnswer": [],
                    "score": 1,
                    "eGallery": null
                }
            ],
        ],
        "totalAverageCompletion": "0 Sec",
        "totalAverageCompletionPerQuestion": 0,
        "leaderboard": [
            {
                "item": {
                    "uuid": "98652b0f-f46a-46b9-bd99-eecf7b053149",
                    "name": "C2P1-1-1s1",
                    "status": "Submitted"
                },
                "progress": {
                    "countAnsweredQuestions": 1,
                    "countActivityQuestions": 1,
                    "status": "Submitted",
                    "percent": 100
                }
            }
        ],
        "totalQuestionsScore": 1
    }
}
```

> 200 (Application - Team)

```json
{
    "data": {
        "activityUuid": "6502d7ab-5310-4cbd-ba09-fac8e3b7144f",
        "name": "Application - Team",
        "description": null,
        "descriptionIsHTML": null,
        "others": {
            "applicationType": "team",
            "isApplicationGraded": true
        },
        "hasStartedBefore": true,
        "isActivitySettingsCompleted": true,
        "pointSettingsVersion": "QajFL",
        "uuid": "9d1e9b70-491a-4f94-9919-c3f91712a0af",
        "type": "application",
        "totalMarks": 1,
        "status": "ongoing",
        "timeStarted": "2019-09-02T07:35:17Z",
        "timeEnded": null,
        "timePaused": null,
        "isVisible": true,
        "isPublished": true,
        "allowStudentsToViewAnswer": false,
        "allowStudentsToViewScore": false,
        "allowStudentsToPreviewQuestions": false,
        "settings": {
            "type": "asynchronous",
            "startDate": "2019-08-14T16:00:00Z",
            "endDate": "2020-02-15T15:59:59Z",
            "durationDays": null,
            "durationHours": null,
            "durationMinutes": 20,
            "confidenceBasedTesting": null,
            "allowTeamClarifications": null,
            "password": null
        },
        "course": {
            "uuid": "9499c8e4-91dc-479a-885d-dc631f8f92e7",
            "name": "C2",
            "code": null
        },
        "plannedDuration": "20 Min, 0 Sec",
        "actualDuration": "0 Sec",
        "eGalleryProgression": {
            "currentQuestionUuid": "bdfa3a32-bac2-47f9-ad1f-a57529cf5ee8"
        },
        "startTime": "2019-08-14T16:00:00Z",
        "endTime": "2020-02-15T15:59:59Z",
        "attendance": {
            "present": 0,
            "teams": [
                {
                    "uuid": "84538319-1e46-4034-97ce-68447ea1fedc",
                    "name": "Team 1",
                    "isPresent": false
                }
            ]
        },
        "activityStatus": {
            "present": 0,
            "started": 0,
            "entered": 0,
            "ongoing": 0,
            "finished": 0,
            "submitted": 0,
            "questionsAnswered": 3
        },
        "questions": [
            [
                {
                    "uuid": "2928cbb7-e17d-42dd-abbf-99c34a61d362",
                    "group": 1,
                    "order": 1,
                    "question": "Who is the President of the Philippines?",
                    "questionIsHTML": true,
                    "type": "mcqs",
                    "settings": {
                        "irat": {
                            "point": 1
                        }
                    },
                    "tags": [],
                    "attachments": [],
                    "options": [
                        {
                            "key": "A",
                            "tags": [],
                            "content": "Rodrigo Duterte",
                            "remarks": "",
                            "isCorrect": true,
                            "contentIsHTML": true
                        },
                        {
                            "key": "B",
                            "tags": [],
                            "content": "Bong Go",
                            "remarks": "",
                            "isCorrect": false,
                            "contentIsHTML": true
                        },
                        {
                            "key": "C",
                            "tags": [],
                            "content": "Gloria Arroyo",
                            "remarks": "",
                            "isCorrect": false,
                            "contentIsHTML": true
                        }
                    ],
                    "minimum": 1,
                    "maximum": null,
                    "difficultyLevel": 1,
                    "topics": [],
                    "displayAnswer": false,
                    "displayAnswerStatistics": false,
                    "optionKeys": [
                        {
                            "key": "A",
                            "isCorrect": true,
                            "countAnswersPerOptionData": 4,
                            "countPresentStudents": 4,
                            "percent": 100,
                            "answersPerOption": [
                                {
                                    "student": {
                                        "userPlacementTestUuid": "892cd54c-9dd4-4002-a572-95dc5dec5533",
                                        "fullname": "C2P1-1-1s1"
                                    },
                                    "dateCompleted": {
                                        "date": "2019-08-16 08:44:44.000000",
                                        "timezone_type": 3,
                                        "timezone": "UTC"
                                    },
                                    "duration": 7
                                }
                            ]
                        },
                        {
                            "key": "B",
                            "isCorrect": false,
                            "countAnswersPerOptionData": 0,
                            "countPresentStudents": 4,
                            "percent": 0,
                            "answersPerOption": []
                        },
                        {
                            "key": "C",
                            "isCorrect": false,
                            "countAnswersPerOptionData": 0,
                            "countPresentStudents": 4,
                            "percent": 0,
                            "answersPerOption": []
                        },
                    ],
                    "answers": [],
                    "statistics": {
                        "averageTime": "0 Sec"
                    },
                    "presentStudentsWithNoAnswer": [],
                    "score": 1,
                    "eGallery": null
                }
            ]
        ],
        "totalAverageCompletion": "0 Sec",
        "leaderboard": [
            {
                "item": {
                    "uuid": "84538319-1e46-4034-97ce-68447ea1fedc",
                    "name": "Team 1",
                    "members": [
                        {
                            "studentUuid": "79a8cab0-fee0-425c-bf5d-d172b58dbcca",
                            "team": "Team 1",
                            "identity": "C2P1-1-1s1",
                            "email": null,
                            "firstname": "C2P1-1-1s1",
                            "lastname": null,
                            "displayName": "C2P1-1-1s1",
                            "avatar": null
                        }
                    ],
                    "status": "Not Started"
                },
                "progress": {
                    "countAnsweredQuestions": 0,
                    "countActivityQuestions": 1,
                    "status": "Not Started",
                    "percent": 0
                }
            }
        ],
        "totalQuestionsScore": 1
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

This resource allows to list the activity overview, student and team attendance, and statistics.

### HTTP Request

`GET [BASE_URL]/tests/{test-uuid}/dashboard/overview`

### HTTP Get Parameters

`No HTTP get parameters required.`

### Request Headers
Key | Value | Description
--------- | ------- | -----------
`Content-Type` | **application/json** | Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
`Authorization` | **Bearer $token** | Lorem ipsum dolor sit amet, consectetur adipiscing elit.


### HTTP Post Parameters

`No HTTP post parameters required.`




## Item Analysis

> 200 (Individual)

```json
{
    "data": {
        "uuid": "00ead9a8-8b51-4382-9b96-891a0d1de85c",
        "itemAnalysis": {
            "item": [
                {
                    "question": {
                        "id": 1538,
                        "group": 1,
                        "order": 1,
                        "question": "Who is the President of the Philippines?",
                        "difficultyLevel": 1,
                        "type": "mcqs",
                        "options": [
                            {
                                "key": "A",
                                "tags": [],
                                "content": "Rodrigo Duterte",
                                "remarks": "",
                                "isCorrect": true,
                                "contentIsHTML": true
                            },
                            {
                                "key": "B",
                                "tags": [],
                                "content": "Bong Go",
                                "remarks": "",
                                "isCorrect": false,
                                "contentIsHTML": true
                            },
                            {
                                "key": "C",
                                "tags": [],
                                "content": "Gloria Arroyo",
                                "remarks": "",
                                "isCorrect": false,
                                "contentIsHTML": true
                            }
                        ],
                        "score": 1
                    },
                    "options": [
                        {
                            "key": "A",
                            "isCorrect": true,
                            "countAnswersPerOptionData": 4,
                            "countPresentStudents": 4,
                            "percent": 100,
                            "answersPerOption": [
                                {
                                    "userPlacementTestID": 15995,
                                    "dateCompleted": {
                                        "date": "2019-08-16 08:44:44.000000",
                                        "timezone_type": 3,
                                        "timezone": "UTC"
                                    },
                                    "duration": 7,
                                    "attempts": [
                                        "A"
                                    ],
                                    "finalPoint": "1.00"
                                }
                            ]
                        },
                        {
                            "key": "B",
                            "isCorrect": false,
                            "countAnswersPerOptionData": 0,
                            "countPresentStudents": 4,
                            "percent": 0,
                            "answersPerOption": []
                        },
                        {
                            "key": "C",
                            "isCorrect": false,
                            "countAnswersPerOptionData": 0,
                            "countPresentStudents": 4,
                            "percent": 0,
                            "answersPerOption": []
                        }
                    ],
                    "pointsOfAllStudents": [
                        "1.00",
                        "1.00",
                        "1.00",
                        "1.00"
                    ],
                    "countOfStudentsWithAnswer": 4,
                    "countOfStudentsWithNoAnswer": 0,
                    "presentStudents": 4,
                    "emptyAnswers": -0.5,
                    "averageCompletionTimePerQuestion": "7 Sec",
                    "percentFinishedLearners": 100,
                    "percentCorrect": 100,
                    "failRate": 0,
                    "pbcc": 0
                }
            ],
            "mean": {
                "failRate": 55.555555555556,
                "totalTime": "7 Min, 37 Sec",
                "noOfLearnersCompletedTheQuestion": 3.2222222222222,
                "percentFinishedLearners": 80.555555555556,
                "percentCorrect": 44.444444444444,
                "pointBiserial": 0.19245008972988
            },
            "high": {
                "percentCorrect": 100
            },
            "low": {
                "percentCorrect": 0
            },
            "median": {
                "percentCorrect": 33.333333333333
            }
        }
    }
}
```

> 200 (Team)

```json
{
    "data": {
        "uuid": "9665e76f-5cb6-4eb8-bf4f-9118f2d7fc10",
        "itemAnalysis": {
            "item": [
                {
                    "question": {
                        "id": 1547,
                        "group": 1,
                        "order": 1,
                        "question": "Who is the President of the Philippines?",
                        "type": "mcqs",
                        "options": [
                            {
                                "key": "A",
                                "tags": [],
                                "content": "Rodrigo Duterte",
                                "remarks": "",
                                "isCorrect": true,
                                "contentIsHTML": true
                            },
                            {
                                "key": "B",
                                "tags": [],
                                "content": "Bong Go",
                                "remarks": "",
                                "isCorrect": false,
                                "contentIsHTML": true
                            },
                            {
                                "key": "C",
                                "tags": [],
                                "content": "Gloria Arroyo",
                                "remarks": "",
                                "isCorrect": false,
                                "contentIsHTML": true
                            }
                        ],
                        "score": 5
                    },
                    "options": [
                        {
                            "key": "A",
                            "isCorrect": true,
                            "allAttempts": [
                                [
                                    "A"
                                ]
                            ],
                            "countOfThisKeyInFirstAttempts": 1,
                            "percent": 100,
                            "answersPerOption": [
                                {
                                    "teamID": 208,
                                    "userPlacementTestID": 16045,
                                    "dateCompleted": {
                                        "date": "2019-08-17 00:48:30.000000",
                                        "timezone_type": 3,
                                        "timezone": "UTC"
                                    },
                                    "duration": 11,
                                    "attempts": [
                                        "A"
                                    ],
                                    "finalPoint": "5.00"
                                }
                            ]
                        },
                        {
                            "key": "B",
                            "isCorrect": false,
                            "allAttempts": [
                                [
                                    "A"
                                ]
                            ],
                            "countOfThisKeyInFirstAttempts": 0,
                            "percent": 0,
                            "answersPerOption": []
                        },
                        {
                            "key": "C",
                            "isCorrect": false,
                            "allAttempts": [
                                [
                                    "A"
                                ]
                            ],
                            "countOfThisKeyInFirstAttempts": 0,
                            "percent": 0,
                            "answersPerOption": []
                        }
                    ],
                    "pointsOfAllTeams": [
                        "5.00"
                    ],
                    "countOfTeamsWithAnswer": 1,
                    "countOfTeamsWithNoAnswer": 0,
                    "presentTeams": 1,
                    "percents": [
                        100,
                        0,
                        0,
                        0
                    ],
                    "emptyAnswers": 0,
                    "averageCompletionTimePerQuestion": "11 Sec",
                    "percentFinishedTeams": 100,
                    "overallPercentCorrect": 100,
                    "firstAttemptPercentCorrect": 100,
                    "failRate": 0
                }
            ],
            "mean": {
                "failRate": 38.666666666667,
                "totalTime": "9 Sec",
                "noOfTeamsCompletedTheQuestion": 1,
                "percentFinishedTeams": 100,
                "overallPercentCorrect": 61.333333333333,
                "firstAttemptPercentCorrect": 50
            },
            "high": {
                "overallPercentCorrect": 100,
                "firstAttemptPercentCorrect": 100
            },
            "low": {
                "overallPercentCorrect": 0,
                "firstAttemptPercentCorrect": 0
            },
            "median": {
                "overallPercentCorrect": 80,
                "firstAttemptPercentCorrect": 50
            }
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

This resource allows to list the activity question analytics.

### HTTP Request

`GET [BASE_URL]/tests/{test-uuid}/dashboard/item`

### HTTP Get Parameters

`No HTTP get parameters required.`

### Request Headers
Key | Value | Description
--------- | ------- | -----------
`Content-Type` | **application/json** | Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
`Authorization` | **Bearer $token** | Lorem ipsum dolor sit amet, consectetur adipiscing elit.


### HTTP Post Parameters

`No HTTP post parameters required.`






## Student/Team

> 200 (Individual)

```json
{
    "data": {
        "uuid": "00ead9a8-8b51-4382-9b96-891a0d1de85c",
        "studentAnalysis": {
            "students": [
                {
                    "rank": 1,
                    "fullname": "C2P1-1-1s2",
                    "identity": "C2P1-1-1s2",
                    "email": null,
                    "organisationID": "C2P1-1-1s2",
                    "team": "Team 1",
                    "status": "Submitted",
                    "answeredQuestions": 9,
                    "countActivityQuestions": 9,
                    "percentFinished": 100,
                    "totalPoint": 5,
                    "finishedOnPercentCorrect": 55.555555555556,
                    "totalTimeTaken": "47 Sec",
                    "questions": [
                        {
                            "studentAnswer": "A",
                            "attempts": [
                                "A"
                            ],
                            "isCorrect": true,
                            "point": "1.00",
                            "percent": 100
                        }
                    ]
                }
            ],
            "studentsFinishedOnPercentCorrect": [
                44.444444444444,
                55.555555555556,
                50,
                33.333333333333
            ],
            "mean": {
                "answeredQuestions": 1.16,
                "percentFinished": 7.25,
                "score": 0.52,
                "finishedOnPercentCorrect": 45.833333333333,
                "studentsTotalTime": "4 Sec"
            },
            "high": {
                "finishedOnPercentCorrect": 55.555555555556
            },
            "low": {
                "finishedOnPercentCorrect": 33.333333333333
            },
            "median": {
                "finishedOnPercentCorrect": 47.222222222222
            }
        }
    }
}
```

> 200 (Team)

```json
{
    "data": {
        "uuid": "9665e76f-5cb6-4eb8-bf4f-9118f2d7fc10",
        "teamAnalysis": {
            "teams": [
                {
                    "rank": 1,
                    "team": "Team 1",
                    "reporter": "C2P1-1-1s1",
                    "status": "Submitted",
                    "answeredQuestions": 10,
                    "countActivityQuestions": 10,
                    "percentFinished": 100,
                    "totalPoint": 28,
                    "finishedQuestionPercentCorrect": 60.869565217391,
                    "percentCorrectOnFirstAttempt": 50,
                    "totalTimeTaken": "6 Min, 40 Sec",
                    "questions": [
                        {
                            "options": [
                                {
                                    "key": "A",
                                    "tags": [],
                                    "content": "Rodrigo Duterte",
                                    "remarks": "",
                                    "isCorrect": true,
                                    "contentIsHTML": true
                                },
                                {
                                    "key": "B",
                                    "tags": [],
                                    "content": "Bong Go",
                                    "remarks": "",
                                    "isCorrect": false,
                                    "contentIsHTML": true
                                },
                                {
                                    "key": "C",
                                    "tags": [],
                                    "content": "Gloria Arroyo",
                                    "remarks": "",
                                    "isCorrect": false,
                                    "contentIsHTML": true
                                }
                            ],
                            "studentAnswer": "A",
                            "attempts": [
                                "A"
                            ],
                            "isCorrect": true,
                            "point": "5.00",
                            "percent": 100,
                            "percentCorrect": 100
                        }
                    ]
                }
            ],
            "teamFinishedQuestionPercentCorrect": [
                60.869565217391
            ],
            "mean": {
                "answeredQuestions": 2,
                "percentFinished": 10,
                "score": 5.6,
                "finishedQuestionPercentCorrect": 60.869565217391,
                "percentCorrectOnFirstAttempt": 50,
                "studentsTotalTime": "1 Min, 20 Sec"
            },
            "high": {
                "finishedOnPercentCorrect": 60.869565217391,
                "percentCorrectOnFirstAttempt": 50
            },
            "low": {
                "finishedOnPercentCorrect": 60.869565217391,
                "percentCorrectOnFirstAttempt": 50
            },
            "median": {
                "finishedOnPercentCorrect": 60.869565217391,
                "percentCorrectOnFirstAttempt": 50
            }
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

This resource allows to list the activity student and team analytics.

### HTTP Request

`GET [BASE_URL]/tests/{test-uuid}/dashboard/student`

### HTTP Get Parameters

`No HTTP get parameters required.`

### Request Headers
Key | Value | Description
--------- | ------- | -----------
`Content-Type` | **application/json** | Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
`Authorization` | **Bearer $token** | Lorem ipsum dolor sit amet, consectetur adipiscing elit.


### HTTP Post Parameters

`No HTTP post parameters required.`