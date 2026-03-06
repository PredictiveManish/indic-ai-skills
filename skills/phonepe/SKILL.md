---
name: phonepe
description: PhonePe UPI payment integration. Send/receive money, check balance, bill payments.
metadata:
  author: ankitjh4
  category: Payments
  display-name: PhonePe UPI
---

# PhonePe Integration

Access PhonePe's UPI and payment services.

## Setup

1. Get Merchant ID: https://business.phonepe.com/
2. Add to Zo secrets: `PHONEPE_MERCHANT_ID`, `PHONEPE_SALT_KEY`, `PHONEPE_SALT_INDEX`

## Features

- UPI payments (send/receive)
- Check account balance
- Bill payments
- Transaction history
- Mobile recharge

## Usage

```bash
# Check balance
python3 scripts/phonepe.py balance

# Send UPI payment
python3 scripts/phonepe.py pay --upi-id user@upi --amount 500

# Transaction history
python3 scripts/phonepe.py transactions --limit 10
```

## API Docs

https://developer.phonepe.com/
