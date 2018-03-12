---
title: /analytics/:id
position: 8.0
type: get
description: Get user's personal financial analytics
parameters:
  - name:
    content:
content_markdown: |-
  The /analytics/:id endpoint allows developers to receive user financial analytics data for credit and depository-type Accounts. Analytics data is standardized across accounts. This API also provides predicted future cash flow and account balances for the user.
left_code_blocks:
  - code_block: |-
      $.get("http://api.kapitalwise.com/analytics/3", {
        token: "YOUR_APP_KEY",
      }, function(data) {
        alert(data);
      });
    title: jQuery
    language: javascript
right_code_blocks:
  - code_block: |2-
      {
        "accountBalance": 700000.00,
        "creditCardDebt": 3400.00,
        "accountsLinked": 5,
        "hasMortgage": yes,
        "hasAutoLoan": yes,
        "hasChildSupport": yes,
        "incomeType": "salaried",
        "income": 11000.00,
        "top10SpendingPercent":
        {
             "home" : 15,
             "bills" : 5,
             "dining": 7,
             "travel": 8,
             "shopping" : 23,
             "childCare": 20,
             "insurance": 2,
             "entertainment": 3,
             "other": 16
        },
        "top3OverSpendingPercent":
        {
          "autoInsurance" : 1.5,
          "gas&Fuel" : 3,
          "mobilePhone": 2
        },
        "spending12Months":
        {
           "Jan2018": 7000.00,
           "Dec2017" : 8500.00,
           "Nov2017": 6500.00,
           "Oct2017": 6400.00,
           "Sept2017" : 7560.00,
           "Aug2017": 6600.00,
           "Jul2017": 5400.00,
           "Jun2017" : 2500.00,
           "May2017": 3500.00,
           "Apr2017": 6900.00,
           "March2017" : 4500.00,
           "Feb2017": 5500.00
        },
        "Balance12Months":
        {
           "Jan2018": 66000.00,
           "Dec2017" : 60500.00,
           "Nov2017": 65000.00,
           "Oct2017": 64000.00,
           "Sept2017" : 71060.00,
           "Aug2017": 66600.00,
           "Jul2017": 65400.00,
           "Jun2017" : 52500.00,
           "May2017": 63500.00,
           "Apr2017": 61900.00,
           "March2017" : 54500.00,
           "Feb2017": 65500.00
        },
        "top10Spending12Months":
        {
           "home" : 36900.00,
           "bills" : 1500.00,
           "dining": 708.00,
           "travel": 1900.00,
           "shopping" : 2300.00,
           "childCare": 22000.00,
           "insurance": 2040.00,
           "entertainment": 789.00,
           "other": 16000.00
        },
        "debt12Months":
        {
           "Jan2018": 4520.00,
           "Dec2017" : 6010.00,
           "Nov2017": 5005.00,
           "Oct2017": 6404.00,
           "Sept2017" : 3460.00,
           "Aug2017": 6600.00,
           "Jul2017": 6540.00,
           "Jun2017" : 5250.00,
           "May2017": 6350.00,
           "Apr2017": 6100.00,
           "March2017" : 5450.00,
           "Feb2017": 6550.00
        },
        "recurringExpense":
        {
          "publicService": 240.00,
          "townGas" : 210,
          "homeMtg": 3600.00,
          "mobilePhone": 169.00,
          "insurance": 150.00
        },
       "Predictions":
         {
         "nextWeekCashflow": 300.00,
         "nextMontCashflow": 11300.00,
         "nextWeekAccBal": 71000.00
         "nextMonthAccBal": 68000.00
         },
       "savingTips": ["You spending 7% more on car insurance", "Pay with your Amex 42000 when you dine out and get 2% cash back"]
      }
    title: Response
    language: json
  - code_block: |2-
      {
        "error": true,
        "message": "User doesn't exist"
      }
    title: Error
    language: json
---





