---
title: /goalSubscriptions/:id
position: 5.2
type: get
description: Get a goal subscription
parameters:
  - name:
    content:
content_markdown: |-
  Returns a specific goal subscription from the database
left_code_blocks:
  - code_block: |-
      $.get("http://api.kapitalwise.com/goalSubscriptions/123", {
        token: "YOUR_APP_KEY",
      }, function(data) {
        alert(data);
      });
    title: jQuery
    language: javascript
right_code_blocks:
  - code_block: |2-
      {
        "id": 5,
        "goalSuggestion": 1,
        "description": "My Emergency Savings Goal",
        "user": 201,
        "target": 100,
        "funded": 0,
        "pending": 12,
        "startDate": "2018-07-17T18:30:00.000Z",
        "endDate": null,
        "nudge": true,
        "status": "ACTIVE"
      }
    title: Response
    language: json
  - code_block: |2-
      {
        "error": true,
        "message": "Goal Subscription doesn't exist"
      }
    title: Error
    language: json
---
