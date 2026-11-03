# Christie's (New York, London, Amsterdam)

Christie's: the "Fine Musical Instruments" sales of New York (christies.com), single instrument lots of other sales,
and the London sales of the author's printed catalogues and price lists (below).

## Files
One file per sale: `<date>_Christies_<sale number>.csv`, the shared columns (see the Raw README), in this order,
then the house's extra columns.

## Columns at this house
| Column | Here |
|---|---|
| title | the lot's two heading lines joined by " / " (maker line, then type / place / date), as published |
| description | the lot's full text as published (it starts with the heading); line breaks written " / " |
| status | sold (the house shows only sold lots of these sales) |
| hammer | not given by the house: empty |
| price_with_fees | the house's "price realised": hammer + buyer's premium |
| currency | USD (New York), GBP (London), EUR (Amsterdam) |
| sale_location (extra) | the sale room, as published |
| provenance, literature, exhibited, lot_essay (extra) | the lot page's sections, as published (certificates are often in lot_essay) |

## Fees
Buyer's premium, % of the hammer, in three bands. The house gives only the price with premium; these bands give a
round hammer for every lot of the New York sales. Seller's commission not published.

| Sales (New York) | Buyer's premium |
|---|---|
| Oct 2007 – Apr 2008 | 25 % up to USD 20 000, 20 % up to USD 500 000, 12 % above |
| Oct 2008 – Jun 2014 | 25 % up to USD 50 000, 20 % up to USD 1 000 000, 12 % above (no lot above USD 1 000 000 to check) |

London, Amsterdam and the sales after 2014 (one to three lots each): not known.

## London: printed catalogues and price lists (1984-1993, 2002)
From the author's printed copies, the Christie's sales of musical instruments in London (King Street and South
Kensington):
- `<date>_Christies_<sale code>.csv` (e.g. `1990-11-21_Christies_ZENANA-4412.csv`, the sale of the "Mendelssohn"
  Stradivari): the catalogue (the lots typed: heading, text, estimate) with the prices of the house's printed list.
- `<date>_Christies_catalogue.csv`: a catalogue whose price list is not held: text and estimates; a hammer price only
  where one is written by hand in the author's copy (price_source: Cross-checked where a second, independent record
  gives the same lot at this hammer + the premium; else Secondary).
- `<date>_Christies_<sale number>_prices.csv`: a printed price list whose catalogue is not held.

The London lists of 1985-1992 print "the aggregate of the final bid and the premium" (price_with_fees; hammer empty)
and only the sold lots ("Where lots fail to sell they will not be shown"): a catalogue lot missing from the list is
"unsold or withdrawn". The South Kensington list of 13 March 2002 prints the hammer ("prices exclude the buyer's
premium").

| London sales | Buyer's premium |
|---|---|
| April 1984 - July 1985 | 8 % of the final bid (price list of 3 July 1985; the earlier sales measured on the hammers written by hand) |
| November 1987 - 1992 | 10 % of the final bid, + VAT on the premium |
| March 1993 (South Kensington) | 15 % of the hammer, + VAT on the premium |
| March 2002 (South Kensington) | 17.5 % of the hammer (lots up to GBP 30 000) |

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
Christie's is a British auction house founded in London in 1766 by James Christie; its first sale is dated by the company to 5 December 1766. Owned since 1998 by François Pinault's Groupe Artémis, it sells fine art and luxury goods from King Street, St James's, and worldwide.
Source: [Wikipedia (CC BY-SA)](https://en.wikipedia.org/wiki/Christie%27s), checked 2026-11-03.

## Secondary files (`_snd`)
`<date>_Christies[_<sale number>]_snd.csv` (and `<date>_Christies_press.csv` for the press): lots of this house that the house's own
documents do not give (138 files, 4072 lots).
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
