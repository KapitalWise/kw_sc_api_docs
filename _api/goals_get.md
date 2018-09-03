---
title: /goals/:id
position: 3.2
type: get
description: Get a goal
parameters:
  - name:
    content:
content_markdown: |-
  Returns a specific goal from the database
left_code_blocks:
  - code_block: |-
      $.get("http://api.kapitalwise.com/goals/123", {
        token: "YOUR_APP_KEY",
      }, function(data) {
        alert(data);
      });
    title: jQuery
    language: javascript
right_code_blocks:
  - code_block: |2-
        {
        "id": 1,
        "name": "Emergency Savings",
        "description": "Your recommended Emergency Savings is intended to help you prepare for unexpected expenses. Depending on the assets you've, we recommend having between 3-6 months of your annual household income set aside for emergencies",
        "iconUrl": null,
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
