# link-audit-evidence

Evidence repository for the quarterly external-link audit of onboarding documentation.

## Pages checked

- https://example.com/ - Example Domain

## Findings

1. https://example.com/ returned HTTP 200 with the title "Example Domain". Its raw Markdown capture is committed under `captures/`.
2. No "Learn more" link exists on https://example.com/. The served HTML contains no anchor (`<a>`) elements at all, and the words "Learn more" are injected by the page's script (`/s.js`) as plain text with no `href`. Because there is no link to follow, no second page could be fetched in this audit round.

## Notes

- Raw page captures are removed from this repository once the Snowflake audit rows and the analytics memo insight are in place, per the data-handling policy. The warehouse (`audits.linkcheck`) is the system of record.
