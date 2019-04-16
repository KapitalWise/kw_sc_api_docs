---
title: /goalSubscriptions/:id/transactions
position: 5.5
type: get
description: Get transaction logs which contributed to this goal
parameters:
  - name:
    content:
content_markdown: |-
  Returns transactions
left_code_blocks:
  - code_block: |-
      $.get("http://api.kapitalwise.com/goalSubscriptions/1/transactions", {
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
        "transactions": [
          {
            "id": 1,
            "accountId": 1,
            "accountName": "sc",
            "amount": 34,
            "roundup": 66,
            "date": "2019-04-03T18:30:00.000Z",
            "status": "PROCESSED"
          },
          {
            "id": 2,
            "accountId": 1,
            "accountName": "sc",
            "amount": 45.5,
            "roundup": 54.5,
            "date": "2019-04-03T18:30:00.000Z",
            "status": "OPEN"
          }
        ]
      }
    title: Response
    language: json
  - code_block: |2-
      {
        "error": true,
        "message": "Goal Subscription doesn't exist"
      }
      {
        "error": true,
        "message": "No transactions found"
      }
    title: Error
    language: json
---
