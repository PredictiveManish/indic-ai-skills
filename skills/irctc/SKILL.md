---
name: irctc
description: Indian Railways train search, PNR status, live train status, and station search using RailwayAPI.com. Free tier available at railwayapi.com
metadata:
  author: ankitjh4.zo.computer
  category: Indian Services
---

# Indian Railways (IRCTC/RailwayAPI)

Train search, PNR status, and live train tracking for Indian Railways.

## Required API Key

Get a free API key from **RailwayAPI.com**:
1. Go to https://railwayapi.com/
2. Sign up for free account
3. Get your API key
4. Add to Zo secrets: `RAILWAYAPI_KEY`

## Features

### 1. PNR Status
Check booking confirmation status:
```bash
python3 scripts/irctc.py pnr 1234567890
```

### 2. Train Search
Find trains between stations:
```bash
python3 scripts/irctc.py trains NDLS ADI --date 2026-03-15
```

### 3. Live Train Status
Track running trains:
```bash
python3 scripts/irctc.py live 12002
```

### 4. Station Search
Find station codes:
```bash
python3 scripts/irctc.py station Delhi
```

### 5. Seat Availability
Check seat availability:
```bash
python3 scripts/irctc.py availability 12002 NDLS AII 2026-03-15 SL
```

## API Endpoints Used

- PNR Status: `https://railwayapi.com/api/v2/pnr-status/pnr/{pnr}/apikey/{api_key}/`
- Trains Between: `https://railwayapi.com/api/v2/trains-between-stations/source/{from}/destination/{to}/date/{date}/apikey/{api_key}/`
- Live Status: `https://railwayapi.com/api/v2/live-train-status/train/{train}/date/{date}/apikey/{api_key}/`
- Station Search: `https://railwayapi.com/api/v1/stations/name/{station}/apikey/{api_key}/`

## Notes

- Free tier: 1000 calls/day
- Commercial: Starts at ₹499/month
- Alternative: IRCTC authorized partner API (paid)
