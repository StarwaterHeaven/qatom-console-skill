# Console walk-through checklist

What to capture on a guided session in a live account (first run: the Centaur League twin group, with Hassan). For each screen: where it is (menu path), what it shows, what each control does, what needs MFA or a second device, and a screenshot reference. Nothing that moves money is done without the account owner's yes on the spot.

## 1. Orientation
- [ ] Console URL and sign-in path; MFA prompts and on which device
- [ ] How a twin group is created and named; how twins are added to it
- [ ] Twin list: columns (name, hostname, role, balance), filters, refresh behaviour

## 2. Assets and transaction records
- [ ] Opening a twin: holdings, history, export options (and whether they match binder / inventory CSV)
- [ ] Finding the payments for one catalog item (by provider twin, by commodity hash)
- [ ] Revenue views, if any

## 3. Inspect and verify
- [ ] Opening a single TODA file: issuer, type, amount, provenance, integrity check
- [ ] Verifying a sale by transaction id
- [ ] What "verified" looks like on screen, and what a failed check looks like

## 4. Moving funds
- [ ] Manual transfer between twins in the group: fields, confirmation, MFA, how long until balances show
- [ ] Transfer to an outside twin URL or email
- [ ] Which twin `POST /v4/transfer` spends from (confirm: primary) — Centaur question from 4 Oct

## 5. Distributions
- [ ] Where rules are created; required fields
- [ ] Schedule options (times per day, specific times, on every payment?)
- [ ] Split by percentage, fixed amount, or remainder; several destinations
- [ ] Minimum balance kept back
- [ ] Run history; pausing, editing and deleting a rule
- [ ] Centaur: create (#32) and join (#33) twins → primary, a few times a day

## 6. Twin API paywall
- [ ] Where a twin's paywall is configured; fields vs `POST /v4/twin/{hostname}/config` (targetUrl, pay type, price)
- [ ] Where `paywallUrl` is shown; how it is then listed
- [ ] How a call through it appears in the twin's records

## 7. Approvals, limits, budgets
- [ ] Where the auto-approve limit is set in the UI
- [ ] Where per-service spending budgets are seen and revoked
- [ ] Approval review page for an agent's request

## 8. Multiplex buying
- [ ] Using a twin group for buying: several agent twins funded from one primary
- [ ] Per-agent limits; scheduled top-ups
- [ ] Personas and delegates in the UI, if present

## 9. Gateways (human only)
- [ ] Card top-up, ACH and wire in; withdrawal out; who can see these screens
- [ ] Confirm agents and connected apps cannot reach them

## Output
For each item: menu path, steps, screenshot name, any gap between UI and API. Then update `SKILL.md` and drop the "(Console steps: to be confirmed)" markers that are now confirmed.
