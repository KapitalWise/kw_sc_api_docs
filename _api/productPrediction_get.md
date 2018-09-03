---
title: /users/:id/products
position: 1.8
type: get
description: Recommends products to the user
parameters:
content_markdown: |-
  Returns a set of products users are likely to have in future
  {: .info}
left_code_blocks:
  - code_block: |-
      $.get("http://api.kapitalwise.com/users/123/products", {
        token: "YOUR_APP_KEY",
      }, function(data) {
        alert(data);
      });
    title: jQuery
    language: javascript
right_code_blocks:
  - code_block: |2-
        {
        "user": 201,
        "products": [
            {
            "id": 3,
            "rank": 3
            },
            {
            "id": 7,
            "rank": 1
            },
            {
            "id": 9,
            "rank": 2
            }]
        }

    title: Response
    language: json
  - code_block: |2-
      {
        "error": true,
        "message": "No product recommendations found"
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
