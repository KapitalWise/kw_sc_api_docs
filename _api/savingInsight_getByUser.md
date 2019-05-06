---
title: /users/:id/savingInsights
position: 1.6
type: get
description: Saving insights for a user
parameters:
  - name: offset
    content: Offset the results by this amount
  - name: limit
    content: Limit the number of objects returned
content_markdown: |-
  Returns an array of timely (eg. weekly) savings made by the user
  {: .info}
left_code_blocks:
  - code_block: |-
      $.get("http://api.kapitalwise.com/users/123/savingInsights?offset=0&limit=10", {
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
        "user": 123,
        "amount": 225.00,
        "asOfDate": "2019-04-07T18:30:00.000Z"
        },
        {
        "id": 2,
        "user": 123,
        "amount": 736.00,
        "asOfDate": "2019-04-014T18:30:00.000Z"
        }
        ]

    title: Response
    language: json
  - code_block: |2-
      {
        "error": true,
        "message": "No saving insight found"
      }
      {
        "error": true,
        "message": "Necessary parameter(s) are missing"
      }
      {
        "error": true,
        "message": "Something went wrong on server-side"
      }
      {
        "error": true,
        "message": "User doesn\'t exist"
      }
    title: Error
    language: json
---
