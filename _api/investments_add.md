---
title: /investments
position: 4.1
type: post
description: Create Investment, called after the investment is settled with the broker dealer
parameters:
  - name: subscriptionId
    content: The subscriptionId, this will be passed to you in the ledger
  - name: fundHoldingId
    content: The fund holding ID
  - name: amount
    content: Amount invested
  - name: unitPrice
    content: Fund unit price 

content_markdown: |-
  The book will automatically be added to your reading list
  {: .success}

  Adds a book to your collection.
left_code_blocks:
  - code_block: |-
      $.post("http://api.kapitalwise.com/investments/", {
        "token": "YOUR_APP_KEY",
        "subscriptionId" : 123,
        "investmentDetails" : [
          {
            "fundHoldingId" : 1,
            "amount" : 345.00,
            "unitPrice" : 23.00
          },
          {
            "fundHoldingId" : 2,
            "amount" : 245.00,
            "unitPrice" : 34.00
          },
          {
            "fundHoldingId" : 3,
            "amount" : 350.00,
            "unitPrice" : 34.00
          }
        ],
        "date" :  "2017-11-19 17:46:48"
      }, function(data) {
        alert(data);
      });
    title: jQuery
    language: javascript
right_code_blocks:
  - code_block: |-
      {
        "id" : 234,
        "subscriptionId" : 123,
        "investmentDetails" : [
          {
            "fundHoldingId" : 1,
            "amount" : 345.00,
            "unitPrice" : 23.00
          },
          {
            "fundHoldingId" : 2,
            "amount" : 245.00,
            "unitPrice" : 34.00
          },
          {
            "fundHoldingId" : 3,
            "amount" : 350.00,
            "unitPrice" : 34.00
          }
        ],
        "date" :  "2017-11-19 17:46:48"
      }
      }
    title: Response
    language: json
  - code_block: |-
      {
        "error": true,
        "message": "Invalid parameter"
      }
    title: Error
    language: json
---
