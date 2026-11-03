# Auctions

Auction records for violins, violas, cellos, double basses and their bows, compiled from the auction houses' own
documents for historical and statistical research.

Transcription, compilation and checking: Frédéric Levi Mazloum.

## Research data

These files are research data. They were built for a study of long-run price trends of violin makers (the *Violin
Auction Trends Analytics* project) and are published so that the figures of that study, and of any other, can be
checked lot by lot. They are offered as they are: errors may remain, and corrections are welcome.

## Coverage

The data come in three layers, told apart by the file name and by the `text_source` / `price_source` columns:

| Layer | Files | Sales | Lots | Houses | Years |
|---|---|---|---|---|---|
| **Primary**: the house's own documents | `<date>_<house>_<sale>.csv` | 626 | 138 858 | 13 | 1968–2026 |
| **Secondary**: other sources; `Cross-checked` when a second source agrees | `<date>_<house>_snd.csv` | 1 503 | 41 300 | 95 | 1829–2026 |
| **Press**: contemporary press reports, with page and link | `<date>_<house>_press.csv` | 85 | 1 391 | 4 | 1857–1911 |

All three sit in the same house folder under `Raw/`. For the secondary and press files a "sale" is one house on one day (or in one
month, when only the month is known). The split per house and per period is in `COVERAGE.md`.

The primary files cover 626 sales of thirteen houses (138 858 lots, 103 152 of them sold); the list per house, with the
source of each, is in `Raw/README.md`. A sale is added once it is complete and checked.

### Why they were built

When this research began there was no academic source of auction data for violins. The data available came from
commercial databases that compile auction results, and from the houses' websites for recent years. None of them
documents its method: how a lot was recorded, whether a price includes the buyer's premium, what was done with unsold
lots, how a maker was identified. Published price studies rest on these compilations, and their errors pass from one
study to the next.

Checked lot by lot against the houses' own documents, the compiled records proved useful, but unreliable in ways that
matter for a price study: they mix price bases, miss most of the cheap and unsold lots, and carry a small share of
wrong prices and wrong makers. A study built on them alone measures a different, more flattering market than the one
in the sale room. Some examples:

- **Prices on another basis.** For 16 to 28 % of the lots checked, the compiled price is not on the house's basis: the
  price with the buyer's premium where the house gives the hammer, or the reverse. The basis is not always stated, and
  the premium itself changed over time (none at the London houses before September 1975, 10 % then, 15 % and more from
  1993, about 25 % today): mixing the two bends a long price series.
- **Wrong prices and wrong makers.** About 1 to 1.5 % of the prices checked are simply wrong, and about 2 % of the lots
  are given under another maker or another lot number. At Christie's, 21 November 1990, a Collin-Mézin violin (lot
  299, estimate £700–1 000) sold for £715 according to the house's printed list; a compiled record gives £2 200. A
  Pressenda sold at Bonhams on 18 March 1996 appears at £95 000 in one record and at £265 913 in another.
