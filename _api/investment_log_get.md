---
title: /investment/:id/log
position: 5.2
type: get
description: Get the logs for an investment. The logs are transactions contributed to an investment, eg. the transactions we rounded-up to make an investment
parameters:
  - name: 
    content: 
content_markdown: |-
  Get all the past investments associated with this investment.
left_code_blocks:
  - code_block: |-
      $.ajax({
        "url": "http://api.kapitalwise.com/investment/3/log",
        "type": "GET",
        "data": {
          "token": "YOUR_APP_KEY",
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
        "id" : 3,
        "transactions": [
        {
          "id": 1,
          "accountId" : 343,
          "accountName" : "Chase Saving",
          "iconUrl": "http://content.kapitalwise.com/images/chase_300_300.png",
          "accountNumber": "XXXX4230",
          "transactionAmount": 23.40,
          "invested_amount": 0.60,
          "transactionDescription": "Lunch at John's burger",
          "created" :  "2017-11-19 17:46:48"
        },
        {
          "id": 2,
          "accountId" : 343,
          "accountName" : "Chase Saving",
          "iconUrl": "http://content.kapitalwise.com/images/chase_300_300.png",
          "accountNumber": "XXXX4230",
          "transactionAmount": 12.50,
          "investedAmount": 0.60,
          "transactionDescription": "Shake Shack 42nd Street",
          "created" :  "2017-11-20 17:46:48"
        },
        {
          "id": 3,
          "accountId" : 343,
          "accountName" : "Chase Saving",
          "iconUrl": "http://content.kapitalwise.com/images/chase_300_300.png",
          "accountNumber": "XXXX4230",
          "transactionAmount": 23.40,
          "investedAmount": 0.60,
          "transactionDescription": "Lunch at John's burger",
          "created" :  "2017-11-21 17:46:48"
        },
        {
          "id": 4,
          "account_id" : 343,
          "accountName" : "Chase Saving",
          "iconUrl": "http://content.kapitalwise.com/images/chase_300_300.png",
          "accountNumber": "XXXX4230",
          "transactionAmount": 23.40,
          "investedAmount": 0.60,
          "transactionDescription": "Lunch at John's burger",
          "created" :  "2017-11-22 17:46:48"
        },
        ]

      }
    title: Response
    language: json
  - code_block: |2-
      {
        "error": true,
        "message": "Investment doesn't exist"
      }
    title: Error
    language: json
---