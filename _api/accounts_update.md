---
title: /accounts/:id
position: 2.4
type: put
description: Update account
parameters:
  - name: userId
    content: The account owner. 
  - name: externalId
    content: The external id for the account. Yodlee, Plaid or bank's own id. 
  - name: accountName
    content: Account name
  - name: accountNumber
    content: The masked account number for display
  - name: nickname
    content: Account nick name
  - name: accountType
    content: Type of account. Checking, saving, credit etc.
  - name: providerType
    content: The account data provider. Yodlee, Plaid or banks 
  - name: loginName
    content: The login name if any
  - name: password
    content: The password if any
  - name: memo
    content: The memo
content_markdown: |-
  Update an existing account.
left_code_blocks:
  - code_block: |-
      $.ajax({
        "url": "http://api.myapp.com/accounts/3",
        "type": "PUT",
        "data": {
          "token": "YOUR_APP_KEY",
          "userId": 123,
          "externalId" :  "vzeNDwK7KQIm4yEog683uElbp9GRLEFXGK98D",
          "accountName":  "Chase Saving",
          "accountNumber": "XXXX4230",
          "nickname" : "My Chase Saving",
          "accountType":  "Saving",
          "loginName" :  "ydltestlogin",
          "password":  "ydltestpassw"
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
        "userId": 123,
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
        "message": "Necessary parameter(s) are missing"
      }
      {
        "error": true,
        "message": "Invalid user"
      }
    title: Error
    language: json
---