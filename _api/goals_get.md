---
title: /goals/:id
position: 3.3
type: get
description: Get a goal
parameters:
  - name:
    content:
content_markdown: |-
  Returns a specific goal from the database
left_code_blocks:
  - code_block: |-
      $.get("http://api.kapitalwise.com/goals/123", {
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
       "name": "Pay credit card bill",
       "description": "this is a goal",
       "iconUrl": "abc.com/icon",
       "status": "ACTIVE"
      }
    title: Response
    language: json
  - code_block: |2-
      {
        "error": true,
        "message": "Goal doesn't exist"
      }
    title: Error
    language: json
---
