---
title: /users/:id/cashflow
position: 1.9
type: get
description: Predicts cashflow for a user
parameters:
content_markdown: |-
  Returns the predicted future income, account balance, expenses, recurring expenses, miscellaneous expense for each of the accounts for a user
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
         "account":
          {
           "id": 652,
           "accountNumber": "2400",
           "accountType": "checking"
          },
         "accountBalance": 22345.00,
         "recurringExpense": 1850.00,
         "income": 9800.00,
         "miscellaneousExpense": 630.00,
         "miscellaneousIncome": 120.00,
         "predictedAccountBalance": 24560.00,
         "predictedFunding": 10,
         "asOfDate": "2018-09-02T00:00:00.000Z"
        },
        {
         "id": 2,
         "user": 201,
         "account":
          {
           "id": 653,
           "accountNumber": "2401",
           "accountType": "checking"
          },
         "accountBalance": 12000.00,
         "recurringExpense": 0.00,
         "income": 0.00,
         "miscellaneousExpense": 0.00,
         "miscellaneousIncome": 0.00,
         "predictedAccountBalance": 12000,
         "predictedFunding": 0.00,
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
