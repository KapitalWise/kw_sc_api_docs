---
title: /users/digit
position: 1.0
type: post
description: Link user to Digit Platform
parameters:
  - name: firstName
    content: User's first name
  - name: lastName
    content: User's last name
  - name: email
    content: User's email
  - name: passcode
    content: Digit passcode 
  - name: password
    content: Password
content_markdown: |-
  The user will automatically be added and enabled
  {: .success}

  Adds a user to your collection.
left_code_blocks:
  - code_block: |-
      $.post("http://api.kapitalwise.com/users/digit", {
        "token": "YOUR_APP_KEY",
        "firstName": "John",
        "lastName": "Doe",
        "email": "john.doe@gmail.com",
        "passcode": "72537252",
        "password": "pass123"
      }, function(data) {
        alert(data);
      });
    title: jQuery
    language: javascript
right_code_blocks:
  - code_block: |-
      { 
        "id": 3,
        "dateOfBirth": "05/28/1988",
        "state": "NY",
        "lastName": "John",
        "firstName": "Doe",
        "address1": "43",
        "zip": "10010",
        "address2": "W 23rd Street",
        "usResident": "true",
        "city": "New York",
        "brokerDealerAff": "false",
        "boardMember": "false",
        "email": "john.doe@gmail.com",
        "subBackupWithld": "false",
        "phone":"+19143184030",
        "finWellScore": null,
        "goalSubscriptions":[{"id":1, "status": "ACTIVE"}],
        "accounts": [1, 2, 3]
      }
    title: Response
    language: json
  - code_block: |-
      {
        "error": true,
        "message": "User with this email already exists"
      }
      {
        "error": true,
        "message": "Known error"
      }
      {
        "error": true,
        "message": "Invalid password"
      }
      {
        "error": true,
        "message": "Invalid passcode"
      }
    title: Error
    language: json
---


