---
title: /goalSubscriptions
position: 5.1
type: post
description: Create a goal Subscription
parameters:
  - name: user
    content: User id of the subscriber
  - name: goalRecommendation
    content: The goal recommendation chosen by the user
  - name: nudge
    content: Whether the user wants to be nudged for funding approval 

content_markdown: |-
  Lets User subscribe to a Goal.
  {: .success}

left_code_blocks:
  - code_block: |-
      $.post("http://api.kapitalwise.com/goalSubscriptions/", {
      "token": "YOUR_APP_KEY",
      "goalRecommendation": "1",
      "user": "1",
      "nudge": true
      }, function(data) {
        alert(data);
      });
    title: jQuery
    language: javascript
right_code_blocks:
  - code_block: |-
      {
        "id": 3,
        "goalRecommendation": 1,
        "user": 1,
        "goalAmount": 50,
        "paidAmount": 0,
        "startDate": "2018-07-17T18:30:00.000Z",
        "endDate": null,
        "nudge": true,
        "status": "ACTIVE"
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
        "message": "Goal recommendation doesn't exist"
      }
      {
        "error": true,
        "message": "Goal recommendation doesn't belong to this user"
      }
    title: Error
    language: json
---
