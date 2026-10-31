# Sample Write-up LAB-002 — LAB EXERCISE ONLY, NOT A REAL DISCLOSURE

- Finding ID: LAB-002
- CVE ID: null (no CVE claimed; this is a lab exercise)
- Vendor / product: none — fictional lab application `lab-app-beta`
- Severity: High (lab assessment only)
- System: local lab application, fictional, with fictional users

## Description

The lab application returned any user's record when asked by ID,
without checking that the caller owned that record. In the lab,
caller `lab-alice` could read caller `lab-bob`'s fictional record.
Both users, both records, and the application are fictional.

## Evidence (lab, redacted)

- Lab request: record ID `lab-record-bob`, caller `lab-alice`.
- Lab response: the fictional record for `lab-bob`.
- No real user, record, or data is involved.

## Reproduction (lab only)

1. Start the fictional lab application locally.
2. Authenticate as the fictional lab user `lab-alice`.
3. Request the fictional record belonging to `lab-bob`.
4. Observe that it is returned, instead of a 403 response.

## What was NOT done

No real application was tested, no real user data was accessed,
and no record was modified or deleted.

## Suggested remediation (lab)

Check ownership on the server for every object access, and return
403 for a caller who does not own the object. The fixed lab version
does exactly that, and its test asserts the 403 case.

## Timeline (lab)

| Date | Event |
|---|---|
| Lab day 1 | Finding reproduced in the local lab |
| Lab day 1 | Written up as a lab exercise, labelled as such |
| — | No owner, no vendor, no publication as a real disclosure |
