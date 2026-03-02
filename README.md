# NAS Vault — Encrypted Personal Finance Tracker

Fully client-side, AES-256-GCM encrypted money manager for GitHub Pages.

## How It Works

- All encryption happens in your browser using Web Crypto API
- AES-256-GCM with PBKDF2 (SHA-256, 310K iterations)
- Even on a public repo, your data is unreadable without your password
- No server, no database, no third-party services

## Quick Setup

1. **Create a GitHub repo** (can be public — data is encrypted)
2. **Copy `index.html`** to the root and push
3. **Enable GitHub Pages**: Settings → Pages → Deploy from main branch
4. **Create a PAT**: Settings → Developer Settings → Fine-grained tokens → Contents: Read & Write
5. **First visit**: Open your Pages URL, expand "GitHub Setup", enter token + repo
6. **Set a master password** and click Unlock
7. **Click "↑ Push"** to save your encrypted vault to GitHub

## Features

- Dashboard with account balances (DBBL, BRAC, bKash, Nagad, Rocket, Cash)
- Full CRUD transactions with search/filter/pagination
- **⚖ Balance Adjustment** — manually fix any account balance without a fake transaction
- Analytics charts (income/expense trends, category breakdown, daily spending)
- CSV export with all balances
- Borrowed/Loaned tracking
- Offline local fallback (encrypted)

## Balance Adjustment

If your balances don't match reality, go to the **⚖ Adjust** tab. Enter the correct balance for any account and apply. This creates a special ADJUSTMENT entry that sets balances directly without needing a fake transaction.

## Pre-loaded Data

482 transactions (Nov 2024 — Mar 2026) with actual Excel-computed balances preserved exactly as they were in your spreadsheet.
