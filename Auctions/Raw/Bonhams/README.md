# Bonhams (London)

Bonhams, musical instrument sales (Knightsbridge / New Bond Street, London).

## Files
One file per sale: `<date>_Bonhams_<sale number>.csv`, the shared columns (see the Raw README), in this order.
Also `<date>_Bonhams_catalogue.csv` (19 Jun 2001, 14 Jul 2003): a printed catalogue, the house's text and estimate;
the hammer is the one written by hand in the author's copy at the sale (not the house's publication): price_source
Cross-checked where a second, independent record of the sale gives the same lot at this hammer + a premium, else
Secondary; last_bid = the
bid noted for an unsold lot. Before 2003 the buyer's premium was 10 % (1992–93, + VAT on the premium), 15 % up to
GBP 30 000 and 10 % above (Nov 1994 – Feb 2002), 17.5 % up to GBP 30 000 and 10 % above (Mar 2002 – Jan 2003)
(the house's catalogues, conditions of sale); 14 Jul 2003: 19.5 % up to GBP 70 000, 10 % above.

## Columns at this house
| Column | Here |
|---|---|
| title, description | as published; the title is the lot's first line; up to mid-2007 the house's site gives only a short title (e.g. "J. B Vuillaume"), no description |
| status | sold; unsold (the house's "bought in"); withdrawn; cs = the house's code, meaning not given (no price) |
| hammer | hammer price |
| price_with_fees | the house's price with buyer's premium |
| currency | GBP |

A few lots of other departments (paintings, furniture, valuations) are listed in these sales: kept as published.

## Fees
Buyer's premium, % of the hammer, in two bands (price_with_fees / hammer on every sold lot: 8 281 of 8 282 sold
lots fit exactly; the one exception is corrected, see below). Seller's commission not published.

| Sales | Buyer's premium |
|---|---|
| Feb – Mar 2003 | 17.5 % up to GBP 30 000, 10 % above |
| May 2003 – Feb 2005 | 19.5 % up to GBP 70 000, 10 % above |
| May 2005 – Mar 2011 | 20 % up to GBP 70 000, 12 % above |
| Oct 2011 – Aug 2013 | 25 % up to GBP 25 000, 20 % above |
| Oct 2013 – May 2015 | 25 % up to GBP 50 000, 20 % above |

Corrected by us: 10 Mar 2010, lot 248. Hammer GBP 120 000 (as published). The house's site gives GBP 144 000
with premium, i.e. 20 % on the whole hammer. It is the only lot of this sale above GBP 70 000; the three other
lots above GBP 70 000 of the period (Oct 2005, Nov 2006, Feb 2007) all pay 20 % up to GBP 70 000 and 12 % above.
We believe it is a site mistake. In this file, price_with_fees = GBP 140 000 (our figure, not the house's):
GBP 120 000 + 20 % of the first GBP 70 000 (GBP 14 000) + 12 % of the GBP 50 000 above (GBP 6 000).

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
Bonhams is a London auction house founded in 1793 by Thomas Dodd and Walter Bonham; the present company was formed in 2001 by the merger of Bonhams & Brooks with Phillips Son & Neale. Bought by the Epiris private equity fund in 2018 and by Pemberton Asset Management in October 2025, it also acquired Skinner and Bruun Rasmussen in 2022.
Source: [Wikipedia (CC BY-SA)](https://en.wikipedia.org/wiki/Bonhams), checked 2026-11-03.

## Secondary files (`_snd`)
`<date>_Bonhams[_<sale number>]_snd.csv` (and `<date>_Bonhams_press.csv` for the press): lots of this house that the house's own
documents do not give (105 files, 1700 lots).
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
