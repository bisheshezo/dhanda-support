# Employee Performance Dashboard

Static browser-based dashboard for importing employee performance, login/logout and paid-report exports.

## Cloudflare Workers deployment

This folder is deployed as a separate Worker using `wrangler.jsonc`.

- Keep the Workers Builds root directory blank (repository root).
- Deploy command: `npx wrangler deploy --config performance-dashboard/wrangler.jsonc`
- Preview command: `npx wrangler preview --config performance-dashboard/wrangler.jsonc`
- The Wrangler assets directory is relative to this config file and is set to `.`.

## Privacy

- Uploaded files are processed locally in the browser.
- No employee rows are bundled into this repository.
- No API/database upload is performed by this starter.
- Refreshing the page clears the imported data.
- Protect the deployed Worker with Cloudflare Access before importing or storing any real employee data.

## Important

Column matching is heuristic. Validate field mappings and calculations against the original exports before using this for payroll, incentives, attendance or formal performance decisions.
