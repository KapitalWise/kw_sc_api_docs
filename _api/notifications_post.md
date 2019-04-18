---
title: /notifications
position: 6.0
type: post
description: Send a notification request to APNs
parameters:
  - name: user
    content: User id
  - name: data
    content: Data object to be sent as notification {has two keys value pair, 'aps' (as per APNs spec) and 'payload' (Any extra info other than aps)}

left_code_blocks:
  - code_block: |-
      $.post("http://api.kapitalwise.com/notifications", {
      "user": "1",
      "data" : {
        "aps" : {
            "alert" : {
                "title" : "Game Request",
                "subtitle" : "Five Card Draw",
                "body" : "Bob wants to play poker"
            },
            "badge": 2
        },
        "payload": {
             "messageId": "ABWHEVDH"
        }
       }
      }, function(data) {
        alert(data);
      });
    title: jQuery
    language: javascript
right_code_blocks:
  - code_block: |-
      {
        "sent": [
          {"device": "7e976aa46427841e58af2d05a9da"}
        ],
        "failed": []
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
        "message": "User doesn\'t exist"
      }
      {
        "error": true,
        "message": "No device is linked to user"
      }
      {
        "error": true,
        "message": "Something went wrong on server-side"
      }
    title: Error
    language: json
---