# GLP-1 telehealth price moves

Every change I recorded in the monthly listed price of a GLP-1 plan at US telehealth providers in the 30 days to November 3, 2026: 20 changes at 7 providers, each with the old price, the new price, the day I recorded it and the provider's own page.

Maintained by Calin Rasniceru, founder and editor of [glp1updates.com](https://glp1updates.com). The live, dated record is at https://glp1updates.com/price-moves

## At a glance

| | |
|---|---|
| Recorded | 2026-10-13 to 2026-11-03 |
| Rows | 20, one per plan price change |
| Providers | 7 |
| Direction | 19 cuts, 1 rise |
| Cuts | Median 33%, smallest 10.1%, largest 55.6% |
| Format | CSV, UTF-8, one header row |
| Licence | [CC BY 4.0](LICENSE) |
| DOI | [10.5281/zenodo.24056779](https://doi.org/10.5281/zenodo.24056779) |
| Status | A snapshot. The live record keeps updating on the site. |

## A look at the file

Five of the 20 rows, trimmed to six of the ten columns:

| date_recorded | provider | plan | old_price_usd_per_month | new_price_usd_per_month | change_pct |
|---|---|---|---|---|---|
| 2026-10-13 | Yucca Health | GLP-1 (Semaglutide): month-to-month | 146 | 89 | -39.0 |
| 2026-10-21 | Maximus | Compounded tirzepatide: 6-month plan | 199.99 | 119.99 | -40.0 |
| 2026-10-26 | Pallas Health | Wegovy® | 1349 | 599 | -55.6 |
| 2026-10-26 | Strut Health | Compounded Injectable Tirzepatide | 149 | 219 | +47.0 |
| 2026-11-03 | Embody | Compounded Semaglutide Injections: flat monthly | 69 | 49 | -29.0 |

## Load it

```python
import pandas as pd

url = "https://raw.githubusercontent.com/glp1updates/glp1-price-moves/main/glp1-price-moves-2026-11-03.csv"
moves = pd.read_csv(url, parse_dates=["date_recorded"])
```

## What counts as a move

A change in the monthly price of one plan between two readings, each confirmed against the provider's own page. The date is the day I recorded the new price, not necessarily the day the provider changed it.

## Files

- `glp1-price-moves-2026-11-03.csv`: 20 rows, one per move.
- `CITATION.cff`: the citation, used by GitHub's "Cite this repository" button.
- `LICENSE`: the CC BY 4.0 text.

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
- One row is one plan. A provider that cuts several plans at once, or lists the same plan on two of its pages, produces several rows.
- A price can move and move back. One plan here, Strut Health's compounded injectable tirzepatide, rose on 2026-10-26 and returned to its old price on 2026-11-02. Both moves are rows.
- Compounded medicines are mixed by a pharmacy and are not FDA-approved. The FDA does not review them for safety, effectiveness or quality before they are sold.
- A price cut says nothing about a provider's quality or safety.

## Related

- [Price moves](https://glp1updates.com/price-moves): the live record, by provider and medication.
- [GLP-1 price index](https://glp1updates.com/price-index/csv): a CSV of every price on file, rebuilt daily, also CC BY 4.0.
- [Methodology](https://glp1updates.com/methodology): how a price is read, dated and made comparable.

## Licence

CC BY 4.0. Use it freely, including commercially, and credit "glp1updates.com price moves" with a link to https://glp1updates.com/price-moves.

## Disclosure

glp1updates.com earns a commission from some providers when a reader signs up through its links. Those providers are marked `verified_partner = true`. A partnership never changes how a provider is listed.

## How to cite

glp1updates.com, "GLP-1 telehealth price moves, 30 days to 2026-11-03", https://glp1updates.com/price-moves. DOI: https://doi.org/10.5281/zenodo.24056779
