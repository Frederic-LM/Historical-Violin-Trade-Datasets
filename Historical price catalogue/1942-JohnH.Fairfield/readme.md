# Fairfield 1942 cohort

American violin makers listed with prices in 1942, followed in the auction record to today.

This folder accompanies Section 7.3 of Levi Mazloum, F. (2026), *The verdict never rendered* (manuscript under review). It tests whether the market sorts contemporary makers over time. The test uses a group of makers fixed in advance by someone else, not makers chosen after their fortunes were known.

## Source

Fairfield, J. H. (1983). *Known violin makers* (4th ed.). Virtuoso Publications. (Original work published 1942)

The American section (pp. 129–188) gives short biographies of "contemporary American craftsmen, professional and amateur", usually with prices. This text is unchanged from the 1942 first edition. In his introduction (p. 127), Rembert Wurlitzer notes that Fairfield "wisely decided to refrain from any attempt to rank the various makers listed".

I transcribed the section from a scan. A check of every entry against the book (October 2026) corrected a few prices and added five entries missed in the first transcription (Chapin, Chase, Gates, Truetschler, Urdahl); see *Corrections* below. Because the 1983 edition is still in copyright, the files give names, prices and coded facts only, not the biographical text.

## Files

- `fairfield_1942_american_entries.csv`: one row for each of the 176 entries. Each row gives:
  - the cohort status and the words in the entry it rests on;
  - the price as printed;
  - the violin price used;
  - the matched auction name, or the reason a name was left unmatched;
  - the book page.
- `fairfield_1942_cohort_outcomes.csv`: auction outcomes for each entry.
- `cohort.py`: reproduces the outcomes and the figures below:
  `python cohort.py fairfield_1942_american_entries.csv all_violin_sales_combined_namefixed.csv`

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

**Prices.** The 1942 price is the midpoint of the violin price stated in the entry. Where an entry also prices violas, cellos or bows, only the violin price is used. Where it gives an earlier and a later price, the range runs from the earliest to the latest. An entry giving only a ceiling ("up to", "as high as") or a floor ("and up") uses that figure as both ends. These rows are marked in the file.

## How outcomes were measured

The rules below were fixed before any matching.

**Matching.** A maker is matched to an auction name only when the surname and first name agree and the birth year or city is consistent. Doubtful cases are listed and left unmatched.

**Survival.** A maker counts as surviving if at least one of his violins sold at auction after 1990.

**Real growth.** Growth runs from the 1942 price to the median auction price of 2010–25, both in 2023 dollars:
- prices are deflated with the US CPI-U annual average (1942 = 16.3; 2023 = 304.702; the 2024 index is used for 2025);
- the rate runs from 1942 to the median year of those sales.

**Two questions.**
1. Did the 1942 price rank the survivors above the others? This is measured by the area under the curve (AUC) from a Mann–Whitney test.
2. Did it predict later growth? This is measured by Spearman's rho.

Auction data: Levi Mazloum, F. (2026). *Violin Auction Trends Analytics* (Version 1.1). Zenodo. https://doi.org/10.5281/zenodo.23085844

## Results

Of the 69 professionals working in 1942:
- 27 (39%) still appear at auction after 1990, so about three in five have left no trace there;
- 18 have enough recent sales to measure real growth. Of these:
  - three rose by more than 1% a year: Sacconi (+2.6%), Becker (+2.0%) and Sindelar (+1.1%);
  - ten stayed within 1% either way;
  - five fell by more than 1% a year: Stenger, Virzi, Phillips, Kaye and Heckel.

Makers who were dearer in 1942 were somewhat more likely to remain at auction (median 1942 price $400 against $250; AUC 0.73, p = 0.006). That is to be expected, since auction houses take only instruments above a certain value.

The 1942 price did not predict who would later rise or fall (rho = −0.05, p = 0.84). The three dearest makers of 1942 went three ways: Sacconi rose, Kaye fell, and Litto disappeared from the record.

| Group | Makers | At auction after 1990 | Rose / flat / fell | AUC | rho |
|---|---|---|---|---|---|
| Main | 69 | 39% | 3 / 10 / 5 | 0.73 (p = 0.006) | −0.05 |
| Broad | 118 | 32% | 4 / 14 / 9 | 0.72 (p < 0.001) | −0.35 |

**Names checked by hand.** Decisions rest on identity only (name, birth year, city), not on prices:
- Oscar A. Gemünder is matched to "Oscar Henry Gemunder": same first name, born 1872 in New York; only the middle name differs;
- John Alfred Gould is matched: full name and city (Boston) agree; the birth year differs (1860 in the book, 1866 in the dataset);
- Claude Heskett is not in the auction data (the only Heskett there is his father) and counts as absent;
- Marcel Aerts appears at auction only jointly with his father and is left unmatched;
- Curt Wunderlich appears only as "C. A. Wunderlich" and is left unmatched.

## Reproducing the figures

The compiled auction transaction file is not redistributed (see the Violin Auction Trends Analytics repository). `fairfield_1942_cohort_outcomes.csv` gives, for every entry, the 1942 price, the number of sales, the first and last sale year, survival after 1990, the median 2010–25 price and the real growth rate, so every figure above can be recomputed from it. `cohort.py` rebuilds that file from the entries and the transaction file.

## Corrections

October 2026, after a check of every entry against the book:
- violin prices corrected where a viola, cello or bow price had been taken: Ricker ($125–150), Simonson ($150–250), Kovanda (bows only, no violin price);
- prices added or adjusted: Chamberland ($100–350), Heskett ($100–500, earlier to later price); Jenks's $200 removed (the violin sold was made by A. W. Howe);
- status corrected under the rules above: Chamberland (a farmer making violins in his spare time) and Thorp (employed by an oil company) moved from the broad group to *left out*;
- five entries added: Chapin, Truetschler and Urdahl (main group), Chase and Gates (broad group);
- Gemünder and Gould matched (see above).

The conclusions are unchanged: the main group grew from 66 to 69 makers, and the growth results (3 / 10 / 5) did not move.

## Limitations

- **"Disappeared" means absent from this auction dataset.** Private sales and small regional auctions are not covered.
- **The 1942 figures and the later figures are different kinds of price.** The 1942 figures are makers' asking prices for new instruments; the later ones are auction resales. The gap between the two pulls every growth rate down. The ranking of makers is less affected.
- **Several growth rates rest on one or two sales.** The number of sales is given for each maker.

## Citation

Levi Mazloum, F. (2026). *Historical violin trade datasets* (Version [x]) [Data set]. Zenodo. https://doi.org/[DOI]

## Licence

Mozilla Public License 2.0, as for the rest of the repository. The source book remains under its own copyright.
