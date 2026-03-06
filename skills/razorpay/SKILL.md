---
name: razorpay
description: Razorpay payment gateway integration. Process payments, manage subscriptions, handle refunds.
metadata:
  author: ankitjh4
  category: Payments
  display-name: Razorpay Payments
---

# Razorpay Integration

Accept payments via Razorpay - India's payment gateway.

## Setup

1. Get API keys: https://dashboard.razorpay.com/app/keys
2. Add to Zo secrets: `RAZORPAY_KEY_ID`, `RAZORPAY_KEY_SECRET`

## Features

- Create payment links
- Process refunds
- Manage subscriptions
- Fetch transaction history

## Usage

```bash
# Create payment link
python3 scripts/razorpay.py create-payment --amount 50000 --currency INR --description "Test Payment"

# List payments
python3 scripts/razorpay.py payments --status captured

# Process refund
python3 scripts/razorpay.py refund --payment-id pay_xxx
```

## API Docs

https://razorpay.com/docs/api/
