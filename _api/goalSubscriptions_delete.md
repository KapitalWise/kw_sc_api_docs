---
title: /goalSubscriptions/:id
position: 5.4
type: delete
description: Deletes a goal subscription
parameters:
  - name:
    content:
content_markdown: |-
  Deletes a goal subscription from the database.
left_code_blocks:
  - code_block: |-
      $.ajax({
        "url": "http://api.kapitalwise.com/goalSubscriptions/123",
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
        "message": "Goal subscription doesn't exist"
      }
    title: Error
    language: json
---

