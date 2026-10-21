# Skinner (Boston)

Skinner, Inc. (Boston, Massachusetts; Bonhams Skinner since 2022).

## Files
One file per sale: `<date>_Skinner_<sale number>.csv`, the shared columns (see the Raw README), in this order.

## Columns at this house
| Column | Here |
|---|---|
| sale_date | the sale's start date (end date for timed online sales) |
| title, description | as published; the house's title is the first sentence of its description |
| hammer | the house's "Sold for" without premium |
| price_with_fees | the house's "Sold for" with buyer's premium |
| maker, estimate_low, estimate_high | not given by the house: empty |
| currency | USD |

## Fees
Buyer's premium, % of the hammer (price_with_fees / hammer on every sold lot); seller's commission not published.

| Sales | Buyer's premium |
|---|---|
| May 2005 – Oct 2007 | 17.5 % |
| May 2008 – May 2011 | 18.5 % |
| Nov 2011 – Apr 2012 | 18.5 %; some lots 22.5 % |
| Oct 2012 – Nov 2013 | 20 %; some lots 23 % (the online sale of Sep 2013: 23 %) |
| Apr 2014 – Nov 2019 | 23 % |
| Jun 2021 | 25 % |

Where a sale has two rates, the house does not say which lots pay the higher one (not the price: both rates
are found on cheap and dear lots).

## Notes
26 Sep 2013 (online sale 2670T): the house's site reports the same figure with and without premium on 176 of the
177 sold lots. We believe it is a site bug: hammer = the figure shown; price_with_fees = hammer + 23 % premium,
calculated by us (the rate of the one lot the site shows with its premium: lot 274, 200 -> 246).
