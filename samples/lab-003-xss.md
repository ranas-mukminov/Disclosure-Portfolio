# Sample Write-up LAB-003 — LAB EXERCISE ONLY, NOT A REAL DISCLOSURE

- Finding ID: LAB-003
- CVE ID: null (no CVE claimed; this is a lab exercise)
- Vendor / product: none — fictional lab page `lab-page-gamma`
- Severity: Medium (lab assessment only)
- System: local lab page, fictional, rendering a caller-supplied name

## Description

The lab page rendered a caller-supplied name without escaping, so
a script tag in the name was rendered as markup. In the lab, the
script was a harmless `alert` placeholder in a local browser view
of a local page. No real user, no real session, and no real site
were involved.

## Evidence (lab, redacted)

- Lab input: name `<script>alert(1)</script>` (lab placeholder).
- Lab output: the script tag appeared unescaped in the page source.
- No real session, cookie, or user data is involved.

## Reproduction (lab only)

1. Start the fictional lab page locally.
2. Supply a name containing a script tag.
3. Observe that it is rendered unescaped.

## What was NOT done

No real site was tested, no session was stolen, no user was
affected, and no script was executed against anyone else.

## Suggested remediation (lab)

Escape user input at render time, and treat all caller-supplied
text as text, never as markup. The fixed lab version escapes the
name, and its test asserts that no script tag survives rendering.

## Timeline (lab)

| Date | Event |
|---|---|
| Lab day 1 | Finding reproduced in the local lab |
| Lab day 1 | Written up as a lab exercise, labelled as such |
| — | No owner, no vendor, no publication as a real disclosure |
