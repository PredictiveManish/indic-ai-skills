---
name: irctc
description: IRCTC train ticket booking and PNR status checking. Search trains, check availability, book tickets.
metadata:
  author: ankitjh4
  category: Travel
  display-name: IRCTC Train Booking
---

# IRCTC Integration

Book train tickets and check PNR status via IRCTC.

## Setup

1. Get API credentials: https://irctc.co.in
2. Add to Zo secrets: `IRCTC_USERNAME`, `IRCTC_PASSWORD`, `IRCTC_API_KEY`

## Features

- Search trains between stations
- Check seat availability
- Book tickets
- Check PNR status
- Get train schedule
- Live train status

## Usage

```bash
# Search trains
python3 scripts/irctc.py trains --from NDLS --to BSB --date 2026-04-01

# Check PNR
python3 scripts/irctc.py pnr-status --pnr 1234567890

# Check availability
python3/scripts/irctc.py availability --train 12560 --date 2026-04-01 --class 3A
```

## API Docs

https://www.irctc.co.in/eticketing/
