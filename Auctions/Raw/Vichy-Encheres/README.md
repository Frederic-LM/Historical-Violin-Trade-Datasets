# Vichy-Enchères (Vichy)

Vichy-Enchères, "Instruments du quatuor" sales (all days: the trade and student lots of the first day included).
Three house sources, put together by lot number: the results documents (prices), the lot lists printed before the
sale (estimates) and the sale catalogues.

## About the house
Vichy Enchères is a French auction house based in Vichy, founded in 1983 by Guy Laurent and now run by the auctioneer Étienne Laurent. Specialising in musical instruments from its founding, its own site says it is the world leader in the sale of bows.
Source: [Vichy Enchères (own site)](https://vichy-encheres.com/en/vichy-encheres-3/presentation/), checked 2026-11-03.

## Files
One file per sale: `<first day>_Vichy-Encheres[_<sale number>].csv`, the shared columns (see the Raw README), in this
order. The Bernard Millant collection sales (own lot numbers) are files of their own: `..._Millant.csv`.

## Columns at this house
| Column | Here |
|---|---|
| sale_number | the house's sale number, where its documents give it (from 2024) |
| sale_title | empty, except the Millant collection sales |
| sale_date | the day the lot was sold, where the document says it; empty otherwise |
| title | not given by the house (one text per lot): empty |
| description | the lot's text, in French, as printed (results document; else the lot list; else the catalogue) |
| estimate_low, estimate_high | from the lot list or the catalogue, where we hold one (one figure: estimate_high empty) |
| status | sold; unsold ("NV", no price, "non vendu"); "sold, price not published" ("sur demande"); empty: the lot is in the list or catalogue but not in a results document |
| hammer | the price where the document gives the hammer ("adjudication", "prix marteau") |
| price_with_fees | the price where the document gives it with the buyer's fees ("montant net", "TTC") |
| currency | EUR |

Each price is in one of the two columns, as the document prints it; a few sales print some days with fees and others
without (Dec 2020, Nov 2021).

## Fees
Buyer's fees, % of the hammer, incl. VAT, from the house's conditions of sale and absentee bid forms.

| Sales | Buyer's fees |
|---|---|
| up to Dec 2013 | 23.92 % (20 % + VAT 19.6 %) |
| Jan 2014 – May 2023 | 24 % (20 % + VAT 20 %) |
| Nov 2023 – Dec 2025 | 25 % |

Buyers bidding through Interenchères pay its own fee on top (1.5 % + VAT for advance bids; some prices with fees show
hammer x 1.276, i.e. 3 % + VAT). Seller's commission: 12 % + VAT, the house's terms since the reform of French
auctions (2002); before, the commissaires-priseurs' state tariff, 7 % + VAT (decree of 29 March 1985).

## Notes
Sales with no results document (list or catalogue only): no price, status empty.
Bernard Millant collection I (29 Nov 2017): the house's results document (hammer prices; `title` = its short line,
`description` = the catalogue's text). Its results list only the lots sold: a catalogue lot missing from them says
`status` = unsold (not in the house's results). For collections II (5 Dec 2018) and III (27 Nov 2019) we have no
results document: where two secondary records of a lot agree (same lot number, same maker, one price = the other +
the house's premium), their price is written in the lot's line: those lines say `price_source` = Cross-checked
(the text and estimate are still the house's: `text_source` = Primary). Millant II: price with fees, 24 % incl. VAT; Millant III: hammer
(round figures).
Millant estimates: the house's estimate sheets. Millant I: the sheet says "Jeudi 29 novembre 2017"; 29 Nov 2017
was a Wednesday, as in the catalogue.
June 2021, 1 and 2 June: the results document gives lot numbers and prices only (no text).
May-June 2022 (31 May - 2 June): the results file gives no day headings: sale_date empty.
Unsold lots with hammer 0 (12 lots, Nov 2010 - Dec 2018): the results document prints 0 in the price column for these
unsold lots; kept as printed.
Nov 2017: on 6 lots the price is printed at the end of the lot text; written in its column.

## Secondary files (`_snd`)
`<date>_Vichy-Encheres[_<sale number>]_snd.csv` (and `<date>_Vichy-Encheres_press.csv` for the press): lots of this house that the house's own
documents do not give (80 files, 4399 lots).
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
