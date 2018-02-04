---
title: Authentication
position: 2
parameters:
  - name:
    content:
content_markdown: |-
  You need to be authenticated for all API requests. You can request an API key by contacting us <a target='_blank' href="http://kapitalwise.com/contact.php">here</a>.

  Add the API key to all requests as a GET parameter.

  Nothing will work unless you include this API key
  {: .error}
left_code_blocks:
  - code_block:
    title:
    language:
right_code_blocks:
  - code_block: |2-
       $.get("http://api.kapitalwise.com/users/", { "token": "YOUR_APP_KEY"}, function(data) {
         alert(data);
       });
    title: JQuery
    language: javascript
  - code_block: |2-
       curl http://api.kapitalwise.com/books?token=YOUR_APP_KEY
    title: Curl
    language: bash
---