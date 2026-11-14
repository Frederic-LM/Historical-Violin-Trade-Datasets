# Auction results by house (raw layer)

Violin-family instruments and bows sold at auction, transcribed from the auction houses' own documents: results
pages, results documents, lot lists and printed catalogues (primary), completed by secondary and press files where
no house document is held. One folder per house, one CSV file per sale, and `sales.csv`, one line per primary sale.

## Why this layer
Studies of violin prices rely on auction data, from the houses themselves or from compiled databases. Neither
usually documents how the figures were collected, and small errors (a price with or without fees, a wrong date, a
misread maker) are copied from one study to the next. A method that is not stated hides its biases. This layer keeps
the houses' own figures and words, unchanged, so that every later reading can be checked against them.

## Rules
- **The house's words and figures, as published.** Nothing is recomputed, converted or corrected in the files; the
  few corrections we believe necessary are explained in the house's README (e.g. Bonhams, 10 March 2010, lot 248).
- **Nothing of ours.** No maker identification, no attribution category, no currency conversion, no inflation, no
  instrument type: those readings belong to the enhanced layer (repository *Violin Auction Trends Analytics*).
- **Every lot we hold**, also the ones a price study would leave out: unsold and withdrawn lots, the trade and
  student lots, bows, accessories. Leaving them out would make the market look better than it is.
- **Empty means not recorded**: the house did not give it, or we did not read it. Someone may fill it one day.
- **Prices in the house's currency, of the kind the house published**: the hammer price, or the price with the
  buyer's fees, or both. The two are never mixed in one column. The fees of each sale are in `sales.csv` and in the
  house's README.

## Files
- `<House>/<date>_<House>_<sale>.csv`: one sale; the shared columns below, in this order, then the house's own
  extra fields (explained in its README).
- `<House>/README.md`: the house's sources, what each column holds at this house, its fees, notes.
- `<House>/<date>_<House>[_<sale>]_snd.csv`: secondary lots (no house document held): facts only (day, lot, maker as
  written, type, price); a month-only date leaves `sale_date` empty and keeps the month in the file name.
- `<House>/<date>_<House>_press.csv`: lots reported by the contemporary press (1857–1911), with page and link.
- `sales.csv`: one line per primary file: sale number and title, first and last day, place, country, currency, language of
  the text, number of lots, sold, unsold, withdrawn, status not given, the kind of price published, the text and
  price sources, buyer's premium.

## Shared columns
| Column | Content |
|---|---|
| sale_number | the house's sale number |
| sale_title | the sale's title |
| sale_date | the day the lot was sold (YYYY-MM-DD); empty if the document does not say |
| lot | the lot number, as printed |
| title | the lot's heading, as printed |
| description | the lot's text, as printed (in the house's language) |
| estimate_low, estimate_high | the estimate, in the sale currency |
| status | sold; unsold; withdrawn; "sold, price not published"; a house's own code (explained in its README); empty: not given |
| hammer | the hammer price, where the house gives it |
| price_with_fees | the price including the buyer's premium, where the house gives it |
| currency | the currency of the prices and estimates |
| text_source | where the words (title, description) come from: Primary; Secondary (below); empty: no text |
| price_source | where the price (hammer, price_with_fees) comes from: Primary; Cross-checked; Secondary; Press (below); empty: no price |

## Sources
The words and the price of a lot can come from different documents (e.g. the house's catalogue text, with a price
from records that compile auction results), so each line says both.
- **Primary**: the house's own published document (results page or document, catalogue, lot list).
- **Cross-checked** (price only): a figure the house did not publish, given alike by two independent records (same
  lot, same maker, the same price or prices that differ only by the house's premium): two or more sources, the
  author's own records (e.g. hammers written by hand in the sale room) and third-party records. Where records disagree, the
  figure kept is the one the checking confirmed, and the other is left out. E.g. the hammers written by hand in the
  author's catalogues of Sotheby's, Christie's and Bonhams sales, confirmed by a second record; the lots known only from
  compiled records.
- **Secondary**: a figure or wording the house did not publish, from one record only (a record that compiles auction
  results, or a hammer written by hand in a printed catalogue, e.g. Phillips, 30 June 1998), or from records that
  disagree. A record that rewrites the house's lot text in its own words: that wording is Secondary too.
- **Press**: a contemporary press report of the sale (one report, page and link given).
The records used besides the author's own are published compilations of auction results (databases and printed
yearbooks), named once in `../COVERAGE.md`. Only facts are taken from them, never their descriptions.

## Coverage (primary files)
| Folder | Years | Sales | Lots | Sold | Source of the house's data |
|---|---|---|---|---|---|
| `Aguttes/` | 2022–2026 | 9 | 861 | 861 | aguttes.com sale and lot pages, read 18 Oct 2026 |
| `Amati/` | 2018–2026 | 42 | 1 476 | 1 476 | the house's own results pages |
| `Artcurial/` | 2025 | 1 | 1 | 1 | the house's lot page and published result |
| `Bonhams/` | 2003–2015 | 44 | 13 157 | 8 291 | bonhams.com sale pages, read 19 Oct 2026 |
| `Christies/` | 1984–2026 | 35 | 4 405 | 3 771 | christies.com lot pages, read 17 Oct 2026; London: the author's printed catalogues and price lists |
| `Credit-Municipal/` | 2018–2026 | 9 | 134 | 122 | the house's results documents on interencheres.com, read 14 Nov 2026 |
| `De-Baecque/` | 2021–2025 | 6 | 71 | 71 | the house's results documents on interencheres.com (lot and hammer only), read 14 Nov 2026 |
| `Gardiner-Houlgate/` | 2019–2026 | 32 | 13 101 | 10 056 | musicalinstrument-auctions.co.uk results pages, read 20 Oct 2026, and the printed catalogues |
| `Ingles-Hayday/` | 2020–2026 | 12 | 2 229 | 1 669 | ingleshayday.com results pages, read 17 Oct 2026 |
| `Phillips/` | 1975–1998 | 132 | 32 833 | 24 545 | the author's printed catalogues and price lists |
| `Skinner/` | 2005–2021 | 28 | 10 235 | 8 771 | skinnerinc.com results archive, read 19 Oct 2026 |
| `Sothebys/` | 1968–2005 | 45 | 10 827 | 8 739 | the author's printed catalogues, price lists and results sheets |
| `T2-Auctions/` | 2016–2023 | 40 | 159 | 159 | the house's own results (Tarisio's online sales; part only) |
| `Tarisio/` | 1999–2026 | 162 | 14 482 | 14 482 | the house's own results archive |
| `Tarn/` | 2017 | 2 | 61 | 61 | the house's results documents on interencheres.com, read 14 Nov 2026 |
| `Vichy-Encheres/` | 1994–2026 | 84 | 52 952 | 41 010 | the house's results documents (also on interencheres.com), lot lists and catalogues (also the author's typed catalogues) |

Sales whose own documents we do not hold (most Sotheby's, Christie's and Phillips London sales: only those of the
author's printed copies are primary here; Brompton's, Dorotheum...) appear through their secondary files (`_snd.csv`),
in the house's folder. The full count per layer, house and period is in `../COVERAGE.md`.

## Use
Prices are not comparable as they stand: a hammer is not a price with fees, and the premium changed over time and
between houses (`sales.csv`, the house READMEs). Convert and deflate with care, and say which you did. The method of
the price study that uses these files, every choice with its reason, is in the *Violin Auction Trends Analytics*
repository.
