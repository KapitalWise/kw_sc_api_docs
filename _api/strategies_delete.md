---
title: /strategies/:id
position: 3.5
type: delete
description: Deletes a user
parameters:
  - name:
    content:
content_markdown: |-
  Deletes a book in your collection.
left_code_blocks:
  - code_block: |-
      $.ajax({
        "url": "http://api.kapitalwise.com/strategies/123",
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
        "status": "deleted"
      }
    title: Response
    language: json
  - code_block: |2-
      {
        "error": true,
        "message": "Strategy doesn't exist"
      }
    title: Error
    language: json
---

