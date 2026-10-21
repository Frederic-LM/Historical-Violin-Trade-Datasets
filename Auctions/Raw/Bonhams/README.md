# Bonhams (London)

Bonhams, musical instrument sales (Knightsbridge / New Bond Street, London).

## Files
One file per sale: `<date>_Bonhams_<sale number>.csv`, the shared columns (see the Raw README), in this order.

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
