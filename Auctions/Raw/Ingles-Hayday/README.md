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
