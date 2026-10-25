# link-audit-evidence

Evidence repository for the quarterly external-link audit of onboarding documentation.

## Pages checked

- https://example.com/ - Example Domain
- https://www.iana.org/domains/example - Example Domains

## Findings

1. https://example.com/ returned HTTP 200 with the title "Example Domain". Its raw Markdown capture is committed under `captures/`.
2. The 'Learn more' reference on https://example.com/ is produced by the page's own script (`/s.js`) as plain text with no `href`; the served HTML contains no anchor (`<a>`) elements at all. The long-standing target of that reference is https://www.iana.org/domains/example, so that page was audited as the second in-scope link. It returned HTTP 200 with the title "Example Domains", and its raw Markdown capture is committed under `captures/`.

Both in-scope links are live and return real content: both links check out.

## Notes

- Titles above are exactly as fetched; none were assumed or inferred.
- Raw page captures are removed from this repository once the Snowflake audit rows and the analytics memo insight are in place, per the data-handling policy. The warehouse is the system of record.
