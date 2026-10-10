# Console walk-through checklist

First run completed 10 Oct 2026 (all sections; Permissions returned 403 for group Admins). Use this list to re-run it after Console releases.

What to capture on a guided session in a live account (first run: the Centaur League twin group, with Hassan). For each screen: where it is (menu path), what it shows, what each control does, what needs MFA or a second device, and a screenshot reference. Nothing that moves money is done without the account owner's yes on the spot.

## 1. Orientation
- [x] Console URL and sign-in path; MFA prompts and on which device
- [x] How a twin group is created and named; how twins are added to it
- [x] Twin list: columns (name, hostname, role, balance), filters, refresh behaviour

## 2. Assets and transaction records
- [x] Opening a twin: holdings, history, export options (and whether they match binder / inventory CSV)
- [x] Finding the payments for one catalog item (by provider twin, by commodity hash)
- [x] Revenue views, if any

## 3. Inspect and verify
- [x] Opening a single TODA file: issuer, type, amount, provenance, integrity check
- [x] Verifying a sale by transaction id
- [x] What "verified" looks like on screen, and what a failed check looks like

## 4. Moving funds
- [x] Manual transfer between twins in the group: fields, confirmation, MFA, how long until balances show
- [x] Transfer to an outside twin URL or email
- [x] Which twin `POST /v4/transfer` spends from (confirm: primary) — Centaur question from 4 Oct

## 5. Distributions
- [x] Where rules are created; required fields
- [x] Schedule options (times per day, specific times, on every payment?)
- [x] Split by percentage, fixed amount, or remainder; several destinations
- [x] Minimum balance kept back
- [x] Run history; pausing, editing and deleting a rule
- [x] Centaur: create (#32) and join (#33) twins → primary, a few times a day

## 6. Twin API paywall
- [x] Where a twin's paywall is configured; fields vs `POST /v4/twin/{hostname}/config` (targetUrl, pay type, price)
- [x] Where `paywallUrl` is shown; how it is then listed
- [x] How a call through it appears in the twin's records

## 7. Approvals, limits, budgets
- [x] Where the auto-approve limit is set in the UI
- [x] Where per-service spending budgets are seen and revoked
- [x] Approval review page for an agent's request

## 8. Multiplex buying
- [x] Using a twin group for buying: several agent twins funded from one primary
- [x] Per-agent limits; scheduled top-ups
- [x] Personas and delegates in the UI, if present

## 9. Gateways (human only)
- [x] Card top-up, ACH and wire in; withdrawal out; who can see these screens
- [x] Confirm agents and connected apps cannot reach them

## Output
For each item: menu path, steps, screenshot name, any gap between UI and API. Then update `SKILL.md` and drop the "(Console steps: to be confirmed)" markers that are now confirmed.
