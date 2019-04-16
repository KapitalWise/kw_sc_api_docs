---
title: /users/:id/device
position: 1.6
type: post
description: Adds a device to user
parameters:
  - name: make
    content: device's make
  - name: model
    content: device's model
  - name: token
    content: device token
content_markdown: |-
  The device will be added
  {: .success}

  Adds a device to user
left_code_blocks:
  - code_block: |-
      $.post("http://api.kapitalwise.com/users/1/device", {
        "token": "YOUR_APP_KEY",
        "make": "a",
        "model": "b",
        "token": "vr73afsjw8bjsbvjashfasfa"
      }, function(data) {
        alert(data);
      });
    title: jQuery
    language: javascript
right_code_blocks:
  - code_block: |-
      { 
        "id": 3,
        "user": 1,
        "make": "a",
        "model": "b",
        "token": "vr73afsjw8bjsbvjashfasfa"
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
        "message": "User doesn't exist"
      }
      {
        "error": true,
        "message": "Something went wrong on server-side"
      }
    title: Error
    language: json
---


