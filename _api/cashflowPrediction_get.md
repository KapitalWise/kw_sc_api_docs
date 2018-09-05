---
title: /users/:id/cashflow
position: 1.9
type: get
description: Predicts cashflow for a user
parameters:
content_markdown: |-
  Returns the predicted future cashflow for all the accounts of the user
  {: .info}
left_code_blocks:
  - code_block: |-
      $.get("http://api.kapitalwise.com/users/123/cashflow", {
        token: "YOUR_APP_KEY",
      }, function(data) {
        alert(data);
      });
    title: jQuery
    language: javascript
right_code_blocks:
  - code_block: |2-
        [{
         "id": 1,
         "user": 201,
         "account": 652
         "recurringExpense": 50,
         "income": 150,
         "miscellaneousExpense": 30,
         "miscellaneousIncome": 50,
         "predictedAccountBalance": 120,
         "predictedFunding": 10,
         "asOfDate": "2018-09-02T00:00:00.000Z"
        },
        {
         "id": 2,
         "user": 201,
         "account": 653
         "recurringExpense": 7860,
         "income": 11147,
         "miscellaneousExpense": 4735,
         "miscellaneousIncome": 1945,
         "predictedAccountBalance": 53657,
         "predictedFunding": 544,
         "asOfDate": "2018-09-02T00:00:00.000Z"
        }]
        

    title: Response
    language: json
  - code_block: |2-
      {
        "error": true,
        "message": "No cashflow predictions found"
      }
      {
        "error": true,
        "message": "Necessary parameter(s) are missing"
      }
      {
        "error": true,
        "message": "Something went wrong on server-side"
      }
      {
        "error": true,
        "message": "User doesn\'t exist"
      }
    title: Error
    language: json
---
