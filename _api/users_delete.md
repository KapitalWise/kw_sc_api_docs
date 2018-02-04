---
title: /users/:id
position: 1.5
type: delete
description: Deletes a user
parameters:
  - name:
    content:
content_markdown: |-
  Deletes a user in the system.
left_code_blocks:
  - code_block: |-
      $.ajax({
        "url": "http://api.kapitalwise.com/users/3",
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
        "id": 3,
        "status": "deleted"
      }
    title: Response
    language: json
  - code_block: |2-
      {
        "error": true,
        "message": "User doesn't exist"
      }
    title: Error
    language: json
---

