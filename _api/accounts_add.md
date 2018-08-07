---
title: /accounts
position: 2.1
type: post
description: Create User
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
  - name: accountSubType
    content: Sub type of account (Funding/None)
  - name: providerType
    content: The account data provider. Yodlee, Plaid or banks 
  - name: loginName
    content: The login name if any
  - name: password
    content: The password if any
  - name: memo
    content: The memo

content_markdown: |-
  The account will automatically be added to the user
  {: .success}

left_code_blocks:
  - code_block: |-
      $.post("http://api.kapitalwise.com/accounts/", {
        "token": "YOUR_APP_KEY",
        "userId": 123,
        "externalId" :  "vzeNDwK7KQIm4yEog683uElbp9GRLEFXGK98D",
        "accountName":  "Chase Saving",
        "accountNumber": "XXXX4230",
        "nickname" : "My Chase Saving",
        "accountType":  "Saving",
        "accountSubType":  "FUNDING",
        "providerType":  "YODLEE",
        "loginName" :  "ydltestlogin",
        "password":  "ydltestpassw",
        "memo": "chase account"
      }, function(data) {
        alert(data);
      });
    title: jQuery
    language: javascript
right_code_blocks:
  - code_block: |-
      {
        "userId": 123,
        "externalId" :  "vzeNDwK7KQIm4yEog683uElbp9GRLEFXGK98D",
        "accountName":  "Chase Saving",
        "accountNumber": "XXXX4230",
        "nickname" : "My Chase Saving",
        "accountType":  "Saving",
        "accountSubType":  "FUNDING",
        "providerType":  "YODLEE",
        "loginName" :  "ydltestlogin",
        "password":  "ydltestpassword",
        "memo":  "Test memo"
      }
    title: Response
    language: json
  - code_block: |-
      {
        "error": true,
        "message": "Necessary parameter(s) are missing"
      }
      {
        "error": true,
        "message": "Invalid user"
      }
      {
        "error": true,
        "message": "Invalid Provider"
      }
      {
        "error": true,
        "message": "Invalid score"
      }
    title: Error
    language: json
---

