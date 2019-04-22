---
title: /users
position: 1.0
type: get
description: List all users on the basis of filters passed
parameters:
  - name: offset
    content: Offset the results by this amount
  - name: limit
    content: Limit the number of users returned
  - name: filter (like email, passcode, city etc.)
    content: fields passed which acts as a filter to find user
content_markdown: |-
  This call will return a maximum of 100 users
  {: .info }

  Lists all the users in the system. You can paginate by using the parameters listed above.
left_code_blocks:
  - code_block: |-
      $.get("http://api.kapitalwise.com/users?email=1@gmail.com", { "token": "YOUR_APP_KEY"}, function(data) {
        alert(data);
      });
    title: jQuery
    language: javascript
  - code_block: |-
      r = requests.get("http://api.kapitalwise.com/users?email=1@gmail.com", token="YOUR_APP_KEY")
      print r.text
    title: Python
    language: python
  - code_block: |-
      var request = require("request");
      request("http://api.kapitalwise.com/users?email=1@gmail.com&&token=YOUR_APP_KEY", function (error, response, body) {
      if (!error && response.statusCode == 200) {
        console.log(body);
      }
    title: Node.js
    language: javascript
  - code_block: |-
      curl http://api.kapitalwise.com/users?email=1@gmail.com
    title: Curl
    language: bash
right_code_blocks:
  - code_block: |2-
      [
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
        "accounts": [1, 2, 3]]
        },
        { 
        "id": 4,
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
        "email": "john.cena@gmail.com",
        "subBackupWithld": "false",
        "phone":"+19143184030",
        "finWellScore": null,
        "goalSubscriptions":[{"id":2, "status": "ACTIVE"}],
        "accounts": [4, 5, 6]
        }
      ]
    title: Response
    language: json
  - code_block: |2-
      {
        "error": true,
        "message": "Invalid offset/limit"
      }
    title: Error
    language: json
---