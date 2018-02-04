---
title: /users
position: 1.1
type: post
description: Create User
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
  The book will automatically be added to your reading list
  {: .success}

  Adds a book to your collection.
left_code_blocks:
  - code_block: |-
      $.post("http://api.kapitalwise.com/books/", {
        "token": "YOUR_APP_KEY",
        "title": "The Book Thief",
        "score": 4.3
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
        "phone":"+19143184030",
        "ssn": "152225201",
        "passcode": "3100",
        "password": "kap1talw1se"
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


