---
title: /users
position: 1.0
type: get
description: List all users
parameters:
  - name: offset
    content: Offset the results by this amount
  - name: limit
    content: Limit the number of users returned
content_markdown: |-
  This call will return a maximum of 100 users
  {: .info }

  Lists all the users in the system. You can paginate by using the parameters listed above.
left_code_blocks:
  - code_block: |-
      $.get("http://api.kapitalwise.com/users/", { "token": "YOUR_APP_KEY"}, function(data) {
        alert(data);
      });
    title: jQuery
    language: javascript
  - code_block: |-
      r = requests.get("http://api.kapitalwise.com/users/", token="YOUR_APP_KEY")
      print r.text
    title: Python
    language: python
  - code_block: |-
      var request = require("request");
      request("http://api.kapitalwise.com/users?token=YOUR_APP_KEY", function (error, response, body) {
      if (!error && response.statusCode == 200) {
        console.log(body);
      }
    title: Node.js
    language: javascript
  - code_block: |-
      curl http://sampleapi.readme.com/orders?key=YOUR_APP_KEY
    title: Curl
    language: bash
right_code_blocks:
  - code_block: |2-
      [
        { 
        "id": 1,
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
        "goalSubscriptions":[124,156]
        },
        { 
        "id": 2,
        "dateOfBirth": "07/18/1982",
        "state": "NY",
        "lastName": "Elizabeth",
        "firstName": "Hibbett ",
        "address1": "65",
        "zip": "10010",
        "address2": "James Street",
        "usResident": "true",
        "city": "Yonkers",
        "brokerDealerAff": "false",
        "boardMember": "false",
        "email": "elizabeth.hibbet@gmail.com",
        "subBackupWithld": "false",
        "phone":"+12019367778",
        "goalSubscriptions":[423,345]
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