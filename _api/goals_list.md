---
title: /goals
position: 3.1
type: get
description: List all Goals
parameters:
  - name: offset
    content: Offset the results by this amount
  - name: limit
    content: Limit the number of goals returned
content_markdown: |-
  This call will return a maximum of 100 goals.
  {: .info}
  Lists all the goals in the system. You can paginate by using the parameters listed above.
left_code_blocks:
  - code_block: |-
      $.get("http://api.kapitalwise.com/goals", {
        token: "YOUR_APP_KEY",
      }, function(data) {
        alert(data);
      });
    title: jQuery
    language: javascript
right_code_blocks:
  - code_block: |2-
      [
        {
        "id": 1,
        "name": "Emergency Savings",
        "description": "Your recommended Emergency Savings is intended to help you prepare for unexpected expenses. Depending on the assets you've, we recommend having between 3-6 months of your annual household income set aside for emergencies",
        "iconUrl": null,
        "status": "ACTIVE"
        },
        {
        "id": 2,
        "name": "Paydown Credit Card Balance",
        "description": "Credit card debt can put a serious drag on your net worth. If you have high interest credit card debt or several different credit card bills to pay every month, it can make a lot of sense to take advantage of a 0% APR balance transfer offer as well.",
        "iconUrl": null,
        "status": "ACTIVE"
        }
      ]
    title: Response
    language: json
  - code_block: |2-
      {
        "error": true,
        "message": "Necessary parameter(s) are missing"
      }
      {
        "error": true,
        "message": "Invalid offset/limit"
      }
      {
        "error": true,
        "message": "Goal doesn't exist"
      }
    title: Error
    language: json
---
