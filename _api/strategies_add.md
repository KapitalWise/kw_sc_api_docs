---
title: /strategies
position: 3.1
type: post
description: Create investment strategy
parameters:
  - name: userId
    content: The user for the strategy is created for
  - name: accountIds
    content: String Array of account Id's
  - name: strategyType
    content: string (enum 'ANALYZE_INVEST', 'ROUNDUP', 'INVEST_WHEN_PAID', 'INVEST_WHEN_SPEND', 'SCHEDULED', 'ONE_TIME')
  - name: params
    content: Config params arrays

content_markdown: |-
  Add a strategy for the user with a set of accounts
  {: .success}

  Adds a book to your collection.
left_code_blocks:
  - code_block: |-
      $.post("http://api.kapitalwise.com/strategies/", {
      "token": "YOUR_APP_KEY",
      "userId": 123,
      "accountIds": ["vzeNDwK7KQIm4yEog683uElbp9GRLEFXGK98D", "vzeNDwK7KQIm4yEog683uElbp9GRLEFED45RT"],
      "strategyType": "ANALYZE_INVEST",
      "params": [{ key: "max_amount", value:"500.00" }],
      "fundIds": [124,156]
      }, function(data) {
        alert(data);
      });
    title: jQuery
    language: javascript
right_code_blocks:
  - code_block: |-
      {
      userId: 123,
      accountIds: ["vzeNDwK7KQIm4yEog683uElbp9GRLEFXGK98D", "vzeNDwK7KQIm4yEog683uElbp9GRLEFED45RT"],
      strategyType: "ANALYZE_INVEST",
      params: [{ key: "max_amount", value:"500.00" }],
      fundIds: [124,156],
      status: "ACTIVE"
      }
    title: Response
    language: json
  - code_block: |-
      {
        "error": true,
        "message": "Necessary parameter(s) are missing"
      }
      {
        "error": true,
        "message": "Invalid strategyType value"
      }
    title: Error
    language: json
---
