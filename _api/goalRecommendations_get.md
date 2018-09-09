---
title: /users/:id/goals
position: 1.6
type: get
description: Recommended financial goals for a user
parameters:
content_markdown: |-
  Returns a set of goal recommendations for the user based on the next best action algorithm. We consider the user's current financial habits and spending patterns to recommend the set of goals that the user would want to save towards.
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
            "iconUrl": "https://www.cdn.kapitalwise.com/bin-public/060_www_kw_com/images/goal_thumb1.jpg"
        },
        "user": 201,
        "target": 22500.00,
        "status": "ACTIVE",
        "isDefault": false
        },
        {
        "id": 2,
        "goal": {
            "id": 2,
            "name": "Paydown Credit Card Balance",
            "description": "Credit card debt can put a serious drag on your net worth. If you have high interest credit card debt or several different credit card bills to pay every month, it can make a lot of sense to take advantage of a 0% APR balance transfer offer as well.",
             "iconUrl": "https://www.cdn.kapitalwise.com/bin-public/060_www_kw_com/images/goal_thumb2.jpg"
        },
        "user": 201,
        "target": 3500.00,
        "status": "ACTIVE",
        "isDefault": false
        },
        {
        "id": 3,
        "goal": {
            "id": 7,
            "name": "Custom Goal",
            "description": "Persoanl goal to do something, get something or go somewhere ",
            "iconUrl": "https://www.cdn.kapitalwise.com/bin-public/060_www_kw_com/images/goal_thumbx.jpg"
        },
        "user": 201,
        "target": 0.00,
        "status": "ACTIVE",
        "isDefault": true
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
