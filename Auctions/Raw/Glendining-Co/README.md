# Glendining & Co.: secondary files


## About the house
London auctioneers founded in 1900 by Douglas Glendining, best known for coins and medals; it also held Oriental art sales. Phillips, Son & Neale took it over in the 1940s (1946 or 1947 depending on the source); Phillips merged into Bonhams in 2001. Bonhams closed its coin and medal department in July 2022, ending the Glendining name.
Source: [Antiques Trade Gazette](https://cdn.antiquestradegazette.com/print-edition/2022/july/2551/news/bonhams-closes-coins-and-medals-department), checked 2026-11-03.

## Secondary files (`_snd`)
`<date>_Glendining-Co[_<sale number>]_snd.csv` (and `<date>_Glendining-Co_press.csv` for the press): lots of this house that the house's own
documents do not give (37 files, 554 lots).
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
