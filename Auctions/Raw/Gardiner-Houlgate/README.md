# Gardiner Houlgate (Corsham / London)

Gardiner Houlgate, music sales. Two house sources, put together by lot number: the house's results pages and its
printed sale catalogues.

## Files
One file per sale: `<date>_Gardiner-Houlgate_<sale number>.csv`, the shared columns (see the Raw README), in this
order. A catalogue with no results page is a file of its own: `<date>_Gardiner-Houlgate_catalogue.csv`.

## Columns at this house
| Column | Here |
|---|---|
| title | the results page's lot title, as published (long titles end in "..." on the site) |
| description | the printed catalogue's lot text (empty: lot not in a catalogue we hold) |
| estimate_low, estimate_high | the printed catalogue's estimate; else the results page's "Estimate" |
| status | sold where the results page says "Sold for"; empty otherwise (not sold, withdrawn, or no price shown) |
| hammer | the results page's "Sold for" figure: hammer price |
| price_with_fees | not given by the house: empty |
| currency | GBP |

## Fees
Buyer's premium, % of the hammer, from the catalogues' conditions of sale; VAT on the premium.
Seller's commission not published.

| Sales | Buyer's premium |
|---|---|
| Dec 2019 – Mar 2021 | 20 % + VAT on the premium |
| Jun 2021 – Sep 2026 | 22 % + VAT on the premium |

## Notes
The results site lists some lot numbers twice (two different lots, probably 2509 and 2509A with the letter lost on
the site): both kept as published; the catalogue text goes to the one whose title matches it.
17 Jun 2022: no prices on the results page.
Corrected by us: 28 Mar 2025 (specialist sale). The results page shows no "Sold for" at all; instead it shows a
one-figure "Estimate: £X" on 78 of the 79 lots, while the printed catalogue gives each lot a range (e.g. lot 3:
printed £500-800, page "Estimate: £1700"). We believe the site writes the hammer in the wrong place: in this file
those 78 lots are sold, hammer = the page's figure, estimate = the printed range.
