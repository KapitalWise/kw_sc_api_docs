---
title: /accounts/:id
position: 2.3
type: get
description: Get User
parameters:
  - name:
    content:
content_markdown: |-
  Returns a specific book from your collection
left_code_blocks:
  - code_block: |-
      $.get("http://api.kapitalwise.com/accounts/5", {
        token: "YOUR_APP_KEY",
      }, function(data) {
        alert(data);
      });
    title: jQuery
    language: javascript
right_code_blocks:
  - code_block: |2-
      {
        "id": 3,
        "userId": 1223,
        "externalId" :  "vzeNDwK7KQIm4yEog683uElbp9GRLEFXGK98D",
        "accountName":  "Chase Saving",
        "accountNumber": "XXXX4230",
        "nickname" : "My Chase Saving",
        "accountType":  "Saving",
        "providerType":  "YODLEE",
        "loginName" :  "ydltestlogin",
        "password":  "ydltestpassword",
        "memo":  "Test memo"
      }
    title: Response
    language: json
  - code_block: |2-
      {
        "error": true,
        "message": "Necessary query parameter(s) are missing"
      }
      {
        "error": true,
        "message": "Requested account not found"
      }
    title: Error
    language: json
---