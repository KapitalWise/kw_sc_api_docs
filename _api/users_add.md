---
title: /users
position: 1.1
type: post
description: Create User
parameters:
  - name: dateOfBirth
    content: User's date of birth
  - name: firstName
    content: User's first name
  - name: lastName
    content: User's last name
  - name: address1
    content: User's address line one
  - name: address2
    content: User's address line two
  - name: state
    content: User's state
  - name: city
    content: User's city
  - name: zip
    content: User's zip
  - name: email
    content: User's email
  - name: phone
    content: User's phone
  - name: ssn
    content: User's social security number
  - name: passcode
    content: Four digit passcode 
  - name: password
    content: Password
  - name: subBackupWithld
    content: Is this user subjected to backup withholding 
  - name: usResident
    content: Is this user US resident
  - name: brokerDealerAff
    content: Is this user affiliated to any broker dealer
  - name: boardMember
    content: Is this user board member of a public listed company

content_markdown: |-
  The user will automatically be added and enabled
  {: .success}

  Adds a user to your collection.
left_code_blocks:
  - code_block: |-
      $.post("http://api.kapitalwise.com/users/", {
        "token": "YOUR_APP_KEY",
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
        "ssn": "152225201",
        "passcode": "3100",
        "password": "kap1talw1se"
      }, function(data) {
        alert(data);
      });
    title: jQuery
    language: javascript
right_code_blocks:
  - code_block: |-
      { 
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
        "phone":"+19143184030"
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


