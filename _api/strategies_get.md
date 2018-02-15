---
title: /strategies/:id
position: 3.3
type: get
description: Get User
parameters:
  - name:
    content:
content_markdown: |-
  Returns a specific strategy from the system
left_code_blocks:
  - code_block: |-
      $.get("http://api.kapitalwise.com/strategies/123", {
        token: "YOUR_APP_KEY",
      }, function(data) {
        alert(data);
      });
    title: jQuery
    language: javascript
right_code_blocks:
  - code_block: |2-
       {
        userId: 123,
        accountIds: ["vzeNDwK7KQIm4yEog683uElbp9GRLEFXGK98D", "vzeNDwK7KQIm4yEog683uElbp9GRLEFED45RT"],
        investmentIds : [234,345],
        strategyType: 'ANALYZE_INVEST',
        params: [{ key: "max_amount", value:"500.00" }],
        fundIds: [124,156],
        status: "ACTIVE"
      }
    title: Response
    language: json
  - code_block: |2-
      {
        "error": true,
        "message": "Requested strategy not found"
      }
    title: Error
    language: json
---
