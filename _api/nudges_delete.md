---
title: /nudges/:id
position: 1.91
type: delete
description: Deletes a nudge
parameters:
  - name:
    content:
content_markdown: |-
  Deletes a nudge in the system.
left_code_blocks:
  - code_block: |-
      $.ajax({
        "url": "http://api.kapitalwise.com/nudges/3",
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
        "message": "Nudge doesn't exist"
      }
    title: Error
    language: json
---

