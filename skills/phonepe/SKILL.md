---
name: phonepe
description: PhonePe UPI payment integration. No Zo-specific setup - uses standard environment variables.
metadata:
  author: ankitjh4
  display-name: PhonePe UPI Payments
---

# PhonePe UPI Payment Gateway

Accept UPI payments via PhonePe - India's leading UPI platform.

## API Key Required

1. Register at https://business.phonepe.com
2. Get API credentials from merchant dashboard

## Setup

```bash
# Set environment variables
export PHONEPE_MERCHANT_ID="your_merchant_id"
export PHONEPE_SALT_KEY="your_salt_key"
export PHONEPE_SALT_INDEX=1
# Environment: production or preprod (testing)
export PHONEPE_ENV="preprod"
```

## Environment Variables

| Variable | Required | Description |
|----------|----------|-------------|
| PHONEPE_MERCHANT_ID | Yes | Merchant ID from PhonePe |
| PHONEPE_SALT_KEY | Yes | Salt key for signing |
| PHONEPE_SALT_INDEX | Yes | Salt index (usually 1) |
| PHONEPE_ENV | No | "preprod" or "production" |

## Usage

```bash
# Initiate UPI collect
python3 scripts/phonepe.py collect "upi@upi" 100 "order123"

# Check transaction status
python3 scripts/phonepe.py status "txn_id"

# Create QR payment
python3 scripts/phonepe.py qr 500 "order456"
```

## Features

- UPI Collect (request payment)
- QR Code payments
- Check transaction status
- Refunds

## API Endpoints

- Sandbox: `https://api-preprod.phonepe.com`
- Production: `https://api.phonepe.com`

## Docs

- https://developer.phonepe.com/
