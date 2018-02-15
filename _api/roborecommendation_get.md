---
title: /robo/recommend
position: 7.0
type: get
description: Return an investment product based on the user's risk tolerence 
parameters:
  - name: questions
    content: Set of questionIds
  - name: answers
    content: Set of answerIds based on the selection in the same order as answer Ids
content_markdown: |-
  This call will return an investment fund based on the user's risk tolerence 
  {: .info }
  Investment fund based on the user's risk tolerence
left_code_blocks:
  - code_block: |-
      $.get("http://api.kapitalwise.com/robo/recommend", { 
      "token": "YOUR_APP_KEY",
      "questionIds":[1,2,3,4],
      "answerIds": [2,3,1,4]
      }, function(data) {
        alert(data);
      });
    title: jQuery
    language: javascript
right_code_blocks:
  - code_block: |2-
      {
        "id" : 123,
        "externalProductId" : "313",
        "fund_name" : "ABSA SELECT EQUITY FUNDS",
        "fund_code" : "ABSAEQTY",
        "fund_factsheet" : "https://www.absainvestments.co.za/wealth-and-investment-management/e-docs/fund-fact-sheets/Absa%20Select%20Equity%20Fund.pdf",
        "fund_info" : "High risk fund for investors who are not risk cautious. This fund is suitable for investors who seek long-term capital growth from equity exposure",
        "fund_icon_url" : "https://image.ibb.co/b96EUa/Core.png",
        "symbol" : "ABSAEQTY",
        "cusip" : "008000AA7",
        "fund_type" : "HightRisk"
      }
    title: Response
    language: json
  - code_block: |2-
      {
        "error": true,
        "message": "Could not recommend any product"
      }
    title: Error
    language: json
---