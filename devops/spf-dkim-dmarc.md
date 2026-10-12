# SPF, DKIM and DMARC

**Date:** 2026-10-12
**Tags:** email, dns, microsoft365

## What I learned

Three DNS records help receiving mail servers trust email from your domain:

- **SPF** (TXT record): lists which servers are allowed to send mail for the domain
- **DKIM**: adds a cryptographic signature to outgoing mail, verified with a public key published in DNS
- **DMARC** (TXT record at `_dmarc`): tells receivers what to do when SPF/DKIM checks fail (none, quarantine, reject) and where to send reports

## Why it matters

Without them, legitimate emails can land in spam and others can spoof your domain more easily. When setting up Microsoft 365 or any email provider for a domain, these are the records to check first.
