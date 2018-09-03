---
title: /users/:id/nudges
position: 1.7
type: get
description: Return nudges(notifications) for a user
parameters:
content_markdown: |-
  Returns a set of nudges for a user
  {: .info}
left_code_blocks:
  - code_block: |-
      $.get("http://api.kapitalwise.com/users/123/nudges", {
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
        "user": 201,
        "goalSubscription": 5,
        "description": "Fund your goal by the amount we predicted after analyzing your profile",
        "accountBalance": 100,
        "predictedAccountBalance": 120,
        "predictedGoalFunding": 10
        }
        ]

    title: Response
    language: json
  - code_block: |2-
      {
        "error": true,
        "message": "No nudges found"
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
