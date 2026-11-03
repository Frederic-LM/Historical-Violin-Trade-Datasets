# Aguttes (Neuilly-sur-Seine)

Aguttes, "Instruments & Archets du quatuor" sales.

## Files
One file per sale: `<date>_Aguttes_<sale number>.csv`, the shared columns (see the Raw README), in this order,
then the house's extra columns.

## Columns at this house
| Column | Here |
|---|---|
| sale_title, title, description | in French, as published |
| title, description | as published; up to Jun 2025 the description starts with the title; from Nov 2025 the title is
the house's two heading lines joined by " / " (e.g. "VIOLON FRANÇAIS / Travail de Mirecourt XIXe") |
| status | sold (the house shows only sold lots) |
| hammer | the house's result: hammer price (adjudication) |
| price_with_fees | not given by the house: empty |
| currency | EUR |
| description_english (extra) | the house's English version of the description, where it gives one |

## Fees
Buyer's premium, % of the hammer, from the house's conditions of sale; VAT (20 %) on the premium.

| Sales | Buyer's premium |
|---|---|
| Jun 2022 | 25 % + VAT (30 % incl. VAT) up to EUR 150 000; 23 % + VAT (27.6 %) above |
| Jun 2023 – Nov 2024 | 20 % + VAT (24 % incl. VAT) |
| Jun 2025 | not known (no conditions of sale found) |
| Nov 2025 – May 2026 | 21 % + VAT (25.2 % incl. VAT) |

Seller's commission: agreed with each seller, not published.


## About the house
Aguttes is an independent French auction house founded in 1974 by Claude Aguttes in Clermont-Ferrand, today headquartered in Neuilly-sur-Seine with offices in Lyon, Aix-en-Provence, Brussels and Geneva.
Source: [Wikipedia (CC BY-SA)](https://fr.wikipedia.org/wiki/Aguttes), checked 2026-11-03.

## Secondary files (`_snd`)
`<date>_Aguttes[_<sale number>]_snd.csv` (and `<date>_Aguttes_press.csv` for the press): lots of this house that the house's own
documents do not give (19 files, 137 lots).
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
