# Methodology

## Before a finding is reported

1. **Reproduce it.** A finding that happens once, under unclear
   conditions, is not a finding yet. Reproduce it in the lab or in
   the authorised scope, and record the conditions.
2. **Scope it.** State the exact system, version, account, and
   conditions. A finding that only occurs with an admin account is
   a different finding from one that occurs unauthenticated, and
   the report must say which.
3. **Bound the impact.** Distinguish what was demonstrated from
   what is theoretically possible. "An attacker could read any
   record" is a claim that needs a demonstration within scope, or
   it is labelled as theoretical.
4. **Redact it.** Remove secrets, tokens, personal data, and
   internal addresses from every artefact before it leaves the
   test environment.
5. **Check the scope again.** If any step of the reproduction went
   outside the authorised scope, the finding is not reportable in
   that form. Report the scope issue to the owner, and re-validate
   within scope.

## What is never reported as a finding

- A lab exercise, presented as a real disclosure.
- A finding about a system that was not authorised for testing.
- A finding with invented evidence, an invented CVE, or an invented
  vendor response.
- A finding published before the owner had the agreed window, or
  with detail the owner did not approve.

## Severity, honestly

Severity is assigned by impact and by the access required, not by
the impressiveness of the technique. A technically interesting flaw
with no realistic impact is a low finding, and the report says so.
Inflating severity to make a portfolio look stronger destroys the
credibility the portfolio is meant to build.
