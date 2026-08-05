# Irie Hub Founder Edition v0.8 — Architecture Baseline

## Current structure

- `index.html`: semantic page structure and application views
- `css/app.css`: all application styling
- `js/app.js`: application state, workflows, storage, rendering, and events

## Reason for this release

Version 0.7 separates presentation and behavior from the HTML document without changing the established user workflow. This reduces the risk of future edits and creates a controlled path toward feature modules.

## Planned JavaScript decomposition

The next controlled refactor should separate `js/app.js` into:

- `js/core/storage.js`
- `js/core/security.js`
- `js/core/utilities.js`
- `js/modules/customers.js`
- `js/modules/estimates.js`
- `js/modules/scheduling.js`
- `js/modules/work-orders.js`
- `js/modules/invoices.js`
- `js/modules/expenses.js`
- `js/modules/reports.js`

That decomposition should occur incrementally with regression testing after each extraction.

## Security boundary

Founder Edition v0.8 remains local and single-user. It must not be treated as a secure multi-user system. Before public deployment, all user-controlled content must be rendered with safe DOM APIs or explicit output encoding, and authentication, authorization, server-side validation, audit logging, and protected storage must be implemented.
