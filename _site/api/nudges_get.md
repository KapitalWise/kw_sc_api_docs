{% comment %}
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
          "id": 4,
          "user": 8,
          "goalSubscription":
            {
             "id": 8,
             "description": "My Custom Description",
             "goalAmount": 100,
             "paidAmount": 0,
             "startDate": "2018-09-09T18:30:00.000Z",
             "endDate": null,
             "nudge": true,
             "status": "ACTIVE",
             "goalRecommendation": 2,
             "user": 8,
             "goalAccount": 1300
            },
           "description": "You will have $537 extra this week in account ending 2400. Would you like to move it to your Goal?",
           "accountBalance": 3353,
           "predictedAccountBalance": 53657,
           "predictedGoalFunding": 537
          },
          {
           "id": 5,
           "user": 8,
           "goalSubscription":
            {
             "id": 8,
             "description": "My Custom Description",
             "goalAmount": 100,
             "paidAmount": 0,
             "startDate": "2018-09-09T18:30:00.000Z",
             "endDate": null,
             "nudge": true,
             "status": "ACTIVE",
             "goalRecommendation": 2,
             "user": 8,
             "goalAccount": 1300
            },
           "description": "You will have $9 extra this week in account ending 2401. Would you like to move it to your Goal?",
           "accountBalance": 3525,
           "predictedAccountBalance": 941,
           "predictedGoalFunding": 9
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
{% endcomment %}