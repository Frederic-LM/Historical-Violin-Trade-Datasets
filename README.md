# Historical Violin Trade Datasets

Transcription, enrichment and compilation: Frédéric Levi Mazloum.

This repository gathers datasets on the historical trade in violins, built from primary sources. It currently holds three kinds of source:

- **Auction results:** the lots of violin-family instruments and bows sold at auction, as the auction houses published them.
- **Ledgers:** the day-to-day records of a dealer or workshop, such as purchases, resales and exports.
- **Price catalogues:** published lists of makers with their prices at a given date.

The datasets were compiled for the Violin Auction Trends Analytics project. Each folder has its own README: source, columns, method and, where it differs, licence.

## Contents

| Folder | Source | Type | Coverage |
|---|---|---|---|
| `Auctions/Raw/` | Primary: the auction houses' own results pages, documents, catalogues and price lists (13 houses, 648 sales, 140 281 lots); secondary: other sources where no house document is held (95 houses, 1 487 files, 39 802 lots); press: contemporary reports (85 files, 1 391 lots) | Auction results, lot by lot: one file per sale, one folder per house | Europe, North America, Japan and South Korea, 1829–2026 |
| `Ledgers/Lupot–Gand–Bernardel–Caressa–Français/` | Fonds Lupot–Gand–Bernardel–Caressa–Français, Musée de la musique, Paris (E.981.8.29 and E.981.8.30) | Dealer ledgers: sales register and export journal | Paris, 1920–1944 |
| `Historical price catalogue/1942-JohnH.Fairfield/` | Fairfield, J. H., *Known violin makers* (1942; 4th ed. 1983), American section | Directory of makers with prices, coded and matched to the auction record | United States, 1942 |

### Auction results

These are research data, built because no academic source of auction data for violins existed and the commercial compilations do not document their method; checked against the houses' own documents, they proved to hold many errors. The files here are not a copy of those compilations: they are built from the houses' own documents and checked lot by lot, with every lot of a sale, where the compilations list only part of it. `Auctions/README.md` explains the problem, with examples, and the checks made here.

The raw layer (`Auctions/Raw/`) has three kinds of file, in each house's folder. Primary files: every lot held for 648 sales (140 281 lots), sold, unsold and withdrawn alike, with the house's own text and prices, unchanged. Secondary files (`_snd`, 1 487 files, 39 802 lots, 1829–2026): lots known from other sources where no house document is held, facts only. Press files (`_press`, 85 files, 1 391 lots, 1857–1911): sales reported by The Violin Times and The Cremona. Each line says where its words and its price come from: the house's own document (Primary), another source (Secondary), a secondary price that a second, separate record confirms (Cross-checked), or the press (Press); `Auctions/COVERAGE.md` gives the shares and names the sources. Prices are in the house's currency, as the hammer price or the price with the buyer's premium, never mixed; the premium of each house and period is in the house's README. The older London sales of Phillips, Sotheby's and Christie's come from the author's printed catalogues and the houses' printed price lists; the compiled online databases list only part of their lots. See `Auctions/README.md`.

### Lupot–Gand–Bernardel–Caressa–Français ledgers

Violin transactions of the Paris house Caressa & Français and its successor Émile Français, from two registers held at the Musée de la musique:
- **Purchase and resale register** (E.981.8.29): 898 entries, 1920–1944.
- **Export journal** (E.981.8.30): 148 entries, 1926–1939, cross-referenced to the register.

Each entry gives the maker, the dates and prices of purchase and sale, repair costs, and the parties to the transaction.

### Fairfield 1942 catalogue

The American section of Fairfield's directory lists the makers working in the United States in 1942, with their prices. The section has 176 entries. Each entry is coded by status (professional, amateur and so on) and matched to the auction record. The folder holds the coded data; the study of which makers priced in 1942 are still traded today, and at what real return, is in the analysis repository [Violin Auction Trends Analytics](https://github.com/Frederic-LM/Violin-Auction-Trends-Analytics/tree/main/fairfield_1942). The biographical text is not included, because the 1983 edition is still in copyright.

## How the data are prepared

Where possible, a dataset keeps a diplomatic transcription of the source, exactly as written. Anything added later goes in separate enrichment columns. These include:
- instrument type;
- standardised maker names and identifications;
- attribution to a house or workshop;
- price calculations;
- cross-references;
- match confidence;
- discrepancy flags.

The transcription itself is never overwritten. Discrepancies found in the historical records are kept as they are, not harmonised.

Prices are recorded in their original currency unless a folder states otherwise. Long price series should be read with inflation, currency reforms and wartime disruption in mind.

Matching rules and any other assumptions are documented in each folder.

## Licence

The repository is distributed under the Mozilla Public License 2.0 (see `LICENSE`). Where a source carries its own terms, these take precedence and are stated in the dataset's folder.

## Citation

Please cite the dataset you use, as given in its folder, and the repository:

> Levi Mazloum, F. (2026). *Historical Violin Trade Datasets* [Data set]. https://github.com/Frederic-LM/Historical-Violin-Trade-Datasets

## Contributions

Corrections, source checks and further ledgers, catalogues or auction documents are welcome. If you hold a primary
document that is not here (an auction catalogue, a printed price list, a dealer's ledger), please contact the author,
by opening an issue or through https://www.ruederome.com. To add data yourself, follow the method of the folder (see
its README), then submit a pull request from a dedicated branch with a short note on the source.

## Disclaimer

These datasets are research resources. Errors and ambiguities may remain, both in the transcriptions and in the historical records themselves. Please check critical information against the original sources.
