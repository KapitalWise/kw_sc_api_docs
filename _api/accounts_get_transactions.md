---
title: /accounts/:id/transactions
position: 2.6
type: get
description: Get Transactions of an account
parameters:
  - name:
    content:
content_markdown: |-
  Returns a specific account
left_code_blocks:
  - code_block: |-
      $.get("http://api.kapitalwise.com/accounts/5", {
        token: "YOUR_APP_KEY",
      }, function(data) {
        alert(data);
      });
    title: jQuery
    language: javascript
right_code_blocks:
  - code_block: |2-
      {
        "id": 3,
        "accountName":  "Chase Saving",
        "transactions": [
         {
          "id": 1, 
          "date": "2019-04-03T18:30:00.000Z"
          "amount": 60
         },
         {
          "id": 2, 
          "date": "2019-04-03T18:30:00.000Z"
          "amount": 50
         },
        ]
      }
    title: Response
    language: json
  - code_block: |2-
      {
        "error": true,
        "message": "No transaction found"
      }
      {
        "error": true,
        "message": "Account doesn't exist"
      }
    title: Error
    language: json
---