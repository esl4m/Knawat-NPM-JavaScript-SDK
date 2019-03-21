<p align="center"><a href="https://knawat.com/"><img src="https://knawat.com/wp-content/uploads/2017/10/253_77.png" alt="Knawat"></a></p>

[![Join the chat at https://gitter.im/Knawat/Lobby](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/Knawat/Lobby)

# Knawat Node.js NPM Package

A Node.js package for Knawat Dropshipping MP REST API. Easily interact with the Knawat MP REST API using this library.

## Installation

```
npm install --save knawat/mp
```

## Getting started

Check out the Knawat Dropshipping MP REST API endpoints and data that can be manipulated in <https://mp.knawat.io/>.

## Setup

Setup for the new Knawat Dropshipping REST API integration:

```javascript
const MP = require('knawat/mp');

const mp = new MP({
  consumer_key: 'XXXXXXXXXXXXXXXXXXXXXXXXXXX',
  consumer_secret: 'XXXXXXXXXXXXXXXXXXXXXXXX'
});
```

### Options

| Option            | Type     | Required | Description                      |
| ----------------- | -------- | -------- | -------------------------------- |
| `consumer_key`    | `string` | yes      | Your Store's API consumer key    |
| `consumer_secret` | `string` | yes      | Your Store's API consumer secret |

# Methods

## Product Methods

### getProducts (GET Products)

```javascript
mp.getProducts(limit, page, lastupdate);
```

| Params       | Type        | Description                                                                                |
| ------------ | ----------- | ------------------------------------------------------------------------------------------ |
| `limit`      | `Integer`   | Number of products to retrieve. `Default: 10`                                              |
| `page`       | `Integer`   | Number of the page to retrieve. `Default: 1`                                               |
| `lastupdate` | `Timestamp` | Optional. UTC Timestamp of last import. for get only updated products after this Timestamp |

### getProductBySku

```javascript
mp.getProductBySku(sku);
```

| Params | Type     | Description                    |
| ------ | -------- | ------------------------------ |
| `sku`  | `string` | SKU of Product you want to get |

### getProductCount

```javascript
mp.getProductCount();
```

## Order Methods

### getOrders (GET Orders)

```javascript
mp.getOrders(limit, page);
```

| Params  | Type      | Description                                  |
| ------- | --------- | -------------------------------------------- |
| `limit` | `Integer` | Number of orders to retrieve. `Default: 1`   |
| `page`  | `Integer` | Number of the page to retrieve. `Default: 1` |

### getOrderById (GET Order By Knawat Order Id)

```javascript
mp.getOrderById(order_id);
```

| Params     | Type     | Description     |
| ---------- | -------- | --------------- |
| `order_id` | `string` | Knawat Order ID |

### createOrder (Create Order)

```javascript
mp.createOrder(order_data);
```

| Params       | Type     | Description                          |
| ------------ | -------- | ------------------------------------ |
| `order_data` | `object` | Array of Order Data for create order |

### updateOrder (Update Order)

```javascript
mp.updateOrder(order_id, order_data);
```

| Params       | Type     | Description                                  |
| ------------ | -------- | -------------------------------------------- |
| `order_id`   | `string` | Knawat Order ID                              |
| `order_data` | `object` | Array of Updated Order Data for create order |

## REST Methods

| Params     | Type     | Description                                                                  |
| ---------- | -------- | ---------------------------------------------------------------------------- |
| `endpoint` | `string` | WooCommerce API endpoint, example: `catalog/products` or `orders/{order_id}` |
| `data`     | `array`  | Only for POST and PUT, data that will be converted to JSON                   |

### GET

```javascript
mp.get(endpoint);
```

### POST

```javascript
mp.post(endpoint, data);
```

### PUT

```javascript
mp.put(endpoint, data);
```

### DELETE

```javascript
mp.delete(endpoint);
```

## Reporting Security Issues

To disclose a security issue to our team, [please submit a report here](https://knawat.com/contact/).

## Support & Chat

Developers are welcome here, please create issue or [chat with us https://gitter.im/Knawat/Lobby](https://gitter.im/Knawat/Lobby). This repository is not suitable for Knawat customers support. Please don't use our issue tracker for support requests, but for Knawat Dropshipping NPM Package issues only. Support can take place through [Knawat support portal](https://help.knawat.com/hc/en-us/requests/new/) which is available for free.

Support requests in issues on this repository will be closed on sight.

## Contributing to Knawat

If you have a patch or have stumbled upon an issue with Knawat NPM Package, you can contribute this back to the code. Please create a pull request.

## Check also

- [Knawat RESTful API](https://mp.knawat.io)
- [Knawat PHP SDK](https://github.com/Knawat/Knawat-PHP-SDK)
- [WooCommerce Dropshipping Plugin](https://github.com/Knawat/dropshipping-woocommerce)
- [Magento 2 Module](https://github.com/Knawat/knawat-dropshipping-magento2)
- [OpenCart Module](https://github.com/Knawat/knawat-dropshipping-opencart)
