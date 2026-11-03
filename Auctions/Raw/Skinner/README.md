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
| estimate_low, estimate_high | not given by the house: empty |
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

## Price lists (`_prices`)
`<date>_<house>_<sale number>_prices.csv`: the house's own printed price list of a sale ('Prices Realised' printed at
the back of the next catalogue, a sale-room results sheet), typed from a paper copy: lot, status, and the price as
the list prints it: the hammer, or the price with the premium (price_with_fees), or both; the other column is empty. No lot text, no
maker: the list gives none. `last_bid` = the bid a bought-in lot stopped at (Sotheby's results sheets); `vat_mark` =
the list's '*' / '**' (VAT on the hammer). price_source = Primary.
`note` (here and in the house files of the typed catalogues): where a figure is read otherwise than the paper prints it,
why. Mostly the house's own misprints, checked on the paper (the note says so): a lot number printed twice or out of
place, read as the missing lot; a price printed out of its column, read as the figure its digits stand under; a price the house
corrected in a later catalogue. Everywhere else the price list is as printed.


## About the house
Skinner was a Boston-area auction house founded by Robert W. Skinner Jr.; Bonhams gives 1962 as the founding year, while Wikipedia records incorporation in 1971 at Bolton, Massachusetts. Acquired by Bonhams in March 2022, it now trades as Bonhams Skinner.
Source: [Wikipedia (CC BY-SA)](https://en.wikipedia.org/wiki/Skinner,_Inc.), checked 2026-11-03.

## Secondary files (`_snd`)
`<date>_Skinner[_<sale number>]_snd.csv` (and `<date>_Skinner_press.csv` for the press): lots of this house that the house's own
documents do not give (49 files, 2900 lots).
They come from secondary sources, such as published compilations of auction results and the author's notes, and from
the press (`Press`). The columns are the same as in the house files; `description` is the maker's name as the source
writes it, and `type` the source's own category.

**`price_source`**
- `Cross-checked`: a second source gives the same price (or the same price without the buyer's premium).
- `Secondary`: one source only. Published when the source names the auction house and gives the day of the sale, or only
  its month (then `sale_date` is empty and the month is in the file name; the sale may have lasted two or three days).
- `Primary`: the price is confirmed by the house's own price list; the maker is still the secondary source's.
- `Press`: a press report of the sale, with `press_publication`, `press_date`, `press_page` and `press_link`.

`hammer` is the hammer price where the source gives it. Where only the month of a sale is known, `sale_date` is left empty
and the month is in the file name. A lot already in the house's own file is not repeated. One line per lot: where two
sources disagree, one price is kept and the other left out.
