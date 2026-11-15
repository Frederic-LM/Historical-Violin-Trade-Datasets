# Millon / Apollium (Paris)

Millon (Millon & Associés) and Apollium are one house here. Apollium is the name under which Millon's
musical-instrument department held its sales from about 2014 to 2023. One folder, `Millon-Apollium`, and every file is
named `<date>_Millon-Apollium...` whichever name the sale was held under. Until 15 November 2026 this folder was
`Millon-Associes`, and the Apollium sales had a folder of their own (`Apollium`).

## About the house
Millon is a Paris auction house founded in 1928 as the Étude Robert by commissaire-priseur Jacques Robert; Joël-Marie Millon joined in 1990 and his son Alexandre has run the group since 2002. One of France's oldest auction houses, it bought the Italian house Il Ponte in 2024.
Source: [Wikipedia (CC BY-SA)](https://fr.wikipedia.org/wiki/Millon_(maison_de_vente_aux_ench%C3%A8res)), checked 2026-11-03.

## Files
House files, one per sale, `<sale day>_Millon-Apollium.csv`: from the house's own results pages (millon.com, past sales of
the musical-instrument department), 7 sales from 30 November 2022 to 29 May 2026. Every lot of the violin family and its
bows, the text as the page prints it (in French; the site cuts long texts: '...').

A lot shown with its estimate and no result has an empty `status`: its result may be missing from the page. Where a
published compilation of auction results gives that lot's price, it is filled in (`price_source` Secondary).

## Prices
`hammer` = the house's result ('Adjugé à' / 'Sold to'), without fees. The house's sale pages of 6 December 2024 and
5 June 2025 print 'Frais de vente : 25 % TTC' (buyer's fees, VAT included).

## Secondary files (`_snd`)
`<date>_Millon-Apollium[_<sale number>]_snd.csv` (and `<date>_Millon-Apollium_press.csv` for the press): lots of this house that the house's own
documents do not give (70 files, 921 lots).
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