- **Missing lots.** In the sales checked here (several hundred sales where the house's complete list is held), the
  compiled records list only part of each sale: on average between about 30 % and 40 % of its lots, depending on the
  database, and above all the lots that sold. This is measured on those sales only; it is not a claim about every sale
  a database covers. A study built on them sees fewer unsold lots and fewer cheap instruments than the sale room did.
- **Lots counted twice, or sold when they were not.** The same lot recorded twice (once with the day, once with the
  month only); lots that the house lists as bought in or withdrawn given as sold. A Stradivari of 1719 from Otto von
  Booth's collection is recorded as sold for £1 500 at Puttick & Simpson on 16 June 1911; The Cremona of 17 July 1911
  reports that it "did not reach the reserve price at £1500".
- **Lots with no sale.** Thousands of compiled records give a price and a month but no auction house, so they cannot
  be checked at all.

The houses' own documents are not free of errors either. Phillips printed lot 162 of 15 May 1980, a Nicolò Amati, at
£2 700 and corrected it to £27 000 in a later catalogue. Sotheby's printed a price of "143000" for a Thomas Dodd cello
in 1984, one column out of place, for £14 300. Price lists print a lot number twice, or skip one.

### What was done

- **The house's own document first.** Every lot comes, wherever possible, from the house itself: its results pages
  and documents for recent sales, and, for the older London sales of Phillips, Sotheby's and Christie's, the printed catalogues
  and price lists of the author's collection, typed lot by lot.
- **Every line states its source.** Two columns say where the words and where the price of a lot come from:
  - Primary: the house's own document;
  - Secondary: any other source (the author's own notes, published compilations of auction results, the press);
  - Cross-checked: a secondary price that a second, separate record gives alike (the same price, or one differing only
    by the house's premium). Two records count as one where one visibly copies the other (same wording, same errors).
- **Every price states its basis.** The hammer price and the price with the buyer's premium are never mixed in one
  column. The premium of each house and period was checked in the conditions of sale and the price lists and, where
  neither prints it, measured on the prices themselves: a price with the premium turns back into a round hammer only
  with the right rate. Christie's London charged 8 % in 1984–1985, not the 10 % usually assumed; Phillips charged none
  before September 1978.
- **Misprints checked on the paper, and documented.** A figure read otherwise than printed, such as the two examples
  above, keeps a note in the file saying what the paper prints and why it is read otherwise. Typing slips of our own
  copies were corrected against the paper; everything else is as printed.
- **Every lot kept**, sold, unsold or withdrawn, instruments of every quality, and bows. Leaving out the lots that did
  not sell would make the market look better than it was.
- **Nothing added.** No maker identification, conversion, inflation adjustment or price estimate is written into these
  files: those readings belong to the analysis, where each choice is documented.

## Relation to the compiled records

- **Built from the houses' own documents** (primary) wherever they exist, sale by sale, and checked lot by lot.
- **Secondary sources** (the author's notes, the press, published compilations of auction results) are used to
  cross-check a house's lot and, where no house document is held, as the source of the lot itself. Every line says
  which, and those lots are in their own files (`_snd.csv`, `_press.csv`).
- **Facts only:** from a compilation, only the facts of a sale are taken (house, day or month, lot number, maker as
  written, type, price); its descriptions, images and notes are not copied. The compilations used are named once, in
  `COVERAGE.md`.

## Contributing

Contributions are welcome, and needed: no one holds all the catalogues and price lists.
- **You hold a primary document that is not here** (a catalogue, a printed price list, a sale-room results sheet, a
  marked copy): please contact the author, by opening an issue on this repository or through
  https://www.ruederome.com.
- **You want to add sales yourself:** follow the same method, so that the files stay comparable. Keep the house's words
  and figures as printed; include every lot of the sale; state the source of each line (Primary, Cross-checked,
  Secondary) and the basis of each price (hammer, or price with the premium); keep a misprint as printed and explain
  your reading in `note`. Then open a pull request, with a short note on the source.
- **You find an error:** open an issue with the lot, the sale and your source.

## Contents

| Folder | Content |
|---|---|
| `Raw/` | One folder per house, one CSV file per sale: the primary files (the house's words and figures unchanged), and the secondary (`_snd.csv`) and press (`_press.csv`) files. `Raw/README.md` gives the rules, the shared columns, the sources of each line and the primary coverage per house; each house folder has its own README (sources, columns at that house, fees). `Raw/sales.csv` lists the primary sales. |

## Using the files

Prices are in the house's currency and of the kind the house published. Before comparing them, bring them to one
basis (hammer, or price with the premium) with the premium of each house and period (house READMEs, `Raw/sales.csv`),
convert and deflate as your question needs, and say what you did.

## Licence

The original research material (transcriptions, compilation, source and price-basis columns, notes) is distributed
under the Mozilla Public License 2.0, the licence of this repository, to the extent that the licence applies. The lot
descriptions are the auction houses' own texts, reproduced for research purposes; their rights remain with the houses.
