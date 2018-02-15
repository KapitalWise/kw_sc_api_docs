---
title: /strategies/:id
position: 3.4
type: put
description: Update Book
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
  Update an existing strategy in the system.
left_code_blocks:
  - code_block: |-
      $.ajax({
        "url": "http://api.kapitalwise.com/strategies/3",
        "type": "PUT",
        "data": {
          "token": "YOUR_APP_KEY",
          "userId": 123,
          "accountIds": ["vzeNDwK7KQIm4yEog683uElbp9GRLEFXGK98D", "vzeNDwK7KQIm4yEog683uElbp9GRLEFED45RT"],
          "strategyType": 'ANALYZE_INVEST',
          "params": [{ key: "max_amount", value:"500.00" }],
          "status": "ACTIVE"
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
          "token": "YOUR_APP_KEY",
          "userId": 123,
          "accountIds": ["vzeNDwK7KQIm4yEog683uElbp9GRLEFXGK98D", "vzeNDwK7KQIm4yEog683uElbp9GRLEFED45RT"],
          "strategyType": "ANALYZE_INVEST",
          "params": [{ key: "max_amount", value:"500.00" }],
          "fundIds": [124,156],
          "status": "ACTIVE"
      }
    title: Response
    language: json
  - code_block: |2-
      {
        "error": true,
        "message": "Necessary parameter(s) are missing"
      }
      {
        "error": true,
        "message": "Invalid strategyType value"
      }
      {
        "error": true,
        "message": "Invalid strategy"
      }
    title: Error
    language: json
---