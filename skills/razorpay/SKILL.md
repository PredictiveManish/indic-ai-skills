---
name: razorpay
description: Razorpay payment gateway integration. No Zo-specific setup - uses standard environment variables.
metadata:
  author: ankitjh4
  display-name: Razorpay Payments
---

# Razorpay Payment Gateway

Accept payments via Razorpay - India's leading payment gateway.

## API Key Required

1. Create account at https://razorpay.com
2. Get API keys from Dashboard → Settings → API Keys

## Setup

```bash
# Set environment variables
export RAZORPAY_KEY_ID="key_id_xxxxx"
export RAZORPAY_KEY_SECRET="key_secret_xxxxx"
```

## Environment Variables

| Variable | Required | Description |
|----------|----------|-------------|
| RAZORPAY_KEY_ID | Yes | Key ID from Razorpay dashboard |
| RAZORPAY_KEY_SECRET | Yes | Key Secret from Razorpay dashboard |

## Usage

```bash
# Create order
python3 scripts/razorpay.py create-order 50000 "INR"

# Check payment status
python3 scripts/razorpay.py status "pay_xxxxx"

# List payments
python3 scripts/razorpay.py list-payments
```

## Features

- Create payment orders
- Verify payment signatures
- Handle refunds
- List transactions

## API Reference

- Docs: https://razorpay.com/docs/payments/
- API: https://razorpay.com/docs/api/
