---
title: /goalSubscriptions
position: 5.1
type: post
description: Create a goal Subscription
parameters:
  - name: user
    content: User id of the subscriber
  - name: goalSuggestion
    content: The goal suggestion chosen by the user
  - name: description
    content: User defined goal description
  - name: target
    content: Target amount for the goal
  - name: goalPreferences
    content: An array of user goal preference objects containing 'keyName' and 'value' 

content_markdown: |-
  Lets User subscribe to a Goal.
  {: .success}

left_code_blocks:
  - code_block: |-
      $.post("http://api.kapitalwise.com/goalSubscriptions/", {
      "token": "YOUR_APP_KEY",
      "goalSuggestion": "1",
      "user": "201",
      "description": "My Emergency Savings Goal",
      "target": 22000.00,
      "goalPreferences": [{"keyName": "ROUNDUP", "value": 100}]
      }, function(data) {
        alert(data);
      });
    title: jQuery
    language: javascript
right_code_blocks:
  - code_block: |-
      {
        "id": 5,
        "goalSuggestion": 1,
        "description": "My Emergency Savings Goal",
        "user": 201,
        "target": 22000.00,
        "startDate": "2018-07-17T18:30:00.000Z",
        "endDate": null
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
        "message": "Goal suggestion doesn't exist"
      }
      {
        "error": true,
        "message": "Goal suggestion doesn't belong to this user"
      }
      {
        "error": true,
        "message": "Something went wrong on server-side"
      }
      {
        "error": true,
        "message": "Rule doesn\'t exist"
      }
    title: Error
    language: json
---