---
title: /accounts/:id
position: 2.5
type: delete
description: Deletes an account
parameters:
  - name:
    content:
content_markdown: |-
  Deletes an account from the system
left_code_blocks:
  - code_block: |-
      $.ajax({
        "url": "http://api.kapitalwise.com/accounts/3",
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
        "message": "Account doesn't exist"
      }
    title: Error
    language: json
---

