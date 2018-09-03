---
title: /users/:id/goals
position: 1.6
type: get
description: Recommend goals for a user
parameters:
content_markdown: |-
  Returns a set of goal recommendations for the user
  {: .info}
left_code_blocks:
  - code_block: |-
      $.get("http://api.kapitalwise.com/users/123/goals", {
        token: "YOUR_APP_KEY",
      }, function(data) {
        alert(data);
      });
    title: jQuery
    language: javascript
right_code_blocks:
  - code_block: |2-
       [
       {
        "id": 1,
        "goal": {
            "id": 1,
            "name": "Emergency Savings",
            "description": "Your recommended Emergency Savings is intended to help you prepare for unexpected expenses. Depending on the assets you've, we recommend having between 3-6 months of your annual household income set aside for emergencies",
            "iconUrl": null
        },
        "user": 201,
        "target": 200,
        "status": "ACTIVE"
        },
        {
        "id": 2,
        "goal": {
            "id": 2,
            "name": "Paydown Credit Card Balance",
            "description": "Credit card debt can put a serious drag on your net worth. If you have high interest credit card debt or several different credit card bills to pay every month, it can make a lot of sense to take advantage of a 0% APR balance transfer offer as well.",
            "iconUrl": null
        },
        "user": 201,
        "target": 500,
        "status": "ACTIVE"
        },
        {
        "id": 3,
        "goal": {
            "id": 7,
            "name": "Custom Goal",
            "description": "Persoanl goal to do something, get something or go somewhere ",
            "iconUrl": null
        },
        "user": 201,
        "target": 0,
        "status": "DEFAULT"
        }
        ]

    title: Response
    language: json
  - code_block: |2-
      {
        "error": true,
        "message": "Could not recommend any goal"
      }
      {
        "error": true,
        "message": "Necessary parameter(s) are missing"
      }
      {
        "error": true,
        "message": "Something went wrong on server-side"
      }
      {
        "error": true,
        "message": "User doesn\'t exist"
      }
    title: Error
    language: json
---
