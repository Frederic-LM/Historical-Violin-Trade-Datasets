# Phillips (London)

Phillips (Phillips, Son & Neale in the 1970s), the musical instrument sales in London, 1975-1998 (the house was taken
over by Bonhams in 2001). From the author's printed copies: the house's catalogues and its printed price lists.

## Files
One file per sale, of three kinds:
- `<date>_Phillips_<sale number>.csv`: the catalogue (the lots typed: heading, text, estimate) with the hammer prices
  of the house's printed price list.
- `<date>_Phillips_catalogue.csv`: a catalogue whose price list is not held: text and estimates; a hammer price only
  where one is written by hand in the author's copy (price_source = Secondary), otherwise no price.
- `<date>_Phillips_<sale number>_prices.csv`: a printed price list whose catalogue is not held: lot, status, hammer.

The price list of a sale ("Prices Realised") is printed at the back of the catalogue of a later sale. It gives the sold
lots only ("Any omitted lots were unsold or withdrawn"): a catalogue lot missing from the list is "unsold or
withdrawn". Catalogues were typed for their violin-family pages: lots before the first typed lot, and the sections of
other instruments, are not in the files.

## Columns at this house
| Column | Here |
|---|---|
| title | the lot's first sentence, as printed (attribution words: by / ascribed to / attributed to / School of / workshop of / labelled) |
| description | the rest of the lot's text, as printed |
| estimate_low, estimate_high | GBP, as printed, where the catalogue prints an estimate |
| status | sold (in the price list); unsold or withdrawn (in the catalogue, not in the list); empty: no price list |
| hammer | the hammer price of the house's price list ("The prices shown are the hammer price and do not include the Buyer's Premium"); or written by hand (price_source = Secondary) |
| price_with_fees | not printed: empty |
| vat_mark, vat_on_hammer (extra) | the list's or the catalogue's star: VAT on the hammer of that lot (from 1989 the lists say the starred price contains it) |
| note (extra) | where a figure is read otherwise than the paper prints it, and why (below) |

## Fees
Buyer's premium, from the catalogues' conditions of sale:

| Sales | Buyer's premium |
|---|---|
| to Aug 1978 | none: the buyer paid the hammer |
| Sep 1978 - Feb 1980 | 10 % of the hammer |
| Mar 1980 - 1990 | 10 % of the hammer, + VAT on the premium |
| 1995 | 15 % of the hammer up to GBP 30 000, 10 % above, + VAT on the premium |
| 1998 | 15 % of the hammer, + VAT on the premium |

Seller's commission (1987 catalogue): 12.5 % up to GBP 1 000, 10 % above, negotiable above GBP 50 000.

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
Phillips is a London auction house founded in 1796 by Harry Phillips, a former clerk of James Christie; its UK operations were merged into Bonhams in 2001, while the international business, later Phillips de Pury, was bought by Russia's Mercury Group in 2008 and later returned to the Phillips name.
Source: [Wikipedia (CC BY-SA)](https://en.wikipedia.org/wiki/Phillips_(auctioneers)), checked 2026-11-03.

## Secondary files (`_snd`)
`<date>_Phillips[_<sale number>]_snd.csv` (and `<date>_Phillips_press.csv` for the press): lots of this house that the house's own
documents do not give (111 files, 3416 lots). One file per sale: when we hold the house's own file of a sale, its secondary
information is in that file (a price on the house's lot, `price_source` Secondary or Cross-checked; a lot the house's
file lacks as a line with `text_source` Secondary) and there is no `_snd` file for that sale.
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
