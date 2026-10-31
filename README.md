# Disclosure-Portfolio

A responsible-disclosure portfolio format: how a finding is written
up, reported, tracked, and — only with owner approval, after the
agreed window — published.

## The important statement, first

Every sample write-up in this repository is a **lab exercise**.
The systems are fictional lab systems, the identifiers are fictional
lab IDs, and **no CVE is claimed for any of them**. A sample is here
to show format, rigour, and restraint — not to inflate a track record.
Presenting a lab exercise as a real disclosure would be fabrication,
and this portfolio is built to make that impossible to do by accident:
every sample is labelled lab-only, on its first line.

## Contents

- `templates/disclosure-report.md` — the report format for a finding.
- `templates/timeline.md` — the disclosure timeline format.
- `templates/owner-approval.md` — the owner-approval checklist that
  must pass before any publication.
- `docs/methodology.md` — how a finding is validated before it is
  reported, and what is never reported.
- `samples/lab-001-ssrf.md`, `samples/lab-002-idor.md`,
  `samples/lab-003-xss.md` — three lab-only sample write-ups
  (fictional lab IDs, cve_id: null, no real vendor).

## How a real disclosure would use this format

1. Validate the finding in the lab or in a system you are authorised
   to test. Record exactly what was tested and what was not.
2. Report privately to the owner, through the owner's chosen channel,
   with the report template, redacted evidence, and a realistic
   severity assessment.
3. Agree a remediation window in writing. Do not publish during it.
4. After the window, publish only what the owner approved, in the
   approved form — or publish nothing, if the owner did not approve
   publication. A private, fixed finding is a complete disclosure;
   publication is optional, not the goal.
5. Never publish exploit detail for an unfixed issue, and never
   publish a finding about a system you were not authorised to test.

## What is not here

- No real vendor, no real product, no real CVE, no real bounty.
- No exploit code for a real system.
- No filled-in report about a real engagement — the templates are
  blank for a reason, and the samples are lab exercises.
