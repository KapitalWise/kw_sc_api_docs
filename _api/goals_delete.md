---
title: /goals/:id
position: 3.5
type: delete
description: Deletes a goal
parameters:
  - name:
    content:
content_markdown: |-
  Deletes a goal from the database.
left_code_blocks:
  - code_block: |-
      $.ajax({
        "url": "http://api.kapitalwise.com/goals/123",
        "type": "DELETE",
        "data": {
          "token": "YOUR_APP_KEY"
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
        "id": 123,
        "status": "DELETED"
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

