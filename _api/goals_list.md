---
title: /goals
position: 3.1
type: get
description: List all Goals
parameters:
  - name: offset
    content: Offset the results by this amount
  - name: limit
    content: Limit the number of goals returned
content_markdown: |-
  This call will return a maximum of 100 goals.
  {: .info}
  Lists all the goals in the system. You can paginate by using the parameters listed above.
left_code_blocks:
  - code_block: |-
      $.get("http://api.kapitalwise.com/goals", {
        token: "YOUR_APP_KEY",
      }, function(data) {
        alert(data);
      });
    title: jQuery
    language: javascript
right_code_blocks:
  - code_block: |2-
      [
        { 
       "id": 1,
       "name": "Pay credit card bill",
       "description": "this is a goal",
       "iconUrl": "abc.com/icon1",
       "status": "ACTIVE"
        },
        { 
       "id": 2,
       "name": "Pay car loan",
       "description": "this is a goal",
       "iconUrl": "abc.com/icon2",
       "status": "ACTIVE"
        }
      ]
    title: Response
    language: json
  - code_block: |2-
      {
        "error": true,
        "message": "Necessary parameter(s) are missing"
      }
      {
        "error": true,
        "message": "Invalid offset/limit"
      }
      {
        "error": true,
        "message": "Goal doesn't exist"
      }
    title: Error
    language: json
---
