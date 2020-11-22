
# Backend Development Workflow

```sh
virtualenv env
env\Scripts\activate
pip install -r requirements.txt
python manage.py makemigrations
python manage.py migrate
python manage.py createsuperuser
python manage.py runserver
```

# Api testing URL
---

# Login - 127.0.0.1:8000/api/auth/login/
```sh
{
    "username": "XXX",
    "password": "XXXXXXXX"
}
```
 # Register - 127.0.0.1:8000/api/auth/register/
```sh
{
    "name": "xxxxx",
    "username": "xx",
    "password": "xxxxx",
    "email": "xxxx@xxx.xxx"
}
```
# Quizzes - 127.0.0.1:8000/api/quizzes/

pass the headers values
| KEY | VALUE |
|-------------|------------------|
|Authorization | your Token |
| Content-Type | application/json |
|Authorization | your Token Value |

# SingleQuiz - 127.0.0.1:8000/api/quizzes/javascript-quiz

pass the headers values
| KEY | VALUE |
|-------------|------------------|
|Authorization | your Token |
| Content-Type | application/json |
|Authorization | your Token Value |

output
```sh
{
    "quiz": {
        "id": 1,
        "quiztakers_set": {
            "id": 1,
            "usersanswer_set": [
                {
                    "id": 1,
                    "quiz_taker": 1,
                    "question": 1,
                    "answer": null
                },
                {
                    "id": 2,
                    "quiz_taker": 1,
                    "question": 2,
                    "answer": null
                },
                {
                    "id": 3,
                    "quiz_taker": 1,
                    "question": 3,
                    "answer": null
                },
                {
                    "id": 4,
                    "quiz_taker": 1,
                    "question": 4,
                    "answer": null
                },
                {
                    "id": 5,
                    "quiz_taker": 1,
                    "question": 5,
                    "answer": null
                },
                {
                    "id": 6,
                    "quiz_taker": 1,
                    "question": 6,
                    "answer": null
                }
            ],
            "score": 0,
            "completed": false,
            "date_finished": null,
            "timestamp": "2020-11-22T17:54:37.776830Z",
            "user": 2,
            "quiz": 1
        },
        "question_set": [
            {
                "id": 1,
                "answer_set": [
                    {
                        "id": 1,
                        "question": 1,
                        "label": "javascript"
                    },
                    {
                        "id": 2,
                        "question": 1,
                        "label": "scripting"
                    },
                    {
                        "id": 3,
                        "question": 1,
                        "label": "script"
                    },
                    {
                        "id": 4,
                        "question": 1,
                        "label": "js"
                    }
                ],
                "label": "LABEL QUESTIONS ????",
                "order": 0,
                "quiz": 1
            },
            {
                "id": 2,
                "answer_set": [
                    {
                        "id": 5,
                        "question": 2,
                        "label": "None of the above"
                    },
                    {
                        "id": 6,
                        "question": 2,
                        "label": "Secured and Progressive App"
                    },
                    {
                        "id": 7,
                        "question": 2,
                        "label": "SOLID Principles for Application"
                    },
                    {
                        "id": 8,
                        "question": 2,
                        "label": "Single Page Application"
                    }
                ],
                "label": "Inside which HTML element do we put the JavaScript?",
                "order": 0,
                "quiz": 1
            },
            {
                "id": 3,
                "answer_set": [
                    {
                        "id": 9,
                        "question": 3,
                        "label": "dim"
                    },
                    {
                        "id": 10,
                        "question": 3,
                        "label": "let"
                    },
                    {
                        "id": 11,
                        "question": 3,
                        "label": "const"
                    },
                    {
                        "id": 12,
                        "question": 3,
                        "label": "var"
                    }
                ],
                "label": "What is the full form of SPA",
                "order": 0,
                "quiz": 1
            },
            {
                "id": 4,
                "answer_set": [
                    {
                        "id": 13,
                        "question": 4,
                        "label": "Displayed text in non-JavaScript browsers."
                    },
                    {
                        "id": 14,
                        "question": 4,
                        "label": "Prevents Script Execution"
                    },
                    {
                        "id": 15,
                        "question": 4,
                        "label": "Requests user not to run scripts"
                    },
                    {
                        "id": 16,
                        "question": 4,
                        "label": "None of the above"
                    }
                ],
                "label": "Which of these keyword is NOT used to declare a variable in Javascript?",
                "order": 0,
                "quiz": 1
            },
            {
                "id": 5,
                "answer_set": [
                    {
                        "id": 17,
                        "question": 5,
                        "label": "alert('Hello World');"
                    },
                    {
                        "id": 18,
                        "question": 5,
                        "label": "display 'Hello World'"
                    },
                    {
                        "id": 19,
                        "question": 5,
                        "label": "msgBox(\\\"Hello World\\\");"
                    },
                    {
                        "id": 20,
                        "question": 5,
                        "label": "alertBox(\\\"Hello World\\\");"
                    }
                ],
                "label": "What does the <noscript> tag used for?",
                "order": 0,
                "quiz": 1
            },
            {
                "id": 6,
                "answer_set": [],
                "label": "How do you write \\\"Hello World\\\" in an alert box?",
                "order": 0,
                "quiz": 1
            }
        ],
        "name": "Javascript Quiz",
        "description": "Javascript Quiz (contains web develepment, Javascript, ES 5/6/7, etc.)",
        "image": "http://127.0.0.1:8000/media/bg1.png",
        "slug": "javascript-quiz",
        "roll_out": false,
        "timestamp": "2020-11-22T17:53:52.550936Z"
    },
    "last_question_id": null
}
```
# My-Quiz 127.0.0.1:8000/api/my-quizzes/ 

pass the headers values
| KEY | VALUE |
|-------------|------------------|
|Authorization | your Token |
| Content-Type | application/json |
|Authorization | your Token Value |

output
```sh
[
    {
        "id": 1,
        "name": "Javascript Quiz",
        "description": "Javascript Quiz (contains web develepment, Javascript, ES 5/6/7, etc.)",
        "image": "http://127.0.0.1:8000/media/bg1.png",
        "slug": "javascript-quiz",
        "questions_count": 6,
        "completed": false,
        "score": null,
        "progress": 0
    }
]
```

# save-answer - 127.0.0.1:8000/api/save-answer/
# submit - 127.0.0.1:8000/api/quizzes/javascript-quiz/submit/