---
title: /users/:id/nudges
position: 1.7
type: get
description: Return nudges(notifications) for a user
parameters:
content_markdown: |-
  Returns a set of nudges for the user based on cashflow/balance/income predictions. Nudges are messages that would guide users to achieve a financial goal.
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
        "description": "You have $150 extra this week in account ending [2004]. Would you like to move it to savings?",
        "accountBalance": 12300.00,
        "predictedAccountBalance": 14300.00,
        "predictedGoalFunding": 150.00
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
