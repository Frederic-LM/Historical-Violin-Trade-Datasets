# Fairfield 1942: American violin makers and their prices

The American makers listed with prices in 1942, coded by status and matched to the auction record.

This folder holds the data. The study built on it (who is still traded today, and at what real return) is in the
analysis repository: [Violin Auction Trends Analytics, `fairfield_1942/`](https://github.com/Frederic-LM/Violin-Auction-Trends-Analytics/tree/main/fairfield_1942),
with the scripts, the outcomes per maker and the results. It accompanies Section 7.3 of Levi Mazloum, F. (2026),
*The verdict never rendered* (manuscript under review).

## Source

Fairfield, J. H. (1983). *Known violin makers* (4th ed.). Virtuoso Publications. (Original work published 1942)

The American section (pp. 129–188) gives short biographies of "contemporary American craftsmen, professional and amateur", usually with prices. This text is unchanged from the 1942 first edition. In his introduction (p. 127), Rembert Wurlitzer notes that Fairfield "wisely decided to refrain from any attempt to rank the various makers listed".

I transcribed the section from a scan. A check of every entry against the book (October 2026) corrected a few prices and added five entries missed in the first transcription (Chapin, Chase, Gates, Truetschler, Urdahl). The columns `price_source` and `price_note` record how each price was read. Because the 1983 edition is still in copyright, the file gives names, prices and coded facts only, not the biographical text.

## File

`fairfield_1942_american_entries.csv`: one row for each of the 176 entries.

| Column | Content |
|---|---|
| `maker` | the name as printed |
| `cohort` | `main`, `broad` or `excluded` (see below) |
| `status`, `status_cues` | the status and the words in the entry it rests on |
| `price_as_transcribed` | the price as printed |
| `violin_price_min_usd`, `violin_price_max_usd` | the violin price used |
| `price_source` | `as printed`, `set by hand (violin price only)` or `no price` |
| `price_note` | how a price or a name match was settled |
| `auction_name_matched` | the maker's name in the auction record (the maker file of the analysis repository), when matched |
| `ambiguous_not_matched` | the reason a name was left unmatched |
| `book_page` | the page in the 1983 edition |

69 entries are in the main group, 49 more in the broad group, 58 are left out.

## Who is in the cohort

Status was set from the text of each entry before any auction data were consulted.

**Main group.** A maker is a professional when the entry states a livelihood in the trade:
- his own shop, atelier or business;
- employment with a dealer, firm or workshop;
- repair or restoration work;
- a guild master's qualification.

**Broad group.** The main group plus the makers whose entries say nothing either way.

**Left out:**
- amateurs and non-commercial makers;
- makers whose main occupation lay elsewhere (physicians, professors, teachers, an electrician);
- entries mixing amateur and trade descriptions;
- firms with no instruments of their own;
- bow makers, since the auction data cover violins only;
- makers who had died before 1942.

**Borderline entries.** A handful were settled by reading the full entry. The reason is recorded in the status column.

## Prices

The 1942 price is the violin price stated in the entry. Where an entry also prices violas, cellos or bows, only the violin price is used. Where it gives an earlier and a later price, the range runs from the earliest to the latest. An entry giving only a ceiling ("up to", "as high as") or a floor ("and up") uses that figure as both ends. These rows are marked in the file.

## Matching to the auction record

The rules were fixed before any matching. A maker is matched to an auction name only when the surname and first name agree and the birth year or city is consistent. Doubtful cases are listed and left unmatched. Decisions rest on identity only (name, birth year, city), not on prices:
- Oscar A. Gemünder is matched to "Oscar Henry Gemunder": same first name, born 1872 in New York; only the middle name differs;
- John Alfred Gould is matched: full name and city (Boston) agree; the birth year differs (1860 in the book, 1866 in the auction record);
- Claude Heskett is not in the auction record (the only Heskett there is his father) and counts as absent;
- Marcel Aerts appears at auction only jointly with his father and is left unmatched;
- Curt Wunderlich appears only as "C. A. Wunderlich" and is left unmatched.

The auction lots themselves are in this repository, under `Auctions/`.

## Citation

Levi Mazloum, F. (2026). *Historical violin trade datasets* [Data set]. Zenodo. https://doi.org/10.5281/zenodo.20681720 (all versions; each release has its own DOI on that page)

## Licence

Mozilla Public License 2.0, as for the rest of the repository. The source book remains under its own copyright.
