# Console walk-through checklist

Use this to re-run a guided walk-through after Console releases. For each screen capture: menu path, what it shows, what each control does, which role it needs, and any gap between the UI and the API. Nothing that moves money is done without the account owner's yes on the spot, and the owner makes the money-moving clicks.

First run: 10 Oct 2026, a customer twin group (primary, second primary, agent twin, two catalog-item provider twins), roles tested Admin, Admin + Manager, Transfer + Manager.

## Covered on the first run
- [x] Sign-in (magic link, passkey offer, Authorize screen), Home, group page, roles and the re-sign-in rule
- [x] Inventory: binder (SSR), SDA, TDN notes, note detail, provenance, Download .toda
- [x] Transactions: filters, CSV, running balance, send and sweep detail pages
- [x] Transfer Activity: filters, detail, note-by-note assembly
- [x] Send form (fields only)
- [x] Purchase TDN: request list and Buy form (Treasury flow explained by the owner)
- [x] Distributions: standing, view, run page with transfer ids, edit form, New
- [x] Paywall form; a catalog item's provider-twin paywall; Directory
- [x] Payment Multiplex: Payers and Top-ups (forms only)
- [x] Banking Profile (owner entered test details); Bank Transfer through to a submitted request; Treasury's Sell Request view (owner screenshot)
- [x] Twin Settings, Usage, Release Notes

## Still open
- [ ] Permissions page (403 for group Admins on 10 Oct 2026)
- [ ] What triggers a standing distribution run (minimum value only, or also a schedule?)
- [ ] Does the Send form accept an email recipient, and does it show a review step?
- [ ] Auto-approve limit and per-service budgets: any Console UI, or API and app only?
- [ ] Personas and delegates in the UI
- [ ] Card top-up path in the Console, if any
- [ ] Admin views for group owners: creating a group, adding twins and members
- [ ] Treasury cancel-and-return for a cash-out (not available on 10 Oct 2026)
