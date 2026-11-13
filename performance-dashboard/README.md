# Employee Performance Dashboard

Compiled employee-wise performance dashboard for September, October and November 2026 (November data through the 13th).

## Deployment

- Separate Worker name: `employee-performance`
- Wrangler config: `wrangler.jsonc`
- Encrypted dataset: `data.enc.json`
- Keep the Workers Builds root directory blank (repository root).
- Deploy command: `npx wrangler deploy --config performance-dashboard/wrangler.jsonc`
- Preview command: `npx wrangler preview --config performance-dashboard/wrangler.jsonc`

## Data security

- The compiled employee dataset is compressed and encrypted with AES-256-GCM.
- The key is derived from a private passphrase using PBKDF2-SHA256 (310,000 iterations).
- The passphrase is not stored in this repository.
- The browser decrypts the dataset only after the passphrase is entered.
- Do not share the passphrase. Add Cloudflare Access for an additional owner-only sign-in layer.

## Included metrics

Employee profiles, monthly performance, daily attendance/login span, first login, last logout, 9-hour days, CDR calls and modes, talk time, sales and available pause/break summaries.

## Caveat

This dashboard reflects the previously compiled source file. Confirm individual employee figures against source exports before using them for payroll, incentives or formal HR decisions.
