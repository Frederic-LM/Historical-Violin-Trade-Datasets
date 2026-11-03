# Les Domaines (DNID): secondary files


## About the house
Not a private house: the French State's own sales of surplus and confiscated movable goods (vehicles, art, jewellery, furniture), run by the Direction nationale d'interventions domaniales (DNID, Saint-Maurice), part of the tax administration. Sales are by auction or tender.
Source: [Ministry of Economy and Finance (Bercy)](https://www.economie.gouv.fr/particuliers/ventes-encheres-publiques), checked 2026-11-03.

## Secondary files (`_snd`)
`<date>_Les-Domaines-DNID[_<sale number>]_snd.csv` (and `<date>_Les-Domaines-DNID_press.csv` for the press): lots of this house that the house's own
documents do not give (1 file, 3 lots).
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
