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


## About the house
Gardiner Houlgate is a regional auction house based in Corsham, near Bath, England, led by David Hare and Jamie South; its specialist sales include musical instruments, notably guitar auctions and sales from the Jacqueline du Pré Collection. Founding year not confirmed.
Source: [Gardiner Houlgate (own site)](https://www.gardinerhoulgate.co.uk/), checked 2026-11-03.

## Secondary files (`_snd`)
`<date>_Gardiner-Houlgate[_<sale number>]_snd.csv` (and `<date>_Gardiner-Houlgate_press.csv` for the press): lots of this house that the house's own
documents do not give (79 files, 1236 lots).
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
