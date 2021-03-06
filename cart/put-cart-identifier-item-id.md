<!--
@title Update item in a cart
@author Moltin Ltd
@description Updates a cart item by identifier
@order 4.2

@sidebar 1
@family Cart
@rate No
@auth Yes
@format JSON
@http PUT
@version beta
-->

You can update an item in the cart by sending a PUT request to the item's endpoint with a list of parameters.


#### Resource URL
PUT [{{ url }}cart/:identifier/item/:id]({{ url }}cart/:identifier/item/:id])

#### Paramaters
Key | Type | Description
--- | ---- | -----------
name*optional* | String | The new name of this item
quantity*optional* | Integer | A new quantity for this item
price*optional* | Float | The new price of this item
weight*optional* | Float | The new weight of this item
height*optional* | Float | The new height of this item
width*optional* | Float | The new width of this item
depth*optional* | Float | The new depth of this item

<!--code-->
#### Example Successful Response
``` json
{
  "status": true,
  "item": {
    "id": "14",
    "quantity": "100",
    "/beta/cart/123": "",
    "sku": "PRD_H0001",
    "title": "Choc Fondue Pot",
    "slug": "choc-fondue-pot",
    "price": "17.99",
    "sale_price": "14.99",
    "status": {
      "key": "1",
      "value": "Live"
    },
    "category": {
      "id": "60",
      "parent": null,
      "title": "Featured",
      "slug": "featured",
      "status": {
        "key": "1",
        "value": "Live"
      },
      "description": "Featured products"
    },
    "stock_level": 8892,
    "stock_status": {
      "key": "1",
      "value": "In Stock"
    },
    "description": "Make your favorite sweets extra special with a coating of freshly melted Chocolate! This chocolate Fondue set makes dessert a fun shared experience, perfect for a romantic meal or for celebrations with friends and family. Always a great gift idea for the chocoholic in your life!",
    "requires_shipping": {
      "key": "1",
      "value": "Yes"
    },
    "weight": "234.00",
    "height": "24.00",
    "width": "24.00",
    "depth": "32.00",
    "tax_band": {
      "id": 1,
      "title": "Default",
      "description": null,
      "rate": "20.00"
    },
    "pricing": {
      "formatted": {
        "with_tax": "£22.00",
        "without_tax": "£18.33"
      },
      "rounded": {
        "with_tax": 22,
        "without_tax": 18.33
      },
      "raw": {
        "with_tax": 21.588,
        "without_tax": 17.99
      }
    },
    "images": {
      "60": {
        "id": 60,
        "name": "fonduepot1.jpg",
        "url": {
          "http": "http://d2xufakadxl3ok.cloudfront.net/1/fonduepot1.jpg",
          "https": "https://d2xufakadxl3ok.cloudfront.net/1/fonduepot1.jpg"
        }
      },
      "61": {
        "id": 61,
        "name": "fonduepot2.jpg",
        "url": {
          "http": "http://d2xufakadxl3ok.cloudfront.net/1/fonduepot2.jpg",
          "https": "https://d2xufakadxl3ok.cloudfront.net/1/fonduepot2.jpg"
        }
      },
      "62": {
        "id": 62,
        "name": "fonduepot3.jpg",
        "url": {
          "http": "http://d2xufakadxl3ok.cloudfront.net/1/fonduepot3.jpg",
          "https": "https://d2xufakadxl3ok.cloudfront.net/1/fonduepot3.jpg"
        }
      }
    },
    "name": "Choc Fondue Pot",
    "tax": "20.00",
    "/beta/cart/123/item/bb4a6db4295d6be8bd12791ed5650087": "",
    "total": 2158.8,
    "total_before_tax": 1799,
    "totals": {
      "formatted": {
        "with_tax": "£2,200.00",
        "without_tax": "£1,833.00"
      },
      "rounded": {
        "with_tax": 2200,
        "without_tax": 1833
      },
      "raw": {
        "with_tax": 2158.8,
        "without_tax": 1799
      }
    }
  }
}
```

#### Example Failed Response
``` json
{
  "status": false,
  "error": "Quantity can not be less than 1"
}
```
<!--/code-->