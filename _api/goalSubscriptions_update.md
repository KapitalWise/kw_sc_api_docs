---
title: /goalSubscriptions/:id
position: 5.3
type: put
description: Update Goal Subscription
parameters:
  - name: goalAmount
    content: Target amount for the goal
  - name: status
    content: ACTIVE/PAUSE
  - name: nudge
    content: Whether the user wants to be nudged for funding approval
content_markdown: |-
  Update an existing goal subscription in the database.
left_code_blocks:
  - code_block: |-
      $.ajax({
        "url": "http://api.kapitalwise.com/goalSubscriptions/3",
        "type": "PUT",
        "data": {
          "token": "YOUR_APP_KEY",
      "goalAmount": 70,
      "status": "PAUSE",
      "nudge": false
        },
        "success": function(data) {
          alert(data);
        }
      });
    title: jQuery
    language: javascript
right_code_blocks:
  - code_block: |2-
      {
        "id": 3,
        "goalRecommendation": 1,
        "user": 1,
        "goalAmount": 70,
        "paidAmount": 0,
        "startDate": "2018-07-17T18:30:00.000Z",
        "endDate": null,
        "nudge": false,
        "status": "PAUSE"
      }
    title: Response
    language: json
  - code_block: |2-
      {
        "error": true,
        "message": "Goal subscription doesn't exist"
      }
      {
        "error": true,
        "message": "Goal subscription status is invalid"
      }
      {
        "error": true,
        "message": "Goal amount is invalid"
      }
    title: Error
    language: json
---