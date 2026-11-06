# SOP 02: Google Ads Search campaign build (local service business)

**Goal:** a clean, measurable Search campaign that can scale. **Prerequisite:** conversion tracking verified (SOP 01, section 2).

## 1. Plan on paper first

| Decision | Default for local services |
|---|---|
| Campaigns | Brand · Core services (non-brand) · optionally one per high-margin service |
| Ad groups | One per service theme (e.g. *airport transfer*, *corporate car service*), not one per keyword |
| Locations | Service area by city/radius, **Presence** only |
| Schedule | Business hours + any hours someone answers the phone |
| Networks | Search only. Turn **off** Display Network expansion; test Search Partners later |
| Bidding | Maximize Conversions until steady volume, then Target CPA near the observed CPA |
| Budget | Enough for at least several clicks per day per core ad group at the expected CPC |

## 2. Keywords

- Start with phrase and exact match on high-intent terms: *service + location*, *service near me*, *service + qualifier* (price, booking, 24 hour).
- Add broad match only once conversions are reliable and Smart Bidding is on, and watch its search terms closely for the first weeks.
- Keep each ad group tight enough that one ad and one landing page fit every keyword in it.

## 3. Negatives before launch

Apply [`templates/negative-keywords-service-business.csv`](../templates/negative-keywords-service-business.csv) as an account-level or shared list, then add business-specific ones (services you don't offer, areas you don't serve, competitor names if you choose not to bid on them).

## 4. Ads

Per ad group, one responsive search ad to start (add a second for testing once traffic allows):

- **Headlines (up to 15):** service + location · price signal ("Flat Rates", "From $95") · proof (years, reviews, licensing) · differentiators (flight tracking, 24/7) · call to action ("Book Online in 60 Seconds").
- **Descriptions (up to 4):** what's included, who it's for, what happens after they click.
- Pin only where a message must appear (e.g. a regulated disclaimer); heavy pinning limits testing.
- Final URL is the matching service × location page, not the homepage.

## 5. Assets

- Sitelinks to the top services, pricing, fleet and reviews pages.
- Callouts: short benefits (Meet & Greet, Flight Tracking, No Surge Pricing).
- Structured snippets: *Services* or *Types* header with real offerings.
- Call asset with call reporting on, and calls counted as conversions above a sensible duration.
- Location asset if a Google Business Profile is linked.

## 6. Launch checklist

Run [`templates/launch-checklist.md`](../templates/launch-checklist.md) in full. Two items catch most launch mistakes: Display expansion off, and location option set to Presence.

## 7. First 14 days

- Days 1 to 3: check impressions, CPC and search terms daily. Add negatives; don't change bids or targets.
- Days 4 to 14: check every 2 to 3 days. Pause clearly irrelevant keywords. Leave the bid strategy alone unless spend is clearly runaway.
- Day 14: first review against target CPA. Decide on budget changes and whether to introduce Target CPA.

Then move to SOP 05.
