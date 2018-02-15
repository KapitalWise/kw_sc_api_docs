---
title: /accounts
position: 2.0
type: get
description: List all books
parameters:
  - name: offset
    content: Offset the results by this amount
  - name: limit
    content: Limit the number of accounts returned
content_markdown: |-
  This call will return a maximum of 100 accounts
  {: .info }

  Lists all the photos you have access to. You can paginate by using the parameters listed above.
left_code_blocks:
  - code_block: |-
      $.get("http://api.kapitalwise.com/accounts/", { "token": "YOUR_APP_KEY"}, function(data) {
        alert(data);
      });
    title: jQuery
    language: javascript
  - code_block: |-
      r = requests.get("http://api.kapitalwise.com/accounts/", token="YOUR_APP_KEY")
      print r.text
    title: Python
    language: python
  - code_block: |-
      var request = require("request");
      request("http://api.kapitalwise.com/accounts?token=YOUR_APP_KEY", function (error, response, body) {
      if (!error && response.statusCode == 200) {
        console.log(body);
      }
    title: Node.js
    language: javascript
  - code_block: |-
      curl http://api.kapitalwise.com/accounts?key=YOUR_APP_KEY
    title: Curl
    language: bash
right_code_blocks:
  - code_block: |2-
      [
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
      },
      {
        "id": 4,
        "userId": 1224,
        "externalId" :  "vzeNDwK7KQIm4yEog683uElbp9GASWDCF3DD",
        "accountName":  "Chase Checking",
        "accountNumber": "XXXX4223",
        "nickname" : "My Chase Checking",
        "accountType":  "Checking",
        "providerType":  "YODLEE",
        "loginName" :  "ydltestlogin",
        "password":  "ydltestpassword",
        "memo":  "Test memo"
      },
      ]
    title: Response
    language: json
  - code_block: |2-
      {
        "error": true,
        "message": "Invalid offset"
      }
    title: Error
    language: json
---