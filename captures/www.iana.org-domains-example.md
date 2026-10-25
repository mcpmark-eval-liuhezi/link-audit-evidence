Example Domains     

[![Homepage](/static/img/iana-logo-header.426b3ac01d35.svg)](/)

*   [Domains](/domains)
*   [Protocols](/protocols)
*   [Numbers](/numbers)
*   [About](/about)

1.  [Instructions and Guides](/help)

Example Domains
===============

A number of domains such as `example.com` and `example.org` are maintained for documentation purposes. These domains may be used as illustrative examples in documents without prior coordination with us. They are not available for registration or transfer.

We provide a web service on the example domain hosts to provide basic information on the purpose of the domain. These web services are provided as best effort, but are not designed to support production applications. We strongly recommend you do not design applications that require the example domains to have operating HTTP service.

Further Reading
---------------

*   [IANA-managed Reserved Domains](/domains/reserved)
*   [Special-Use Domain Names](/go/rfc6761) (RFC 6761)
*   [Reserved Top Level DNS Names](/go/rfc2606) (RFC 2606)

Last revised 2026-09-27.

[Domain Names](/domains)

*   [Root Zone Registry](/domains/root)
*   [.INT Registry](/domains/int)
*   [.ARPA Registry](/domains/arpa)
*   [IDN Repository](/domains/idn-tables)

[Number Resources](/numbers)

*   [Number Registries](/numbers/registries)
*   [RIR Allocation Data](/numbers/allocations/)
*   [Abuse Information](/help/abuse)

[Protocols](/protocols)

*   [Protocol Registries](/protocols)
*   [Time Zone Database](/time-zones)

[About Us](/about)

*   [News](/news)
*   [Performance](/performance)
*   [The Organization](/about/organization)
*   [Archive](/archive)
*   [Contact Us](/contact)

The IANA functions coordinate the Internet's globally unique identifiers, and are provided by [Public Technical Identifiers](https://pti.icann.org), an affiliate of [ICANN](https://www.icann.org/).

*   [Privacy Policy](https://www.icann.org/privacy/policy)
*   [Terms of Service](https://www.icann.org/privacy/tos)

// Highlight the table-of-contents entry for the section currently at the // top of the viewport, following the page as it scrolls. Purely additive: // without JS the rail still works as a list of jump links. (function () { var toc = document.querySelector('.article-toc'); if (!toc) return; var sections = Array.prototype.map.call( toc.querySelectorAll('a\[href^="#"\]'), function (a) { var id = decodeURIComponent(a.getAttribute('href')).slice(1); var target = document.getElementById(id); return target ? { link: a, target: target } : null; } ).filter(function (s) { return s; }); if (!sections.length) return; var current = null; function update() { var line = 120; // trigger line, px below the top of the viewport var active = sections[0]; for (var i = 0; i < sections.length; i++) { if (sections[i].target.getBoundingClientRect().top - line <= 0) { active = sections[i]; } } if (active && active.link !== current) { if (current) { current.classList.remove('is-current'); current.removeAttribute('aria-current'); } current = active.link; current.setAttribute('aria-current', 'location'); } } var ticking = false; function onScroll() { if (ticking) return; ticking = true; window.requestAnimationFrame(function () { update(); ticking = false; }); } window.addEventListener('scroll', onScroll, { passive: true }); window.addEventListener('resize', onResize); update(); })();
