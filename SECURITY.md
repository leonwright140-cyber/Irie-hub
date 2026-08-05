# Irie Hub Founder Edition v0.8 — Verification Record

## Automated checks performed

- ZIP integrity check
- HTML file presence check
- CSS and JavaScript reference check
- JavaScript syntax validation with Node.js
- Verification that the inline `<style>` and inline application `<script>` blocks were removed
- Verification that the external CSS and JavaScript files are non-empty

## Manual acceptance checklist

1. Open `index.html` in Safari or Chrome.
2. Confirm the dashboard loads with the normal styling.
3. Confirm existing customer records appear.
4. Open Customer CRM and verify search and customer details.
5. Open Estimates and verify existing records.
6. Open Scheduling and verify existing records.
7. Open Invoices and Expenses.
8. Export a backup.
9. Import the backup into a test browser profile or after creating a recovery snapshot.
10. Confirm no data loss and no visible workflow regression.

## Known limitation

Some user-entered data is still rendered through HTML template strings. Complete output-encoding hardening remains required before public or multi-user deployment.
