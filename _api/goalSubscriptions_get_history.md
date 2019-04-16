---
title: /goalSubscriptions/:id/history
position: 5.6
type: get
description: Get funding history for the goal
parameters:
  - name:
    content:
content_markdown: |-
  Returns funding history
left_code_blocks:
  - code_block: |-
      $.get("http://api.kapitalwise.com/goalSubscriptions/1/history", {
        token: "YOUR_APP_KEY",
      }, function(data) {
        alert(data);
      });
    title: jQuery
    language: javascript
right_code_blocks:
  - code_block: |2-
      {
        "id": 1,
        "fundings": [
          {
            "id": 1,
            "amount": 34,
            "asOfDate": "2019-04-03T18:30:00.000Z",
            "status": "PROCESSED"
          }
        ]
      }
    title: Response
    language: json
  - code_block: |2-
      {
        "error": true,
        "message": "Goal Subscription doesn't exist"
      }
      {
        "error": true,
        "message": "No history of funding found"
      }
    title: Error
    language: json
---
