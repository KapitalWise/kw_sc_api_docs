---
title: /goals
position: 3.2
type: post
description: Create a goal
parameters:
  - name: name
    content: Goal name
  - name: description
    content: A short description about the goal
  - name: iconUrl
    content: URL for the an icon of the goal

content_markdown: |-
  Adds a goal to the database
  {: .success}

left_code_blocks:
  - code_block: |-
      $.post("http://api.kapitalwise.com/goals/", {
      "token": "YOUR_APP_KEY",
      "name": "Pay car loan",
      "description": "this is a goal",
      "iconUrl": "abc.com/icon"
      }, function(data) {
        alert(data);
      });
    title: jQuery
    language: javascript
right_code_blocks:
  - code_block: |-
      {
        "id": 3,
        "name": "Pay car loan",
        "description": "this is a goal",
        "iconUrl": "abc.com/icon",
        "status": "ACTIVE"
      }
    title: Response
    language: json
  - code_block: |-
      {
        "error": true,
        "message": "Necessary parameter(s) are missing"
      }
    title: Error
    language: json
---
