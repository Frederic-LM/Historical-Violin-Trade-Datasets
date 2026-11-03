# Sotheby's (London)

Sotheby's (Sotheby Parke Bernet from the late 1970s to the early 1980s), the musical instrument sales in London,
1968-2005. From the author's printed copies: the house's catalogues, its printed price lists and sale-room results
sheets.

## Files
One file per sale, of three kinds:
- `<date>_Sothebys_<code name or sale number>.csv`: the catalogue (the lots typed: heading, text, estimate) with the
  prices of the house's price list. Sotheby's gives each sale a code name, printed on the catalogue and the price list
  (CATHEDRALE, ALETTA...): it stands for the sale number where the house printed no number.
- `<date>_Sothebys_catalogue.csv`: a catalogue whose price list is not held: text and estimates; a hammer price only
  where one is written by hand in the author's copy (price_source: Cross-checked where a second, independent record
  gives the same lot at this hammer + the premium; else Secondary).
- `<date>_Sothebys_<code name or sale number>_prices.csv`: a price list or results sheet whose catalogue is not held.

Catalogues were typed for their violin-family pages: lots of other instruments are not in the files.

## Columns at this house
| Column | Here |
|---|---|
| title | the lot's heading, as printed (attribution words: by / ascribed to / attributed to / School of / workshop of / labelled, defined in the catalogue's glossary) |
| description | the lot's text, as printed (label, wood, varnish, length of back, certificates) |
| estimate_low, estimate_high | GBP, as printed; empty where the catalogue says "Refer Dept." (see estimate_text) |
| status | sold; unsold (results sheets: bought in, see last_bid); withdrawn; unsold or withdrawn (in the catalogue, not in the list); empty: not known |
| hammer | the hammer price, where the list or results sheet prints it, or written by hand (see price_source); empty where the list prints only the price with the premium |
| price_with_fees | where the list prints it: from 1984 the lists give "the hammer price plus 10% buyer's premium (rounded down)" |
| last_bid (extra) | the bid at which a bought-in lot stopped (results sheets) |
| estimate_text, vat_on_hammer, vat_mark, note (extra) | the estimate as printed; VAT on the hammer (the catalogue's dagger, the list's star); a figure read otherwise than printed, and why (below) |

## Fees
| Sales | Buyer's premium |
|---|---|
| to Aug 1975 | none: the buyer paid the hammer (a commission was charged to the seller) |
| Sep 1975 - 1978 | 10 % of the hammer |
| 1979 - 1992 | 10 % of the hammer, + VAT on the premium |
| 1993 - 1999 | 15 % up to USD 100 000 (from 1 January 1993), 10 % above |
| March 2002 | 20 % up to GBP 10 000, 15 % to GBP 60 000, 10 % above, + VAT on the premium |
| November 2005 | 20 % up to GBP 100 000, 12 % above |

Seller's commission (catalogue of 22 November 1984): 15 % up to GBP 500, 10 % above (plus VAT for UK / EEC sellers
not registered for VAT).

## Price lists (`_prices`)
`<date>_<house>_<sale number>_prices.csv`: the house's own printed price list of a sale ('Prices Realised' printed at
the back of the next catalogue, a sale-room results sheet), typed from a paper copy: lot, status, and the price as
the list prints it: the hammer, or the price with the premium (price_with_fees), or both; the other column is empty. No lot text, no
maker: the list gives none. `last_bid` = the bid a bought-in lot stopped at (Sotheby's results sheets); `vat_mark` =
the list's '*' / '**' (VAT on the hammer). price_source = Primary.
`note` (here and in the house files of the typed catalogues): where a figure is read otherwise than the paper prints it,
why. Mostly the house's own misprints, checked on the paper (the note says so): a lot number printed twice or out of
place, read as the missing lot; a price printed out of its column, read as the figure its digits stand under; a price the house
corrected in a later catalogue. Everywhere else the price list is as printed.


## About the house
Sotheby's is an auction house founded in London on 11 March 1744 by the bookseller Samuel Baker, today headquartered in New York; it is one of the world's largest brokers of fine and decorative art, jewellery and collectibles, and was taken private in 2019 when Patrick Drahi bought it.
Source: [Wikipedia (CC BY-SA)](https://en.wikipedia.org/wiki/Sotheby%27s), checked 2026-11-03.

## Secondary files (`_snd`)
`<date>_Sothebys[_<sale number>]_snd.csv` (and `<date>_Sothebys_press.csv` for the press): lots of this house that the house's own
documents do not give (191 files, 10040 lots).
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
