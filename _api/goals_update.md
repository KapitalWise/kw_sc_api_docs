---
title: /goals/:id
position: 3.4
type: put
description: Update Goal
parameters:
  - name: name
    content: Goal name
  - name: description
    content: A short description about the goal
  - name: iconUrl
    content: URL for the an icon of the goal
content_markdown: |-
  Update an existing goal in the database.
left_code_blocks:
  - code_block: |-
      $.ajax({
        "url": "http://api.kapitalwise.com/goals/3",
        "type": "PUT",
        "data": {
          "token": "YOUR_APP_KEY",
      "name": "Pay car loan",
      "description": "this is a goal",
      "iconUrl": "abc.com/icon"
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
        "name": "Pay car loan",
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