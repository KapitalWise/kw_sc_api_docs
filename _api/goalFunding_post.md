---
title: /goalSubscriptions/:id/fund
position: 5.5
type: post
description: Fund the goal to meet the target
parameters:
  - name: amount
    content: Goal funding amount approved by user
content_markdown: |-
  Fund the goal to meet the target
  {: .success}

left_code_blocks:
  - code_block: |-
      $.post("http://api.kapitalwise.com/goalSubscriptions/5/fund", {
      "token": "YOUR_APP_KEY",
      "amount": "150.00"
      }, function(data) {
        alert(data);
      });
    title: jQuery
    language: javascript
right_code_blocks:
  - code_block: |-
        {
        "id": 1,
        "goalSubscription": 5,
        "amount": 120.00,
        "status": "OPEN"
        }

    title: Response
    language: json
  - code_block: |-
      {
        "error": true,
        "message": "Necessary parameter(s) are missing"
      }
      {
        "error": true,
        "message": "Goal subscription doesn't exist"
      }
      {
        "error": true,
        "message": "Something went wrong on server-side"
      }
    title: Error
    language: json
---
