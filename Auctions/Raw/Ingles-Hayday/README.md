# Ingles & Hayday (London)

Ingles & Hayday, instrument and bow sales.

## Files
One file per sale: `<date>_Ingles-Hayday_<sale number>.csv`, the shared columns (see the Raw README), in this order,
then the house's extra columns.

## Columns at this house
| Column | Here |
|---|---|
| sale_date | the month (YYYY-MM): the house's results pages give no day; the day only where the house's calendar gives it |
| sale_title | not given by the house: empty |
| title | the catalogue's short title, as published |
| description | the catalogue's full text (label, length of back, documents, provenance), lines written " / " |
| status | sold / unsold, as on the results page; "not in results": in the catalogue, absent from the results page; empty: no result yet |
| hammer | not given by the house: empty |
| price_with_fees | the results page's price ("all results are inclusive of buyer's premium") |
| currency | GBP |
| vat_note (extra) | the catalogue's VAT mark (Reduced Rate, Standard Rate, ...), as published |
| export_note (extra) | the catalogue's note on protected materials (ivory, pernambuco: CITES permits), as published |

## Fees
Buyer's premium, % of the hammer, from the house's conditions of sale; VAT on the premium, not in price_with_fees.
Seller's commission not published.

| Sales | Buyer's premium |
|---|---|
| Oct 2020 – Mar 2026 | 20 % + VAT on the premium (price_with_fees / 1.2 = a round hammer on 1 667 of 1 669 sold lots) |

## Notes
Only violins, violas, cellos and their bows: the house's lots of books, tonewood, loose parts and double-bass bows
are not in these files.


## About the house
Ingles & Hayday is a London auction house and dealership for fine stringed instruments, founded in 2012 by Tim Ingles and Paul Hayday, former heads of Sotheby's musical instrument department. Its 2023 sale of the Rosenberg Collection made £9 million.
Source: [Ingles & Hayday (own site)](https://ingleshayday.com/about-us/), checked 2026-11-03.

## Secondary files (`_snd`)
`<date>_Ingles-Hayday[_<sale number>]_snd.csv` (and `<date>_Ingles-Hayday_press.csv` for the press): lots of this house that the house's own
documents do not give (34 files, 1286 lots).
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
