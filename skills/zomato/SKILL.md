---
name: zomato
description: Zomato food delivery API integration. Search restaurants, get menus, place orders, and manage deliveries.
metadata:
  author: ankitjh4
  category: Food
  display-name: Zomato Food Delivery
---

# Zomato Integration

Access Zomato's food delivery and restaurant data.

## Setup

1. Get API key: https://developers.zomato.com/api
2. Add to Zo secrets: `ZOMATO_API_KEY`

## Features

- Restaurant search by location, cuisine, rating
- Menu fetching
- Order management
- Delivery tracking

## Usage

```bash
# Search restaurants
python3 scripts/zomato.py search --city Delhi --cuisine Chinese

# Get restaurant details
python3 scripts/zomato.py restaurant --id 123456

# Get menu
python3 scripts/zomato.py menu --restaurant-id 123456
```

## API Docs

https://developers.zomato.com/api
