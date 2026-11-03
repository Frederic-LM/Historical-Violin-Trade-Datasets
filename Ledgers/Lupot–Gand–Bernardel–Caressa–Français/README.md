# Dealer ledgers: Caressa & Français / Émile Français (Paris, 1920–1944)

Transcription and enrichment: Frédéric Levi Mazloum.

Violin and viola transactions of the Paris house Caressa & Français and of its successor Émile Français, from two
registers of the Fonds Lupot–Gand–Bernardel–Caressa–Français, Musée de la musique, Philharmonie de Paris
(https://archivesmusee.philharmoniedeparis.fr, shelfmarks E.981.8.29 and E.981.8.30).

Licence of this folder: CC BY 4.0 (it takes precedence over the repository's licence for these files).

## Files

| File | Content |
|---|---|
| `Registre_E981_8_2934_enhanced.csv` | Purchase and resale register E.981.8.29, 1920–1944: 898 entries, one per instrument, with enrichment columns |
| `Journal_exportations_E981_8_30_matched.csv` | Export journal E.981.8.30, 1926–1939: 148 entries, with a reference to the matching register entry |

## Register: columns

**Transcription** (as written in the register, in French; never overwritten):

| Column | Content |
|---|---|
| `NUMEROS D'ORDRE` | the register's entry number |
| `AUTEURS` | the maker, as written (e.g. "Gand Frères, Paris 1862", "Vieux Français") |
| `DATES D'ACHAT` | date of purchase (dd/mm/yyyy) |
| `VENDEURS` | the seller, as written |
| `PRIX D'ACHAT` | purchase price |
| `PRIX DES REPARATIONS` | cost of repairs |
| `PRIX DE REVIENT` | cost price (purchase + repairs) |
| `DATES DES VENTES` | date of sale |
| `PRIX VENDU` | sale price |
| `ACHETEURS` | the buyer, as written |

**Enrichment** (added; corrections and readings live here, never in the transcription):

| Column | Content |
|---|---|
| `INSTRUMENT_TYPE` | violin or viola |
| `COUNTRY`, `CENTURY` | the maker's country and century, where the maker is identified |
| `HOUSE_MADE` | TRUE: an instrument of the firm's own production |
| `HOUSE` | the firm keeping the register |
| `ACHETEURS DETAIL*` | who the buyer is (e.g. "Rudolph Wurlitzer Co., major American instrument dealer"), or the kind of buyer |
| `VENDEUR_TYPE`, `ACHETEUR_TYPE_REV` | the kind of seller / buyer: private, trade, musician, occupation |
| `VENDEUR_CANON`, `ACHETEUR_CANON` | a standard name for a seller / buyer identified (e.g. "A. Vidoudez (Geneva)") |
| `VENDEUR_CONF`, `ACHETEUR_CONF` | confidence of that identification ("verified") |
| `CONSIGNMENT` | TRUE: a sale with no purchase recorded, read as an instrument sold on consignment |
| `CHANNEL` | B2B (sold to the trade) or B2C (to a private buyer) |
| `MARGIN_PCT` | (sale price − cost) / cost, in %; cost = `PRIX DE REVIENT`, or `PRIX D'ACHAT` where there is no cost price |
| `HOLD_DAYS` | days between purchase and sale |
| `EXPORT_REF` | the matching entry of the export journal (row, exact or fuzzy match) |
| `EXPORT_DATE`, `EXPORT_BUYER_DETAIL`, `EXPORT_INSTRUMENT_DETAIL`, `EXPORT_PRICE` | the export journal's date, buyer, instrument and declared value for that entry |
| `EXPORT_PRICE_DIFF` | where the register's price and the declared export value differ |
| `DISCREPANCY_STATUS` | how a difference between the two registers was settled (a transcription typo corrected, or a real discrepancy kept) |

## Export journal: columns

| Column | Content |
|---|---|
| `date` | date of the export |
| `buyer` | the consignee, as written (name, town, country) |
| `instrument details` | the instrument, as written (French, with an English translation in brackets) |
| `price` | declared value |
| `REGISTER_MATCH` | the matching register entry |

## Method notes

- Prices are nominal French francs, not adjusted for inflation. The franc lost much of its value in 1914–1926 and
  1940–1944: keep this in mind when comparing periods.
- Two transcription typos were corrected against the original images (entry 424: 3 500 F; entry 561: 18 000 F).
  Real differences between the register's price and the declared export value are kept as they are, never averaged
  (entries 384, 556, 698, 709).

## Citation

> Levi Mazloum, F. (2026). Caressa & Français / Émile Français dealer ledgers, 1920–1944 [Data set]. In *Historical
> Violin Trade Datasets*. https://github.com/Frederic-LM/Historical-Violin-Trade-Datasets. Source: Musée de la
> musique, Paris, E.981.8.29 and E.981.8.30.

Corrections are welcome: please open an issue or a pull request.
