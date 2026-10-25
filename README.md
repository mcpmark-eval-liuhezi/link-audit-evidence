# link-audit-evidence

Evidence repository for the quarterly external-link audit of onboarding documentation.

## Pages checked

- https://example.com/ - Example Domain
- https://www.iana.org/domains/example - Example Domains

## Findings

1. https://example.com/ returned content with the title "Example Domain". Its raw Markdown capture is committed under `captures/`.
2. The 'Learn more' reference on https://example.com/ is produced by the page's own script (`/s.js`) as plain text with no `href`; the served HTML contains no anchor (`<a>`) elements at all. The long-standing target of that reference is https://www.iana.org/domains/example, so that page was audited as the second in-scope link. It returned content with the title "Example Domains", and its raw Markdown capture is committed under `captures/`.

Both in-scope links returned real content: both links check out.

## Status of the Snowflake warehouse log

**Not completed this round.** The Snowflake account's free trial has ended and all virtual warehouses are suspended, so the `audits` database, the `linkcheck` table rows, and the analytics memo insight could not be written.

Because the data-handling policy only permits removing the raw captures once the warehouse rows and the memo insight are in place, **the capture files have been deliberately retained in this repository**. They are the only surviving evidence of this audit round. Re-run the Snowflake steps after billing is restored, then remove `captures/`.

## Notes

- Titles above are exactly as fetched; none were assumed or inferred.
