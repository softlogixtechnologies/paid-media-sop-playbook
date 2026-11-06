# SOP 01: Account audit (new client or takeover)

**Goal:** know what's broken before changing anything. **Time:** 2 to 4 hours per platform. **Output:** audit doc with findings ranked by impact and a 30-day fix plan.

Do not edit the account during the audit. Record what you find, then fix in priority order.

## 1. Access and ownership

- [ ] Client owns the Google Ads account, GA4 property, GTM container and Meta Business Portfolio. The agency has user access, not ownership.
- [ ] Billing is on the client's payment method.
- [ ] Google Ads is linked to GA4 and to the Merchant Center (if e-commerce). Auto-tagging is on.
- [ ] Meta Pixel / dataset is owned by the client's Business Portfolio, not a former agency's.

## 2. Measurement (always first)

Bad conversion data makes every other finding unreliable.

- [ ] List every conversion action in Google Ads: source (Google Ads tag, GA4 import, offline import, calls), counting (One / Every), primary or secondary.
- [ ] Flag duplicates: the same business action counted by two primary actions (e.g. a Google Ads lead tag **and** an imported GA4 `generate_lead`).
- [ ] Flag soft conversions set as primary (page views, scroll, time on site, button clicks).
- [ ] Check leads fire on successful submit, not on button click. Submit a test form in GTM Preview.
- [ ] Meta: Events Manager shows the main event with an event ID, and server events (CAPI) are deduplicated.
- [ ] Compare platform-reported conversions with the client's CRM or booking system for the last 30 days. A large gap is a finding on its own.

Fix kit: [ga4-gtm-conversion-tracking-kit](https://github.com/softlogixtechnologies/ga4-gtm-conversion-tracking-kit).

## 3. Structure

- [ ] Campaigns map to business lines and margins, not to whoever built them.
- [ ] Brand and non-brand search are in separate campaigns, so non-brand performance isn't flattered by brand traffic.
- [ ] Location targeting uses **Presence** (people in or regularly in the area) for local services, not "Presence or interest".
- [ ] Ad schedule matches when the business can answer the phone.
- [ ] No campaigns limited by budget while others with worse CPA have spare budget.

## 4. Queries and keywords (Search)

- [ ] Search terms report, last 90 days, sorted by cost: list the irrelevant spend (jobs, DIY, free, competitors you don't want, wrong service, wrong area).
- [ ] Negative keyword lists exist and are applied at the right level (account-level for universal junk, shared lists per campaign type).
- [ ] Broad match is only running alongside Smart Bidding and reliable conversion data.

## 5. Ads and assets

- [ ] Each ad group has at least one responsive search ad with distinct headlines (service, location, price signal, proof, call to action).
- [ ] Sitelinks, callouts, structured snippets and a call asset are set at account or campaign level.
- [ ] Landing pages match the ad's service and location and load fast on mobile.

## 6. Bidding and budgets

- [ ] Bid strategy matches data volume. Target CPA or ROAS needs consistent conversions to learn; low-volume campaigns often do better on Maximize Conversions or manual CPC first.
- [ ] Targets are realistic against the last 30 days' actual CPA or ROAS.
- [ ] No frequent target changes in the change history (each big change can restart learning).

## 7. Meta specifics

- [ ] Campaign objective matches the outcome (Leads or Sales, not Traffic, for conversion goals).
- [ ] Ad sets are consolidated enough to exit learning (Meta's guidance is roughly 50 optimization events per ad set per week).
- [ ] Creative: at least 3 to 6 distinct concepts live; frequency and CTR trends checked for fatigue.
- [ ] Lead forms (if used) have a qualifying question and leads reach the CRM within minutes.

## 8. Write it up

Use [`templates/client-report-template.md`](../templates/client-report-template.md) sections 1 to 3. Rank each finding:

| Priority | Meaning |
|---|---|
| P1 | Measurement wrong, or money clearly wasted. Fix this week. |
| P2 | Structural issues limiting scale or efficiency. Fix in 30 days. |
| P3 | Optimisation opportunities. Schedule into the weekly routine. |
