# Irie Hub Founder Edition v0.8 — Security Hardening

## Controls added

- Sanitizes all HTML assigned through `innerHTML` before it reaches the page.
- Removes executable elements including scripts, iframes, objects, embeds, forms, and metadata elements.
- Removes inline event-handler attributes such as `onclick` and `onerror`.
- Blocks `javascript:` and `vbscript:` URLs.
- Restricts `data:` URLs to images, preserving locally stored estimate photos.
- Adds basic email-format validation for newly created customers.
- Migrates existing local data into the v0.8 storage key without changing financial methodology.

## Scope

This release materially reduces stored and reflected cross-site scripting risk in the current single-user browser-local edition. It is not authorization for public or multi-user deployment. A hosted edition will also require server-side validation, authentication, authorization, Content Security Policy, secure headers, audit logging, dependency review, and penetration testing.
