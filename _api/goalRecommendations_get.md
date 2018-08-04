---
title: /goalSuggestions
position: 4.1
type: get
description: Recommend goals for a user
parameters:
  - name: user
    content: User for which the recommendation is to be made
content_markdown: |-
  Returns a set of goal recommendations for the user
  {: .info}
left_code_blocks:
  - code_block: |-
      $.get("http://api.kapitalwise.com/goalSuggestions", {
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
            "goal": {
            	  "id": 10,
                "name": "Pay credit card bill",
                "description": null,
                "iconUrl": null
                },
            "user": 1,
            "target": 100
        },
        {
            "id": 2,
            "goal": {
            	  "id": 17,
                "name": "Pay house loan",
                "description": null,
                "iconUrl": null
            },
            "user": 1,
            "target": 500
        }]
    title: Response
    language: json
  - code_block: |2-
      {
        "error": true,
        "message": "Could not recommend any goal"
      }
    title: Error
    language: json
---
