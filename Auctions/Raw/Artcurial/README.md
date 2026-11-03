# Artcurial (Paris)

Artcurial, Paris. One sale here: 16 December 2025, a sale of a single lot, the violin by Giuseppe Guarneri "del Gesù",
circa 1727-1730.

## Files
`2025-12-16_Artcurial.csv`: the lot's heading and text from the house's lot page (in French), and the result the house
published: EUR 2 314 800, price with fees.

## Fees
From the catalogue's conditions of sale: buyer's premium 27 % + VAT up to EUR 850 000, 21 % + VAT from EUR 850 001 to
6 000 000, 14.5 % + VAT above (VAT 20 % on the premium). The result divides into a round hammer of EUR 1 800 000 by
this scale (not published by the house).


## About the house
Artcurial is a Paris auction house created in 2002 by Nicolas Orlowski, who reused the name of the Artcurial gallery founded in 1975 and hired auctioneers Francis Briest, Hervé Poulain and Rémy Le Fur. A subsidiary of the Dassault Group, it is headquartered at the Hôtel Marcel Dassault on the Rond-Point des Champs-Élysées.
Source: [Wikipedia (CC BY-SA)](https://en.wikipedia.org/wiki/Artcurial), checked 2026-11-03.

## Secondary files (`_snd`)
`<date>_Artcurial[_<sale number>]_snd.csv` (and `<date>_Artcurial_press.csv` for the press): lots of this house that the house's own
documents do not give (1 file, 12 lots).
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
