---
title: /users/email
position: 1.5
type: get
description: Get User
parameters:
  - name: email
    content: email of the user
left_code_blocks:
  - code_block: |-
      $.get("http://api.kapitalwise.com/users/3", {
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
  - code_block: |2-
      {
        "error": true,
        "message": "User doesn't exist"
      }
    title: Error
    language: json
---