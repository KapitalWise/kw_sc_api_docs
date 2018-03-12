---
title: /robo/questions
position: 6.0
type: get
description: List all risk tolerance questions for the robo recommendation 
parameters:
  - name: offset
    content: Offset the results by this amount
  - name: limit
    content: Limit the number of accounts returned
content_markdown: |-
  This call will return a maximum of 100 accounts
  {: .info }

  Lists all the risk tolerence questions. You can paginate by using the parameters listed above.
left_code_blocks:
  - code_block: |-
      $.get("http://api.kapitalwise.com/robo/questions", { "token": "YOUR_APP_KEY"}, function(data) {
        alert(data);
      });
    title: jQuery
    language: javascript
  - code_block: |-
      r = requests.get("http://api.kapitalwise.com/robo/questions", token="YOUR_APP_KEY")
      print r.text
    title: Python
    language: python
  - code_block: |-
      var request = require("request");
      request("http://api.kapitalwise.com/robo/questions?token=YOUR_APP_KEY", function (error, response, body) {
      if (!error && response.statusCode == 200) {
        console.log(body);
      }
    title: Node.js
    language: javascript
  - code_block: |-
      curl http://api.kapitalwise.com/robo/questions?key=YOUR_APP_KEY
    title: Curl
    language: bash
right_code_blocks:
  - code_block: |2-
       [
          {
          "id": 1,
          "type": "RADIO",
          "category" : "RISK_TOLERANCE",
          "sno": 1,
          "text": "Compared to others, how do you rate your willingness to take financial risks?",
          "choices": [
            {
            "id": 1,
            "choice": "Extremely Low",
            "sno": 1
            },
            {
            "id": 2,
            "choice": "Very Low",
            "sno": 2
            },
            {
            "id": 3,
            "choice": "Low",
            "sno": 3
            },
            {
            "id": 4,
            "choice": "Average",
            "sno": 4
            }
          ]
          },
          {
            "id": 2,
            "type": "RADIO",
            "category": "TIME_HORIZON",
            "sno": 1,
            "text": "How easily do you adapt when things go wrong financially?",
            "choices": [
              {
                "id": 1,
                "choice": "Very difficult",
                "score" : 1,
                "sno": 1
              },
              {
                "id": 2,
                "choice": "Reasonably difficult",
                "score" : 4,
                "sno": 2
              },
              {
                "id": 3,
                "choice": "Reasonably well",
                "score" : 5,
                "sno": 3
              },
              {
                "id": 4,
                "choice": "No problem",
                "score" : 8,
                "sno": 4
              }
            ]
          }
          }
       ]
    title: Response
    language: json
  - code_block: |2-
      {
        "error": true,
        "message": "Invalid offset/limit"
      }
    title: Error
    language: json
---