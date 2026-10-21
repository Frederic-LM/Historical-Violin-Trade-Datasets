# Christie's (New York, London, Amsterdam)

Christie's: the "Fine Musical Instruments" sales of New York, and single instrument lots of other sales.

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
