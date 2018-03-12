---
title: /robo/recommend
position: 7.0
type: get
description: Return an investment product based on the user's risk tolerence 
parameters:
  - name: userId
    content: The user for the fund is recommend 
  - name: questionId
    content: The Id of the question
  - name: answerId
    content: The selected answer Id
content_markdown: |-
  This call will return an investment fund based on the user's risk tolerance 
  {: .info }
  Investment fund based on the user's risk tolerance
left_code_blocks:
  - code_block: |-
      $.get("http://api.kapitalwise.com/robo/recommend", { 
      "token": "YOUR_APP_KEY",
      "userId":123,
      "userResponses": [
      {
        "questionId": 1, 
        "answerId": 1
      },
      {
        "questionId": 2, 
        "answerId": 3
      }
      {
        "questionId": 3, 
        "answerId": 4
      }]
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
        "fundName" : "ABSA SELECT EQUITY FUNDS",
        "fundCode" : "ABSAEQTY",
        "fundFactsheet" : "https://www.absainvestments.co.za/wealth-and-investment-management/e-docs/fund-fact-sheets/Absa%20Select%20Equity%20Fund.pdf",
        "fundInfo" : "High risk fund for investors who are not risk cautious. This fund is suitable for investors who seek long-term capital growth from equity exposure",
        "fundIconUrl" : "https://image.ibb.co/b96EUa/Core.png",
        "symbol" : "ABSAEQTY",
        "cusip" : "008000AA7",
        "fundType" : "HighRisk"
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