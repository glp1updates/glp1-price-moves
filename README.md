# GLP-1 telehealth price moves

Every change I recorded in the monthly listed price of a GLP-1 plan at US telehealth providers in the 30 days to November 3, 2026: 20 changes at 7 providers, each with the old price, the new price, the day I recorded it and the provider's own page.

Maintained by Calin Rasniceru, founder and editor of glp1updates.com. The live, dated record is at https://glp1updates.com/price-moves

**Summary:** 19 cuts and 1 rise. The median cut was 33%.

## What counts as a move

A change in the monthly price of one plan between two readings, each confirmed against the provider's own page. The date is the day I recorded the new price, not necessarily the day the provider changed it.

## Files

- `glp1-price-moves-2026-11-03.csv`: 20 rows, one per move.

## Columns

| Column | Meaning |
|---|---|
| `date_recorded` | The day the new price was recorded (YYYY-MM-DD). |
| `provider` | The provider's name. |
| `verified_partner` | `true` if glp1updates.com has an affiliate link with this provider (see Disclosure). |
| `plan` | The plan, as the provider names it. |
| `old_price_usd_per_month` | The monthly price at the earlier reading, in US dollars. |
| `new_price_usd_per_month` | The monthly price at the later reading, in US dollars. |
| `change_pct` | The change, to one decimal place. Negative is a cut. |
| `direction` | `cut` or `rise`. |
| `source_url` | The provider's own page the new price was read from. |
| `tracker_url` | The live record on glp1updates.com. |

## Read before using

- These are listed cash prices, not insured prices, and they are readings, not live prices. A price recorded on a given day may have moved since.
- Every plan is recorded as a monthly figure. Some providers bill in other cycles, such as every four weeks or one payment per term, and many of the lowest rates need a multi-month commitment. The source page has the terms.
- Compounded medicines are mixed by a pharmacy and are not FDA-approved. The FDA does not review them for safety, effectiveness or quality before they are sold.
- A price cut says nothing about a provider's quality or safety.

## Licence

CC BY 4.0. Use it freely, including commercially, and credit "glp1updates.com price moves" with a link to https://glp1updates.com/price-moves.

## Disclosure

glp1updates.com earns a commission from some providers when a reader signs up through its links. Those providers are marked `verified_partner = true`. A partnership never changes how a provider is listed.

## How to cite

glp1updates.com, "GLP-1 telehealth price moves, 30 days to 2026-11-03", https://glp1updates.com/price-moves
