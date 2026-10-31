# Sample Write-up LAB-001 — LAB EXERCISE ONLY, NOT A REAL DISCLOSURE

- Finding ID: LAB-001
- CVE ID: null (no CVE claimed; this is a lab exercise)
- Vendor / product: none — fictional lab service `lab-service-alpha`
- Severity: Medium (lab assessment only)
- System: local lab service, fictional, running on 127.0.0.1 in the lab

## Description

The lab service fetched a URL supplied by the caller without
validating it against an allowlist, so a caller could make the
service request an internal lab address. In the lab, the "internal"
address was another fictional lab service on the same host. No real
internal network, no real service, and no real data were involved.

## Evidence (lab, redacted)

- Lab request: `GET /lab/fetch?url=http://lab-internal.example.invalid/status`
- Lab response: the service returned the lab-internal status page.
- No real addresses, credentials, or data appear in this write-up,
  because none were involved.

## Reproduction (lab only)

1. Start the fictional lab service locally.
2. Request `/lab/fetch` with a lab-internal URL as the parameter.
3. Observe that the service fetches it, instead of rejecting it.

## What was NOT done

No real service was probed, no real internal network was accessed,
and no data was exfiltrated from anywhere. The lab demonstrates
the pattern and the fix, nothing more.

## Suggested remediation (lab)

Validate the supplied URL against an explicit allowlist of hosts
and schemes, reject private and link-local addresses, and do not
follow redirects to unlisted hosts. The fixed lab version applies
exactly that allowlist check.

## Timeline (lab)

| Date | Event |
|---|---|
| Lab day 1 | Finding reproduced in the local lab |
| Lab day 1 | Written up as a lab exercise, labelled as such |
| — | No owner, no vendor, no publication as a real disclosure |
