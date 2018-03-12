---
title: /investment/:id/history
position: 5.1
type: get
description: Get the history of all investments
parameters:
  - name: 
    content: 
content_markdown: |-
  Get all the past investments associated with this investment.
left_code_blocks:
  - code_block: |-
      $.ajax({
        "url": "http://api.kapitalwise.com/investment/3/history",
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
        "accountBalance" : 12200.00,
        "investmentAmount": 11200.00, 
        "pendingBalance": 7.00,
        "investmentThreshold": 10.00,
        "icon_url": "https://image.ibb.co/b96EUa/ABSA1.png",
        "holdings": [
          {
            "fundName" : "SELECT EQUITY FUNDS",
            "fundId" : 2,
            "weight": 25,
            "closePrice": 123.00,
            "fundIcon_url": "https://image.ibb.co/b96EUa/Core.png",
            "fundFactsheet_url": "https://www.absainvestments.co.za/wealth-and-investment-management/e-docs/fund-fact-sheets/Absa%20Select%20Equity%20Fund.pdf"
          },
          {
            "fundName" : "BALANCED FUND",
            "fundId" : 3,
            "weight": 75,
            "closePrice": 423.00,
            "fundIcon_url": "http://image.ibb.co/iNKqX5/Balance.png",
            "fundFactsheet_url": "https://www.absainvestments.co.za/wealth-and-investment-management/e-docs/fund-fact-sheets/Absa%20Balanced%20Fund.pdf"
          }
        ],
        "performance": [
          {
            "asofdate": "2017-12-06 17:46:48",
            "balance": 10100.00,
            "gain": 100.00
          },
          {
            "asofdate": "2017-11-29 17:46:48",
            "balance": 90100.00,
            "gain": 100.00
          },
          {
            "asofdate": "2017-11-19 17:46:48",
            "balance": 8100.00,
            "gain": 100.00
          },
          {
            "asofdate": "2017-11-12 17:46:48",
            "balance":7000.00,
            "gain": 100.00
          }
        ],
        "created" : "2017-11-12 17:46:48"
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