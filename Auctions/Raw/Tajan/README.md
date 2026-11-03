# Tajan: secondary files


## About the house
Tajan is a Paris auction house whose origins go back to 1971, when Jacques Tajan became a partner in the Ader study; it was called Ader-Picard-Tajan from 1973 and Étude Jacques Tajan from 1994. Owned by LVMH in 2001-2003 and by Rodica Seward from 2003, it was sold in October 2025 to Bail Art founder Édouard Challemel du Rozier.
Source: [Wikipedia (CC BY-SA)](https://fr.wikipedia.org/wiki/Tajan_(maison_de_vente)), checked 2026-11-03.

## Secondary files (`_snd`)
`<date>_Tajan[_<sale number>]_snd.csv` (and `<date>_Tajan_press.csv` for the press): lots of this house that the house's own
documents do not give (15 files, 324 lots).
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
