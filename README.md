# Qatom Console skill

An agent skill for running a Qatom store or wallet after launch in the TODAQ Console (https://console.todaq.net) and by API: see your assets and transaction records, find out who paid, inspect and verify TODA files and sales, send funds, sweep item revenue to your main wallet or pay up to 200 people with distributions, put a twin paywall in front of an API, set up Payment Multiplex for high-volume buying, buy TDN and cash out to a bank.

> **Status: 0.2.** Written from a guided walk-through of a live customer account in the TODAQ Console (console.todaq.net) with the Qatom founder on 10 Oct 2026, plus the published v4 OpenAPI.

## Install

```bash
npx skills add StarwaterHeaven/qatom-console-skill --skill qatom-console
```

Then ask your agent: *"Where did the payments for my Qatom items go?"* *"Help me sweep my item revenue to my primary twin."* or *"How do I cash out to my bank?"*

## What's inside

| File | What it is |
|---|---|
| [`SKILL.md`](skills/qatom-console/SKILL.md) | The skill: how a sale moves through the twins, the TODA file types, sign-in and roles, records and verification, sending, distributions, twin paywalls, Payment Multiplex, buying TDN and cashing out, settings, approvals, recipes |
| [`references/api-map.md`](skills/qatom-console/references/api-map.md) | Every Console-relevant API endpoint, grouped |
| [`references/walkthrough-checklist.md`](skills/qatom-console/references/walkthrough-checklist.md) | What a Console walk-through covers, and what is still open |

## Money safety

This skill never moves money, changes a distribution, a paywall price or an approval limit without the human's explicit yes for that change, and leaves the money-moving clicks, passwords, API keys and bank details to the human. Agents only ever spend what their own agent twin holds.

## Related

- Designing and listing items: https://github.com/StarwaterHeaven/qatom-seller-guide
- A setup recipe for every use case: https://github.com/StarwaterHeaven/qatom-use-cases
- Qatom API reference: https://docs.m.todaq.net

## About

Published by StarwaterHeaven and Wizard Kepler. MIT licensed.
