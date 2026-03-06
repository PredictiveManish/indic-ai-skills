---
name: zoho
description: Zoho CRM, Books, and other Zoho services integration. Manage contacts, leads, invoices, and more.
metadata:
  author: ankitjh4
  category: Business
  display-name: Zoho Suite
---

# Zoho Integration

Connect to Zoho's suite of business applications.

## Supported Services

- **Zoho CRM** - Customer relationship management
- **Zoho Books** - Accounting & invoicing
- **Zoho Projects** - Project management
- **Zoho Desk** - Helpdesk tickets

## Setup

1. Get Zoho API credentials: https://api-console.zoho.com/
2. Add to Zo secrets: `ZOHO_CLIENT_ID`, `ZOHO_CLIENT_SECRET`, `ZOHO_ACCESS_TOKEN`

## Usage

```bash
# List contacts from Zoho CRM
python3 scripts/zoho.py contacts --module Leads

# Create a new lead
python3 scripts/zoho.py create-lead --first-name John --last-name Doe --email john@company.com

# List invoices
python3 scripts/zoho.py invoices --status overdue
```

## API Endpoints

- CRM: https://www.zoho.com/crm/developer/docs/api/
- Books: https://www.zoho.com/books/api/v3/
