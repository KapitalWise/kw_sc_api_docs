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
       [
        {
         "id": 1,
         "user": 1612,
         "product": {
            "id": 1,
            "name": "savings_account",
            "description": null
          },
         "rank": 2
        },
        {
         "id": 2,
         "user": 1612,
         "product": {
            "id": 5,
            "name": "payroll_account",
            "description": null
         },
         "rank": 1
        },
        {
         "id": 2,
         "user": 1612,
         "product": {
            "id": 15,
            "name": "tax_savings",
            "description": null
         },
         "rank": 3
        }
       ]

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
