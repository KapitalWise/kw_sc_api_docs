---
title: /users/:id
position: 1.4
type: put
description: Update User
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
    content: User's adress line two
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
  Update an existing user in the system.
left_code_blocks:
  - code_block: |-
      $.ajax({
        "url": "http://api.kapitalwise.com/users/3",
        "type": "PUT",
        "data": {
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
        "phone":"+19143184030"
      }
    title: Response
    language: json
  - code_block: |2-
      {
        "error": true,
        "message": "User doesn't exist"
      }
    title: Error
    language: json
---