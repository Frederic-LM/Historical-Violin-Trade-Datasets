# Hôtel Drouot: secondary files


## About the house
The main auction complex of Paris, opened in 1852 on the initiative of the Compagnie des commissaires-priseurs at 9 rue Drouot; the present building dates from 1976-1980. It is a sale room, not one firm: sales take place there daily under several dozen auctioneering firms. Lots are listed under Hôtel Drouot when the record names the place but not the auctioneer, as in the press reports, so that the minor auctioneers who sold there are not lost.
Source: [Wikipedia (CC BY-SA)](https://fr.wikipedia.org/wiki/H%C3%B4tel_Drouot), checked 2026-11-03.

## Secondary files (`_snd`)
`<date>_Hotel-Drouot[_<sale number>]_snd.csv` (and `<date>_Hotel-Drouot_press.csv` for the press): lots of this house that the house's own
documents do not give (10 files, 19 lots).
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
