---
title: /users/:id
position: 1.4
type: put
description: Update User
parameters:
  - name: dateOfBirth
    content: The title for the book
  - name: state
    content: The book's score between 0 and 5
  - name: lastName
    content: The title for the book
  - name: firstName
    content: The book's score between 0 and 5
  - name: address1
    content: The title for the book
  - name: address2
    content: The title for the book
  - name: city
    content: The title for the book
  - name: zip
    content: The book's score between 0 and 5 
  - name: email
    content: The book's score between 0 and 5 
  - name: phone
    content: The book's score between 0 and 5
  - name: ssn
    content: The book's score between 0 and 5
  - name: passcode
    content: The book's score between 0 and 5
  - name: password
    content: The book's score between 0 and 5
  - name: subBackupWithld
    content: The book's score between 0 and 5 
  - name: usResident
    content: The book's score between 0 and 5
  - name: brokerDealerAff
    content: The title for the book
  - name: boardMember
    content: The book's score between 0 and 5
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