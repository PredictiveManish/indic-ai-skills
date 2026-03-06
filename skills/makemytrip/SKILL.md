---
name: makemytrip
description: MakeMyTrip flight, hotel, and holiday booking integration. Search flights, compare prices, manage bookings.
metadata:
  author: ankitjh4
  category: Travel
  display-name: MakeMyTrip
---

# MakeMyTrip Integration

Search and book flights, hotels, and holidays via MakeMyTrip.

## Setup

1. Get API credentials: https://www.makemytrip.com/api/
2. Add to Zo secrets: `MMT_API_KEY`, `MMT_CLIENT_ID`

## Features

- Flight search & booking
- Hotel search & booking
- Holiday packages
- Fare alerts
- Booking management

## Usage

```bash
# Search flights
python3 scripts/makemytrip.py flights --from DEL --to BOM --date 2026-04-01

# Search hotels
python3 scripts/makemytrip.py hotels --city Goa --checkin 2026-04-01 --checkout 2026-04-05

# Get booking details
python3 scripts/makemytrip.py booking --id BOOK123
```

## API Docs

https://www.makemytrip.com/public/api-docs/
