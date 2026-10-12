# DNS record types I use most

**Date:** 2026-10-12
**Tags:** dns, hosting, domains

## What I learned

- **A**: points a name to an IPv4 address
- **AAAA**: points a name to an IPv6 address
- **CNAME**: points a name to another name (for example `www` to a hosting provider)
- **MX**: tells the world which servers receive email for the domain
- **TXT**: free text, used for SPF, DKIM, and domain verification

A CNAME cannot be set on the root domain at most DNS providers, so use an A record or ALIAS/ANAME there.

## Why it matters

Most "site not loading" and "email not arriving" problems after a domain change are DNS records.
