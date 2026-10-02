# Historical Violin Trade Datasets

Transcription, enrichment and compilation: Frédéric Levi Mazloum.

This repository gathers datasets on the historical trade in violins, built from primary sources. It currently holds two kinds of source:

- **Ledgers:** the day-to-day records of a dealer or workshop, such as purchases, resales and exports.
- **Price catalogues:** published lists of makers with their prices at a given date.

The datasets were compiled for the Violin Auction Trends Analytics project. Each folder documents its own source, columns, method and, where it differs, its licence.

## Contents

| Folder | Source | Type | Coverage |
|---|---|---|---|
| `Ledgers/Lupot–Gand–Bernardel–Caressa–Français/` | Fonds Lupot–Gand–Bernardel–Caressa–Français, Musée de la musique, Paris (E.981.8.29 and E.981.8.30) | Dealer ledgers: sales register and export journal | Paris, 1920–1944 |
| `Historical price catalogue/1942-JohnH.Fairfield/` | Fairfield, J. H., *Known violin makers* (1942; 4th ed. 1983), American section | Directory of makers with prices, followed to today in the auction record | United States, 1942 |

### Lupot–Gand–Bernardel–Caressa–Français ledgers

Violin transactions of the Paris house Caressa & Français and its successor Émile Français, from two registers held at the Musée de la musique:
- **Purchase and resale register** (E.981.8.29): 898 entries, 1920–1944.
- **Export journal** (E.981.8.30): 148 entries, 1926–1939, cross-referenced to the register.

Each entry gives the maker, the dates and prices of purchase and sale, repair costs, and the parties to the transaction.

### Fairfield 1942 catalogue

The American section of Fairfield's directory lists the makers working in the United States in 1942, with their prices. The section has 171 entries. Each entry is coded by status (professional, amateur and so on) and matched to the auction record. This shows which makers priced in 1942 are still traded today, and at what real return. The folder holds the coded data and the script that reproduces the results. The biographical text is not included, because the 1983 edition is still in copyright.

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

Corrections, source checks and further ledgers or catalogues are welcome. Please open an issue, or submit a pull request from a dedicated branch with a short note on the source.

## Disclaimer

These datasets are research resources. Errors and ambiguities may remain, both in the transcriptions and in the historical records themselves. Please check critical information against the original sources.
